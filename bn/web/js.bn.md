---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Jএস ফাইল ফর্মat
linktitle: JS
description: Lজেএস ফাইল ফরম্যাট এবং এপিআই সম্পর্কে আয় করুন যা জেএস ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## একটি JS ফাইল কি? ##

JS (JavaScript) হল এমন ফাইল যা ওয়েব পৃষ্ঠাগুলিতে কার্যকর করার জন্য JavaScript কোড ধারণ করে। জাভাস্ক্রিপ্ট ফাইল .js এক্সটেনশনের সাথে সংরক্ষণ করা হয়। [HTML](/web/html/) নথির ভিতরে, আপনি হয় জাভাস্ক্রিপ্ট কোড এম্বেড করতে পারেন \ ব্যবহার করে <script>\</script> ট্যাগ করুন বা একটি JS ফাইল অন্তর্ভুক্ত করুন। [CSS](/web/css/) ফাইলের মতো, JS ফাইলগুলিকে কোড পুনঃব্যবহারযোগ্যতার জন্য একাধিক HTML নথিতে অন্তর্ভুক্ত করা যেতে পারে। জাভাস্ক্রিপ্ট HTML DOM ম্যানিপুলেট করতে ব্যবহার করা যেতে পারে।

## সংক্ষিপ্ত ইতিহাস ##

জাভাস্ক্রিপ্ট নেভিগেটর ব্রাউজারের অংশ হিসেবে 1995 সালের সেপ্টেম্বরে নেটস্কেপ দ্বারা লাইভস্ক্রিপ্ট নামে পাঠানো হয়েছিল। তিন মাস পরে এটির নামকরণ করা হয় জাভাস্ক্রিপ্ট। 1996 সালে, মাইক্রোসফ্ট JScript তৈরির জন্য রিভার্স-ইঞ্জিনিয়ারড নেভিগেটর এর দোভাষী। JScript ইন্টারনেট এক্সপ্লোরারের সাথে প্রকাশ করা হয়েছিল এবং জাভাস্ক্রিপ্টের চেয়ে খুব আলাদা ছিল।

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 1998 সালে, ECMAScript 3 1999 সালে মুক্তি পায়, এবং ECMAScript 4 এর কাজ 2000 সালে শুরু হয়েছিল কিন্তু কখনই সফল হয়নি।

জেসি জেমস গ্যারেট 2005 সালে একটি সাদা কাগজ প্রকাশ করেন যেখানে তিনি *Ajax* শব্দটি তৈরি করেছিলেন। এটি ওয়েব অ্যাপ্লিকেশানগুলি তৈরি করতে ব্যাকবোন হিসাবে জাভাস্ক্রিপ্ট ব্যবহার করে যা ব্যাকগ্রাউন্ডে ডেটা লোড করে এবং সম্পূর্ণ পৃষ্ঠা পুনরায় লোড এড়ায়। এর ফলে JQuery, Prototype, Dojo ইত্যাদি লাইব্রেরি তৈরি হয়।

Google released the Chrome browser with the V8 JavaScript engine in 2008. 2009 সালের প্রথম দিকে, সমস্ত প্রাসঙ্গিক কাজ একত্রিত করতে এবং জাভাস্ক্রিপ্টকে এগিয়ে নিয়ে যাওয়ার জন্য একটি চুক্তি করা হয়েছিল। এর ফলে ডিসেম্বর 2009 সালে ECMAScript 5 স্ট্যান্ডার্ড প্রকাশ করা হয়।

## কিভাবে JS ফাইল ব্যবহার করবেন ##

একটি JS ফাইল ব্যবহার করতে, আপনি এটি HTML নথিতে অন্তর্ভুক্ত করুন। আপনি নীচে দেখানো হিসাবে ফাইল অন্তর্ভুক্ত করার জন্য লিঙ্ক ট্যাগ ব্যবহার করুন.

```html
<script src="site.js"></script>
```

*স্ক্রিপ্ট* ট্যাগের *src* বৈশিষ্ট্য JS ফাইলের পাথ ধারণ করে। এটি করার মাধ্যমে, JS কার্যকারিতা HTML নথিতে যোগ করা হয়।

## জেএস সিনট্যাক্স ##

জাভাস্ক্রিপ্ট ফাইলে ভেরিয়েবল, অপারেটর, ফাংশন, কন্ডিশন, লুপ, অ্যারে, অবজেক্ট ইত্যাদি থাকতে পারে। নিচে জাভাস্ক্রিপ্টের সিনট্যাক্সের একটি সংক্ষিপ্ত বিবরণ দেওয়া হল।

- প্রতিটি কমান্ড একটি সেমিকোলন (;) দিয়ে শেষ হয়।
- ভেরিয়েবল ঘোষণা করতে *var* কীওয়ার্ড ব্যবহার করুন।
- Supports arithmetic operators ( + - * / ) মান গণনা করতে।
- একক লাইনের মন্তব্য // এর সাথে যোগ করা হয় এবং মাল্টিলাইন মন্তব্যগুলি /* এবং */ দ্বারা বেষ্টিত হয়।
- সমস্ত শনাক্তকারী কেস-সংবেদনশীল যেমন *মডেলন* এবং *মডেলনো* দুটি ভিন্ন ভেরিয়েবল।
- ফাংশন *ফাংশন* কীওয়ার্ড ব্যবহার করে সংজ্ঞায়িত করা হয়।
- বর্গাকার বন্ধনী [] ব্যবহার করে অ্যারে সংজ্ঞায়িত করা যেতে পারে।
- JS তুলনা অপারেটর সমর্থন করে যেমন ==, != , >=, !==, ইত্যাদি।
- ক্লাসগুলি *ক্লাস* কীওয়ার্ড ব্যবহার করে সংজ্ঞায়িত করা যেতে পারে।

## JS ব্যবহারের উদাহরণ ##

নিম্নলিখিত একটি সহজ ব্যবহার উদাহরণ জাভাস্ক্রিপ্ট ফাইল দেখায়.

### HTML নথি ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### জেএস কোড ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## তথ্যসূত্র ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

