---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS ফাইল ফরম্যাট - Sass ক্যাসকেডিং স্টাইল সেet
linktitle: SCSS
description: LSCSS ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা SCSS ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## একটি SCSS ফাইল কি? ##

SCSS হল Sass (Syntactically Awesome Stylesheet) এর দ্বিতীয় সিনট্যাক্স যা ইন্ডেন্টেশনের পরিবর্তে বন্ধনী ব্যবহার করে। SCSS এমনভাবে ডিজাইন করা হয়েছে যে একটি বৈধ CSS3 ফাইলও একটি বৈধ SCSS ফাইল। SCSS ফাইল .scss এক্সটেনশনের সাথে সংরক্ষণ করা হয়।

## কেন SCSS ব্যবহার করবেন ##

যেহেতু ওয়েবসাইটগুলির ডিজাইন জটিল হয়ে উঠছে ফলে বড় [CSS](/web/css/) ফাইলগুলি তৈরি হচ্ছে৷ এই ধরনের ফাইল বজায় রাখা কঠিন। এখানেই SCSS আসে। SCSS CSS ডেভেলপমেন্টে ভেরিয়েবল, নেস্টিং, মিক্সিন, ইম্পোর্ট এবং সিলেক্টর ইনহেরিটেন্স প্রবর্তন করে। এই সংযোজনগুলি ডিজাইনের সাথে কাজকে অনেক বেশি মজাদার করে তোলে।

## কিভাবে SCSS ফাইল ব্যবহার করবেন ##

SCSS ফাইলগুলি সরাসরি CSS এর মত [HTML](/web/html/) নথিতে অন্তর্ভুক্ত করা হয় না৷ পরিবর্তে, SCSS ফাইলগুলিকে CSS ফাইলে রূপান্তরিত করা হয় যা HTML ফাইলে অন্তর্ভুক্ত করা হয়। আপনার সিস্টেমে SCSS ইনস্টল করতে, [Official Sass Site](https://sass-lang.com/install) এ দেওয়া নির্দেশাবলী অনুসরণ করুন৷
SCSS-কে CSS-এ রূপান্তর করতে, আপনি হয় ইতিমধ্যে সংরক্ষিত SCSS ফাইলকে রূপান্তর করতে পারেন অথবা পরিবর্তনগুলি দেখতে পারেন এবং ফাইলটি সংরক্ষিত হওয়ার সাথে সাথে রূপান্তর করতে পারেন। উভয়ের জন্য কমান্ড নীচে দেওয়া আছে.

### একবার রূপান্তর করুন ###

প্রথম প্যারামিটার হল উৎস SCSS ফাইল এবং দ্বিতীয় প্যারামিটার হল আউটপুট CSS ফাইল।

```cmd
sass main.scss main.css
```

### পরিবর্তনের জন্য দেখুন ###

কমান্ডটিতে একটি অতিরিক্ত *ওয়াচ** ফ্ল্যাগ রয়েছে যা কমান্ডটি চলমান রাখে এবং SCSS ফাইলটি সংরক্ষণ করার সাথে সাথে আউটপুট CSS তৈরি হয়।

```cmd
sass --watch main.scss main.css
```

## SCSS সিনট্যাক্স ##

SCSS ভেরিয়েবল, নেস্টিং, মিক্সিন, ইম্পোর্ট, সিলেক্টর ইনহেরিটেন্স ইত্যাদি সমর্থন করে। নিচে এই বৈশিষ্ট্যগুলির উদাহরণ দেওয়া হল।

### ভেরিয়েবল ###

ভেরিয়েবল ব্যবহার করে, আপনি সংরক্ষণ বোতামের জন্য প্রাথমিক রঙ বা পটভূমির রঙের মতো পুনরায় ব্যবহারযোগ্য তথ্য সেট করতে পারেন। আপনি যদি সেই তথ্যটি পরিবর্তন করতে চান তবে এটি দরকারী, আপনি এটি শুধুমাত্র একটি অবস্থানে পরিবর্তন করেন এবং এটি যেখানে ব্যবহার করা হয় সেখানে এটি আপডেট হয়।

**এসসিএসএস**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

আপনি HTML এর অনুক্রমের অনুরূপ CSS নির্বাচকদের নেস্ট করতে পারেন। নীচের উদাহরণে, স্প্যানটি h1 ব্লকের ভিতরে অবস্থিত।

**এসসিএসএস**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

মিক্সিনগুলি একই রকম বৈশিষ্ট্যগুলিকে একত্রিত করতে ব্যবহার করা যেতে পারে যা একাধিক জায়গায় একসাথে ব্যবহৃত হয়। আপনি mixins এ পরামিতি পাস করতে পারেন।

**এসসিএসএস**

**একটি মিশ্রণ ঘোষণা করা হচ্ছে**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**মিক্সিন ব্যবহার করে**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

প্রসারিত/উত্তরাধিকার এমন ক্ষেত্রে উপযোগী যেখানে এক নির্বাচকের বৈশিষ্ট্য অন্য নির্বাচকের সাথে ভাগ করা প্রয়োজন। নীচের উদাহরণে, *.error-notice* নির্বাচক *.error-text* নির্বাচকের সমস্ত বৈশিষ্ট্য নেয় এবং বর্ডার এবং প্যাডিং বৈশিষ্ট্য যোগ করে।

**এসসিএসএস**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

উদ্বেগ বিচ্ছিন্ন করতে আমদানি কার্যকর হতে পারে। আপনি স্টাইলগুলিকে এমনভাবে ভাগ করতে পারেন যাতে হেডার শৈলীগুলি একটি পৃথক ফাইলে থাকে, ফুটারের শৈলীগুলি একটি পৃথক ফাইলে থাকে, শৈলীগুলিতে ব্যবহৃত সমস্ত রঙের ভেরিয়েবলগুলি একটি পৃথক ফাইলে থাকতে পারে ইত্যাদি। এই কৌশলটি ব্যবহার করে, শৈলী সংগঠিত থাকে। আপনি শুধু আপনার প্রধান SCSS ফাইলে ফাইলগুলি আমদানি করুন যেমন নীচের উদাহরণে দেখানো হয়েছে। আপনাকে আমদানি নির্দেশে ফাইল এক্সটেনশন নির্দিষ্ট করতে হবে না। Sass সমস্ত SCSS ফাইল সরাসরি কম্পাইল করে। ফাইলগুলিকে সরাসরি কম্পাইল করা এড়াতে, আপনি তাদের নামের আগে আন্ডারস্কোর(_) যোগ করে তাদের আংশিক করতে পারেন। আপনি আন্ডারস্কোর ছাড়াই সাধারণ SCSS ফাইলের মতো আংশিক আমদানি করতে পারেন।

**এসসিএসএস**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

আউটপুট CSS-এ সমস্ত আমদানি করা ফাইলের স্টাইল থাকবে।

## References ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

