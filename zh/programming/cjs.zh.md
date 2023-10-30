{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS File - CommonJS Code File",
  "description":"What is a .cjs file and how to open it?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

CJS 文件 - CommonJS 代码文件

什么是 .cjs 文件以及如何打开它？

## 什么是 CJS 文件？
CommonJS (CJS) 文件是包含以 CommonJS 语法编写的 JavaScript 代码的文件。 CommonJS 是一个模块系统，设计用于在前端 Web 浏览器之外的环境中工作，并且通常在服务器端 JavaScript 环境中使用，例如 Node.js。

## CJS 文件格式 - 更多信息
CJS 文件采用 CommonJS 语法编写，可以在任何文本编辑器（例如 Microsoft Notepad 或 Apple TextEdit）中进行编辑。 CommonJS 模块通常存储在单独的文件中，旨在封装和模块化代码，以实现更好的组织和可维护性。 这些模块使用所需的函数来导入依赖项，并使用 module.exports 或导出对象来公开可供代码其他部分使用的值和函数。

## CJS 代码示例
CommonJS 模块具有特定的语法和结构，其中包括导入其他模块和模块所需的函数等功能。导出或导出对象以从模块导出值、函数或对象。 这些模块用于封装和分离代码片段，使管理和维护大型 JavaScript 代码库变得更加容易。 这是 CommonJS 模块的基本示例：

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## 参考 ＃＃

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)