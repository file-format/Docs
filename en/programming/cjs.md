{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CJS File - CommonJS Code File",
  "description": "What is a .cjs file and how to open it?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cjs"
    }
  },
  "lastmod": "2023-10-26"
}

## What is a CJS file?

A CommonJS (CJS) file is a file that contains JavaScript code written in CommonJS syntax. CommonJS is a module system designed to work in environments beyond frontend web browsers, and it's often used in server-side JavaScript environments, like Node.js.

## CJS File Format - More Informaiton

CJS files are written in CommonJS syntax and can be edited in any text editor such as Microsoft Notepad or Apple TextEdit. CommonJS modules are typically stored in separate files and are intended to encapsulate and modularize code for better organization and maintainability. These modules use the require function to import dependencies and the module.exports or exports object to expose values and functions that can be used by other parts of the code.

### CJS Code Example

CommonJS modules have a specific syntax and structure that includes features such as the require function for importing other modules and the module.exports or exports objects for exporting values, functions, or objects from a module.  These modules are used to encapsulate and separate pieces of code, making it easier to manage and maintain large JavaScript codebases. Here's a basic example of a CommonJS module:

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

## References

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
