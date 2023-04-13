---
title: git删除所有分支
slug: /git-delete-all-branches-z22hnwp.html
url: ''
date: 2022-07-15 11:19:09
tags:
  - git
  - rm
  - repo
  - 删除
  - 分支
categories:
  - 经验分享
lastmod: ''
toc: true
keywords: git,rm,repo,删除,分支
description: todeleteallthelocaltagssimplerunthefollowingcommandgittag_xargsgittagdtodeleteremotetagsafterdeletingthelocaltagsbyrunningtheabovecommandyoucanrunthecomandbelowgitlsremotetagsrefsorigin_cutf_xargsgitpushorigindeletenote_replaceoriginwithyourremotehandler
isCJKLanguage: true
---
To delete all the local tags simple run the following command

```bash
git tag | xargs git tag -d
```

To delete remote tags after deleting the local tags by running the above command, you can run the comand below

```bash
git ls-remote --tags --refs origin | cut -f2 | xargs git push origin --delete
```

NOTE: replace origin with your remote handler