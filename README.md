[中文](https://github.com/hugo-next/hugo-theme-next-starter/blob/main/README.zh.md) | [English](#)

# Hugo NexT theme starter

## ⏬ Clone & Update Theme

Click the green button which name call `Use this template` and upper right corner on the page. Full information such as below image:

![Use Template](https://imgs.lisenhui.cn/hugo-next/use-hugo-next-starter.png)

After do that click the green button which name call `Create repository from template`, then will create your site code automatic, and clone it on your PC environment.

Remember that need use `git submodule` command to pull all things from `hugo-theme-next` at first time.

```
# First time
git submodule update --init --recursive
# Next time
git submodule update --remote --merge
```

> **Note**
> When you are in China, recommend to use `Gitee` repository url replace the submodule url in `.gitmodules` file content and then execute the above `Git` command line to improve the speed.

## 💻 Local Preview

Execute the `startup.sh` boot start script file which is under site root directory, when see some words like `stop` that mean success, and open browser visit
 [http://localhost:1414/](http://localhost:1414/) will enjoy yourself.

```shell
./startup.sh
```