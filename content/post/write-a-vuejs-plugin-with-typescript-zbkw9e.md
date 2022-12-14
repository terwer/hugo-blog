---
title: 使用TypeScript写一个Vue-js插件
slug: write-a-vuejs-plugin-with-typescript-zbkw9e
url: post/write-a-vuejs-plugin-with-typescript-zbkw9e.html
date: '2022-12-07 16:52:30'
tags:
  - 插件
  - 使用
  - 可以
  - 一个
  - 方法
categories: []
lastmod: '2022-12-14 18:03:01'
toc: true
keywords: 插件,使用,可以,一个,方法
description: >-
  插件是使用其他属性方法assets等来增强vuejs功能集推荐的方法。用当前版本的vuejs在typescript中编写它们很简单但你可以在web上找到的建议通常是指旧版本不再适用。事实上你发现的矛盾建议可能会很令人困惑_我如何在我的插件中引用vuejs类型？好吧这里有一个一般的经验法则它会有所帮助并且永远不会让你再次谷歌搜索所需的语法。自从vuejs发布了自己的typings以来要解决这个问题您可以简单地查看它们。基本上有两种方法可以定义插件_要么使用基于函数的方法要么使用插件对象（实际上只是插件函数的
isCJKLanguage: true
---



[插件](https://vuejs.org/v2/guide/plugins.html) 是使用其他属性、方法、assets 等来增强 Vue.js 功能集推荐的方法。用当前版本*的* Vue.js 在 TypeScript 中编写它们很简单，但你可以在 Web 上找到的建议通常是指旧版本，不再适用。事实上，你发现的矛盾建议可能会很令人困惑：我如何在我的插件中引用 Vue.js 类型？好吧，这里有一个一般的经验法则，它会有所帮助，并且永远不会让你再次谷歌搜索所需的语法。

自从 Vue.js 发布了自己的 typings 以来，要解决这个问题，您可以简单地查看它们。基本上有两种方法可以定义插件：要么使用基于函数的方法，要么使用插件对象（实际上只是插件函数的包装器）。两者都可以在 Vue.js 包中找到（遵循版本 2.5.13 的代码）：`types/plugin.d.ts`​

```ts
import { Vue as _Vue } from "./vue";

export type PluginFunction<T> = (Vue: typeof _Vue, options?: T) => void;

export interface PluginObject<T> {
  install: PluginFunction<T>;
  [key: string]: any;
}
```

这正是您用作自己代码模板的内容。让我们编写一个插件函数！

```ts
import _Vue from "vue"; // <-- notice the changed import
import Axios from "axios";

// export type PluginFunction<T> = (Vue: typeof _Vue, options?: T) => void;
export function AxiosPlugin(Vue: typeof _Vue, options?: any): void {
    Vue.prototype.$http = Axios;
}
```

这就是实施所需的一切。对于示例，我只是在此处将 Axios 附加到 Vue。如果需要，您可以使用 or 功能进行更复杂的扩充。当然，如果需要，您可以使用自己的类型安全选项：`mixin`​​`directive`​

```ts
import _Vue from "vue";
import Axios from "axios";

// export type PluginFunction<T> = (Vue: typeof _Vue, options?: T) => void;
export function AxiosPlugin<AxiosPlugOptions>(Vue: typeof _Vue, options?: AxiosPluginOptions): void {
    // do stuff with options
    Vue.prototype.$http = Axios;
}

export class AxiosPluginOptions {
    // add stuff
}
```

## 配置和使用您的插件

所需的进一步步骤类似于任何其他插件。确保在启动时正确配置它：

```ts
import Vue from "vue";
import { AxiosPlugin } from "./AxiosPlugin";

// pass in your custom options as second parameter if applicable
Vue.use(AxiosPlugin); 
new Vue({
    // ...
});
```

如果你的插件像我上面的例子一样扩展了 Vue 原型，你需要提供类型，以便编译器可以正确地选择它（否则当你在组件中使用插件时，你会收到编译器错误）：

```ts
// put this in your source folder somewhere
// with a .d.ts extension the TS compiler will pick it up automatically
import { AxiosStatic } from "axios";

declare module 'vue/types/vue' {
  interface Vue {
    $http: AxiosStatic;
  }
}
```

在这里使用只是 Axios 的一个特点，不用担心。您只需在此处配置扩展属性或函数的类型，就可以在组件中使用：`AxiosStatic`​

```ts
// in your components
this.$http.[...] // use all Axios features, with full intellisense support
```

玩得愉快！

## 参考

[https://www.mistergoodcat.com/post/vuejs-plugins-with-typescript](https://www.mistergoodcat.com/post/vuejs-plugins-with-typescript)
