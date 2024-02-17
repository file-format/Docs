---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM ফাইল ফরম্যাট - PYM ম্যাক্রো প্রিপ্রসেসর File
linktitle: PYM
description: LPYM ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা PYM ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## একটি PYM ফাইল কি?

একটি PYM ফাইল পাইথন প্রোগ্রামিং ভাষার উপর ভিত্তি করে একটি ম্যাক্রো প্রিপ্রসেসর ফাইল। এটি ভিআরভিস রিসার্চ এবং স্টোর ম্যাক্রো শর্টকাট দ্বারা তৈরি করা হয়েছে। PYM ফাইলটি যখন পাইথন ইন্টারপ্রেটারের প্রিপ্রসেসিং স্টেজ দ্বারা ব্যাখ্যা করা হয়, তখন এই শর্টকাটগুলি তাদের সম্পূর্ণ পাঠ্যের প্রতিস্থাপন হিসাবে প্রসারিত হয়। উপরন্তু, একটি তৃতীয়, ঐচ্ছিক অপারেশন যা একটি ম্যাক্রো প্রিপ্রসেসর দ্বারা সঞ্চালিত হতে পারে তা হল ফাইল অন্তর্ভুক্তি। লিনাক্সে নোটপ্যাড, নোটপ্যাড++, অ্যাপল টেক্সটএডিট এবং VI টেক্সট এডিটরগুলিতে PYM ফাইল খোলা যেতে পারে।

## PYM ফাইল ফরম্যাট

PYM ফাইলগুলি ডিস্কে প্লেইন টেক্সট ফাইল হিসাবে সংরক্ষণ করা হয়। একটি PYM ফাইল `#include` নির্দেশিকা ব্যবহার করে অন্যান্য ফাইলও অন্তর্ভুক্ত করতে পারে।

### PYM সিনট্যাক্স

PYM স্টেটমেন্টগুলি #begin python এবং #end python মার্কারগুলির মধ্যে অন্তর্ভুক্ত করা হয়েছে যেমনটি নীচে দেখানো হয়েছে৷

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### পিওয়াইএম ম্যাক্রো সম্প্রসারণ

PYM ম্যাক্রো সম্প্রসারণ দুটি ক্রম দ্বারা প্রতিনিধিত্ব করা হয় যেমন <[ এবং ]>। এগুলি বিশেষ html ট্যাগ এবং একটি লাইনে যে কোনও জায়গায় উপস্থিত হতে পারে। একটি সামান্য PYM উদাহরণ অনুসরণ করা হয়.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

PYM এর মাধ্যমে এটি চালানোর আউটপুট নিম্নরূপ:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## তথ্যসূত্র ##

 * [PYM - পাইথনের উপর ভিত্তি করে একটি ম্যাক্রো প্রিপ্রসেসর](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [পিওয়াইএম ইন্টারপ্রেটারস](https://github.com/interpreters/pym)

