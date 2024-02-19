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
  "title": "MJS - Node.js ES মডিউল জাভাস্ক্রিপ্ট ফাইল",
  "description": "একটি MJS ফাইল এবং API যা MJS ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন।",
  "linktitle": "MJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mjs-bn"
    }
  },
  "lastmod": "2021-07-20"
}

## একটি MJS ফাইল কি?

A file with .mjs extension is a JavaScript source code file that is used as an ECMA Module (ECMAScript Module) in Node.js applications. Node.js's natvie module system is CommonJS that is used to split the code in different files to keep the [JS](/web/js/) code organized. MJS is the only way used by Node.js to identify if the module is a CommonJS or an ES6. ECMAScript মডিউল হল প্যাকেজিং জাভাস্ক্রিপ্ট কোড পুনঃব্যবহারের জন্য স্ট্যান্ডার্ড ফর্মটা। MJS ফাইলগুলি টেক্সট এডিটর যেমন Atom, Vim, Apple xCode, Microsoft Visual Studio, এবং Notepad-এ খোলা যেতে পারে।

## MJS ফাইল ফরম্যাট - আরও তথ্য

MJS ফাইলগুলি জাভাস্ক্রিপ্ট সিনট্যাক্সে প্লেইন টেক্সট ফরম্যাট হিসাবে ডিস্কে সংরক্ষিত হয়। এগুলি যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে এবং এটি মানুষের পাঠযোগ্য। 2018 সাল থেকে, প্রায় সব প্রধান ব্রাউজার এখন ES মডিউল সমর্থন করে।

## ES মডিউল এবং CommonJS এর মধ্যে পার্থক্য

তাহলে কি MJS ফাইলগুলিকে প্লেইন JS ফাইলের চেয়ে আলাদা করে তোলে? ES মডিউল এবং CommonJS-এর মধ্যে পার্থক্য নিম্নলিখিত হিসাবে সংক্ষিপ্ত করা যেতে পারে:

 * কোন প্রয়োজন, রপ্তানি বা module.exports
 * কোন \__filename বা \__dirname নেই
 * কোন JSON মডিউল লোড হচ্ছে না
 * কোনো নেটিভ মডিউল লোড হচ্ছে না
 * কোন প্রয়োজন নেই. সমাধান
 * NODE_PATH নেই
 * প্রয়োজন নেই।এক্সটেনশন
 * প্রয়োজন নেই.ক্যাশে

## তথ্যসূত্র

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Difference Between JS And MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

