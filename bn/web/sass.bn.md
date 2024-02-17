---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass ফাইল ফর্মat
linktitle: Sass
description: LSass ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা Sass ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## একটি SASS ফাইল কি? ##

সাস (সিনট্যাক্টিক্যালি দুর্দান্ত স্টাইল শীট) একটি প্রিপ্রসেসর স্ক্রিপ্টিং ভাষা। এটি [CSS](/web/css/) এ কম্পাইল করা হয়েছে এবং .sass এক্সটেনশনের সাথে সংরক্ষণ করা হয়েছে। Sass দুটি সিনট্যাক্স নিয়ে গঠিত, মূলটি ইন্ডেন্টেশনের উপর ভিত্তি করে যা .sass এক্সটেনশন ব্যবহার করে এবং CSS এর মত ব্লক ফরম্যাটিং সহ নতুন SCSS যা .scss এক্সটেনশন ব্যবহার করে।

## কেন Sass ব্যবহার করুন ##

Sass শৈলী বজায় রাখার জন্য সত্যিই সহায়ক কারণ এটি অনেক বৈশিষ্ট্য যেমন প্রবর্তন ভেরিয়েবল, নেস্টিং, মিক্সিন, আমদানি এবং নির্বাচক উত্তরাধিকার প্রদান করে যা শৈলীগুলির সাথে কাজকে মজাদার করে তোলে।

## কিভাবে SASS ফাইল ব্যবহার করবেন ##

SASS ফাইলগুলি সরাসরি [HTML](/web/html/) নথিতে অন্তর্ভুক্ত করা হয় না বরং HTML ফাইলে অন্তর্ভুক্ত CSS ফাইলে রূপান্তরিত হয়৷ আপনি [Official Sass Site](https://sass-lang.com/install)-এ দেওয়া নির্দেশাবলী অনুসরণ করে আপনার সিস্টেমের Sass ইনস্টল করতে পারেন৷

ইতিমধ্যে সংরক্ষিত SASS ফাইল রূপান্তর করে বা পরিবর্তনগুলি দেখে এবং ফাইলটি সংরক্ষিত হওয়ার সাথে সাথে রূপান্তর করে Sass কে CSS-এ রূপান্তর করা যেতে পারে। উভয়ের জন্য কমান্ড নীচে দেওয়া আছে.

### একবার রূপান্তর করুন ###

কমান্ডের প্রথম প্যারামিটার হল উৎস SASS ফাইল এবং দ্বিতীয় প্যারামিটার হল আউটপুট CSS ফাইল।

```cmd
sass main.sass main.css
```

### পরিবর্তনের জন্য দেখুন ###

উপরের কমান্ডটি একটি অতিরিক্ত *ওয়াচ* ফ্ল্যাগ দিয়ে চালানো যেতে পারে যা কমান্ডটি চলমান রাখে এবং Sass ফাইলটি সংরক্ষণ করার সাথে সাথে আউটপুট CSS তৈরি হয়।

```cmd
sass --watch main.sass main.css
```

## Sass সিনট্যাক্স ##

Sass ভেরিয়েবল, নেস্টিং, মিক্সিন, ইম্পোর্ট, সিলেক্টর ইনহেরিটেন্স ইত্যাদি সমর্থন করে। নিচে এই বৈশিষ্ট্যগুলির উদাহরণ দেওয়া হল।

### ভেরিয়েবল ###

একটি বোতামের জন্য প্রাথমিক রঙ বা প্যাডিংয়ের মতো পুনরায় ব্যবহারযোগ্য তথ্য সেট করতে ভেরিয়েবল ব্যবহার করা যেতে পারে। এটি কার্যকর প্রমাণিত হতে পারে যদি ভবিষ্যতে আপনার সেই তথ্যটি পরিবর্তন করার প্রয়োজন হয়, আপনি শুধুমাত্র একটি স্থানে এটি পরিবর্তন করেন এবং এটি সর্বত্র আপডেট হয়।

**সাস**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**জেনারেট করা CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### বাসা বাঁধা ###

সিএসএস নির্বাচকদের এইচটিএমএল এর অনুক্রমের অনুরূপ নেস্ট করা যেতে পারে। নিম্নলিখিত উদাহরণে, স্প্যানটি h1 ব্লকের ভিতরে অবস্থিত।

**সাস**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**জেনারেট করা CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### মিশ্রণ ###

মিক্সিনগুলি একই ধরণের বৈশিষ্ট্যগুলিকে একত্রিত করতে ব্যবহৃত হয় যা একাধিক জায়গায় ব্যবহৃত হয়। Mixins এছাড়াও পরামিতি সমর্থন করে।

**সাস**

**একটি মিশ্রণ ঘোষণা করা হচ্ছে**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**মিক্সিন ব্যবহার করে**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**জেনারেট করা CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### প্রসারিত করা ###

প্রসারিত/উত্তরাধিকার সেই ক্ষেত্রে উপযোগী প্রমাণিত হতে পারে যেখানে একজন নির্বাচকের বৈশিষ্ট্য অন্য নির্বাচকের সাথে ভাগ করা প্রয়োজন। নীচের উদাহরণে, *.error-notice* নির্বাচক *.error-text* নির্বাচকের সমস্ত বৈশিষ্ট্য নেয় এবং বর্ডার এবং প্যাডিং বৈশিষ্ট্য যোগ করে।

**সাস**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**জেনারেট করা CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### আমদানি ###

আপনি যদি আপনার স্টাইলগুলিকে কার্যকারিতার উপর ভিত্তি করে বিভিন্ন ফাইলে বা আপনি অনুসরণ করেন এমন অন্য কোনো কাঠামোতে গঠন করেন তাহলে আমদানি করা উপযোগী হতে পারে। আপনি এই সমস্ত ফাইলগুলিকে একটি প্রাথমিক SASS ফাইলে আমদানি করতে পারেন যা পরে CSS-এ রূপান্তরিত হয়। আমদানি করার সময়, আপনাকে আমদানি নির্দেশে ফাইল এক্সটেনশন নির্দিষ্ট করতে হবে না। Sass সমস্ত SASS ফাইল সরাসরি কম্পাইল করে। ফাইলগুলিকে সরাসরি কম্পাইল করার জন্য আমদানি করা এড়াতে, আপনি তাদের নামের শুরুতে আন্ডারস্কোর(_) যোগ করে তাদের আংশিক করতে পারেন। আংশিকগুলি সাধারণ Sass ফাইলের মতোই আমদানি করা হয়।

**সাস**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

আউটপুট CSS-এ সমস্ত আমদানি করা ফাইলের স্টাইল থাকবে।

## তথ্যসূত্র ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

