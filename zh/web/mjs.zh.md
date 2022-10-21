{
  "date" : "2021-07-20",
  "keywords" :["MJS","文件","扩展名","文件格式","文件扩展名","Node.js ES 模块文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES 模块 Javascript 文件",
  "description" :"了解什么是 MJS 文件以及可以创建和打开 MJS 文件的 API。",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## 什么是一 .mjs 文件？

扩展名为 .mjs 的文件是 JavaScript 源代码文件，在 Node.js 应用程序中用作 ECMA 模块（ECMAScript 模块）。 Node.js 的 natvie 模块系统是 CommonJS，用于将代码拆分到不同的文件中，以保持 [JS](/zh/web/js/) 代码的组织性。 MJS 是 Node.js 用来识别模块是 CommonJS 还是 ES6 的唯一方法。 ECMAScript 模块是用于打包 JavaScript 代码以供重用的标准格式。 MJS 文件可以在 Atom、Vim、Apple xCode、Microsoft Visual Studio 和记事本等文本编辑器中打开。

## MJS 文件格式 - 更多信息

MJS 文件以 JavaScript 语法以纯文本格式保存到光盘。这些可以在任何文本编辑器中打开并且是人类可读的。自 2018 年以来，几乎所有主流浏览器现在都支持 ES 模块。

## ES 模块和 CommonJS 的区别

那么是什么让 MJS 文件与普通 JS 文件不同呢？ ES Modules 和 CommonJS 的区别可以总结如下：

* 没有要求、导出或 module.exports
* 没有 \__filename 或 \__dirname
* 没有 JSON 模块加载
* 没有本地模块加载
* 没有 require.resolve
* 没有 NODE_PATH
* 没有 require.extensions
* 没有 require.cache

## 参考

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [JS 和 MJS 的区别](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

