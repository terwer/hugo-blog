---
title: Github-Actions使用release-please实现自动发版
slug: githubactions-uses-reaseplease-to-implement-automatic-version-z1yj1lb
url: >-
  /post/githubactions-uses-reaseplease-to-implement-automatic-version-z1yj1lb.html
tags:
  - 自动
  - 发版
  - release
  - release-please
  - google
categories:
  - post
lastmod: '2023-03-06 22:01:55'
toc: true
keywords: 自动,发版,release,release-please,google
description: >-
  githubactions使用releaseplease实现自动发版​releaseplease​是一个来自于google​的自动发版工具基于githubactions可实现全自动发版。官网_https_githubcomgoogleapisreleaseplease上手在项目根目录的github​的workflows​里面新建一个releasepleaseyml​文件下面是一个准对的node项目的标准配置_on_push_branches_mainname_releasepleasejobs_relea
isCJKLanguage: true
---



​`release please`​ 是一个来自于 `Google`​ 的自动发版工具，基于 Github Actions 可实现全自动发版。

官网：[https://github.com/googleapis/release-please](https://github.com/googleapis/release-please)

## 上手

在项目根目录的 `.github`​ 的 `workflows`​ 里面新建一个 `release-please.yml`​ 文件，下面是一个准对的 node 项目的标准配置：

```yaml
on:
  push:
    branches:
      - main

name: release-please
jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      # create release pr
      - uses: google-github-actions/release-please-action@v3
        with:
          release-type: node
          package-name: release-please-action
          changelog-types: '[{"type":"feat","section":"Features","hidden":false},{"type":"fix","section":"Bug Fixes","hidden":false},{"type":"chore","section":"Miscellaneous","hidden":false}]'
      - run: echo "A release was created."
        if: ${{ steps.release.outputs.releases_created }}
      - run: echo "Release ${{ steps.release.outputs['packages/package-a--tag_name'] }} created for package-a."
        if: ${{ steps.release.outputs['packages/package-a--release_created'] }}

      # create tag
      - uses: actions/checkout@v3
      - name: tag major and minor versions
        if: ${{ steps.release.outputs.release_created }}
        run: |
          git config user.name github-actions[bot]
          git config user.email 41898282+github-actions[bot]@users.noreply.github.com
          git tag -d v${{ steps.release.outputs.major }} || true
          git tag -d v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
          git push origin :v${{ steps.release.outputs.major }} || true
          git push origin :v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
          git tag -a v${{ steps.release.outputs.major }} -m "Release v${{ steps.release.outputs.major }}"
          git tag -a v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} -m "Release v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}"
          git push origin v${{ steps.release.outputs.major }}
          git push origin v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}

      # publish to npm
      - uses: actions/setup-node@v1
        with:
          node-version: '16.x'
          registry-url: 'https://registry.npmjs.org'
      - name: Publish to npm
        if: ${{ steps.release.outputs.release_created }}
        run: |
          pnpm install
          pnpm build
          npm publish --access public
        env:
          NODE_AUTH_TOKEN: ${{ secrets.NPM_TOKEN }}
```

提交之后，正常情况就会在 main 的 push 事件触发之时，启动自动发版，包括发布到 npm 仓库。

如果不需要发不发哦 npm，可以使用下面的配置：

```yaml
on:
  push:
    branches:
      - main

name: release-please
jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      # create release pr
      - uses: google-github-actions/release-please-action@v3
        with:
          release-type: node
          package-name: release-please-action
          changelog-types: '[{"type":"feat","section":"Features","hidden":false},{"type":"fix","section":"Bug Fixes","hidden":false},{"type":"chore","section":"Miscellaneous","hidden":false}]'
      - run: echo "A release was created."
        if: ${{ steps.release.outputs.releases_created }}
      - run: echo "Release ${{ steps.release.outputs['packages/package-a--tag_name'] }} created for package-a."
        if: ${{ steps.release.outputs['packages/package-a--release_created'] }}

      # create tag
      - uses: actions/checkout@v3
      - name: tag major and minor versions
        if: ${{ steps.release.outputs.release_created }}
        run: |
          git config user.name github-actions[bot]
          git config user.email 41898282+github-actions[bot]@users.noreply.github.com
          git tag -d v${{ steps.release.outputs.major }} || true
          git tag -d v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
          git push origin :v${{ steps.release.outputs.major }} || true
          git push origin :v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
          git tag -a v${{ steps.release.outputs.major }} -m "Release v${{ steps.release.outputs.major }}"
          git tag -a v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} -m "Release v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}"
          git push origin v${{ steps.release.outputs.major }}
          git push origin v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}

```

## 注意事项

* 配置 npm token

  去 [https://www.npmjs.com/settings/terwer/tokens](https://www.npmjs.com/settings/terwer/tokens) 申请一个 `token`​ ，然后再项目里面设置：

  Settings -> Secrets and variables -> Actions -> `New repository secret`​ ，新建一个即可。

* Github 仓库权限设置

  注意：默认的 Github 仓库不允许拉取，需要开启权限才行。方法如下：

  转到 `https://github.com/OWNER/REPO/settings/actions`​ 页面向下划到 **Workflow Permissions** 然后切换到 s **Read and Write permissions 。**

  ​![](https://static.terwergreen.com/test/202303062150540.png)​

> 文章更新历史
> 2023-03-06 feat:初稿

‍