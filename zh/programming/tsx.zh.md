{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX 文件 - React TypeScript 文件 - 什么是 .tsx 文件以及如何打开它?",
  "description":"了解 TSX React TypeScript 文件以及如何打开它.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-zh-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## 什么是 .tsx 文件？

“.tsx”文件扩展名通常与包含 **React** 代码的 TypeScript 文件相关联。 **TypeScript 是 JavaScript 的超集**，它为语言添加了静态类型，而 **React 是用于构建用户界面的 JavaScript 库**。 当一起使用 React 和 TypeScript 时，开发人员经常使用“.tsx”扩展名来表示它们的文件同时包含 TypeScript 和 JSX（React 的 JavaScript 语法扩展）。

## TSX 文件示例

TypeScript 允许您定义变量、函数参数等的类型。 您经常会在“.tsx”文件中看到 TypeScript 代码，指定 React 组件中使用的 props、状态和其他变量的类型。

````
// 示例：React 组件中的 TypeScript 代码
接口 MyComponentProps {
   名称：字符串；
   年龄：数字；
}
const MyComponent: React.FC<MyComponentProps> = ({ 姓名, 年龄 }) => {
   // 这里是组件逻辑
   return <div>{name} 已 {age} 岁。</div>;
};
````

## JSX（React 语法扩展）

JSX 是 React 推荐的 JavaScript 语法扩展。 它看起来类似于 XML/HTML，用于描述 UI 应该是什么样子。

````
// 示例：React 组件中的 JSX
const MyComponent: React.FC<MyComponentProps> = ({ 姓名, 年龄 }) => {
   return <div>{name} 已 {age} 岁。</div>;
};
````

“.tsx”文件通常包含使用函数组件或类组件的 React 组件的定义。

````
// 示例：“.tsx”文件中的 React 组件定义
const MyComponent: React.FC = () => {
   return <div>你好，React！</div>;
};
````

您经常会在文件的开头看到导入语句，引入必要的依赖项和模块。

````
// 示例：导入“.tsx”文件中的语句
从“反应”导入反应；
````

## 如何打开 .tsx 文件？

TSX 文件是纯文本文件，因此您可以在任何文本编辑器中打开它们，例如 记事本。 然而，这些是编码文件，需要由 IDE 打开，例如 Visual Studio 代码。