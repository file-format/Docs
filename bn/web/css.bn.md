---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Cএসএস ফাইল ফর্মat
linktitle: CSS
description: LCSS ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা CSS ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## একটি CSS ফাইল কি? ##

CSS (ক্যাসকেডিং স্টাইল শীট) হল এমন ফাইল যা বর্ণনা করে যে কীভাবে HTML উপাদানগুলি স্ক্রীন, কাগজ ইত্যাদিতে প্রদর্শিত হয়। শৈলী এমবেড করার জন্য, \ <style>\</style> ট্যাগ ব্যবহার করা হয়। বহিরাগত স্টাইলশীটগুলি .css এক্সটেনশনের সাথে ফাইলগুলিতে সংরক্ষণ করা হয়। বাহ্যিক CSS-এর সাথে, আপনি সেই পৃষ্ঠাগুলির শৈলী আপডেট করতে একাধিক HTML পৃষ্ঠাগুলিতে এটি অন্তর্ভুক্ত করতে পারেন। এমনকি একটি একক CSS ফাইল একটি সম্পূর্ণ ওয়েবসাইট স্টাইল করতে ব্যবহার করা যেতে পারে।

## সংক্ষিপ্ত ইতিহাস ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. এর ফলে 1997 সালের নভেম্বরে CSS2 তৈরি হয় যা 12ই মে 1998-এ W3C সুপারিশ হিসাবে প্রকাশিত হয়েছিল। এই সংস্করণটি মিডিয়া-নির্দিষ্ট ডিভাইস যেমন প্রিন্টার, ডাউনলোডযোগ্য ফন্ট, টেবিল এবং উপাদান অবস্থানের জন্য সমর্থন যোগ করেছে। জুন 1999 সালে, CSS3 W3C-এর সুপারিশ হয়ে ওঠে। এটি ডকুমেন্টেশনকে মডিউলে বিভক্ত করেছে যেখানে প্রতিটি মডিউলের এক্সটেনশন বৈশিষ্ট্য CSS2-তে সংজ্ঞায়িত করা হয়েছে।

## কিভাবে CSS ফাইল ব্যবহার করবেন ##

একটি CSS ফাইল ব্যবহার করতে, আপনি এটিকে HTML নথির প্রধান বিভাগে অন্তর্ভুক্ত করুন। আপনি নীচে দেখানো হিসাবে ফাইল অন্তর্ভুক্ত করার জন্য লিঙ্ক ট্যাগ ব্যবহার করুন.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

লিঙ্ক ট্যাগের *href* অ্যাট্রিবিউটে CSS ফাইলের পাথ রয়েছে। এটি করার মাধ্যমে, অন্তর্ভুক্ত CSS ফাইলে থাকা প্রযোজ্য শৈলীগুলি HTML নথিতে প্রয়োগ করা হয়।

## CSS সিনট্যাক্স ##

একটি CSS নিয়ম দুটি উপাদান, একটি নির্বাচক এবং একটি ঘোষণা নিয়ে গঠিত। একটি নির্বাচক HTML নথিতে একটি উপাদান নির্দেশ করে। এটি হয় একটি এলিমেন্ট ট্যাগ, ক্লাসের নাম, আইডি নাম, একাধিক ট্যাগ যা শ্রেণিবিন্যাস দেখায়, ইত্যাদি হতে পারে। একটি ঘোষণায় সম্পত্তি এবং মান সমন্বিত শৈলী সংজ্ঞা থাকে। আপনি যে উপাদানটি পরিবর্তন করতে চান তার বৈশিষ্ট্যটি বৈশিষ্ট্যটি সনাক্ত করে এবং মানটি তার নতুন মানকে সংজ্ঞায়িত করে। প্রতিটি CSS নিয়মে একাধিক ঘোষণা থাকতে পারে। নিচের একটি CSS নিয়মের উদাহরণ।

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

উপরের উদাহরণে, আমাদের একটি নির্বাচক হিসাবে **h1** রয়েছে যা HTML নথিতে সমস্ত h1 ট্যাগ নির্বাচন করে। নিয়মে দুটি ঘোষণা রয়েছে, একটি ফন্ট-ওয়েট এবং অন্যটি রঙের জন্য। *ফন্ট-ওজন* এবং *রঙ* হল বৈশিষ্ট্য এবং *700* এবং *বনসবুজ* হল তাদের মান।

## CSS ব্যবহারের উদাহরণ ##

নিম্নলিখিতটি HTML নথির উদাহরণ এবং এটিকে স্টাইল করতে ব্যবহৃত স্টাইলশীট দেখায়। স্টাইল করা এবং প্লেইন এইচটিএমএল নথির তুলনা করার জন্য তুলনা চিত্রটিও যোগ করা হয়েছে

### HTML নথি ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS স্টাইলশীট ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### আউটপুট তুলনা ###

চিত্রের বাম দিকে প্রয়োগ করা শৈলী ছাড়াই HTML নথি প্রদর্শন করে এবং ডান দিকে প্রয়োগ করা শৈলী সহ HTML নথি প্রদর্শন করে।

{{< figure src="../CssExample.jpg" alt="উদাহরণ চিত্র" >}}

## তথ্যসূত্র ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

