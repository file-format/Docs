{
  "date": "2021-07-20",
  "keywords": [
    "MJS",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "Node.js ES Module File"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MJS - Node.js ES Module Javascript File",
  "description": "Learn about what is a MJS file and APIs that can create and open MJS file.",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mjs"
    }
  },
  "lastmod": "2021-07-20"
}

## What is an MJS file?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript modules are standard formta for packaging JavaScript code for reuse. MJS files can be opened in text editors such as Atom, Vim, Apple xCode, Microsoft Visual Studio, and Notepad.

## MJS File Format - More Information

MJS files are saved to disc as plain text format in JavaScript syntax. These can be opened in any text editor and are human readable. Since 2018, almost all major browsers now support ES modules. 

## Differences between ES modules and CommonJS

So what makes MJS files different than plain JS files? The difference between ES Modules and CommonJS can be summarized as follow:

 * No require, exports or module.exports
 * No \__filename or \__dirname
 * No JSON Module Loading
 * No Native Module Loading
 * No require.resolve
 * No NODE_PATH
 * No require.extensions
 * No require.cache

## References

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)
