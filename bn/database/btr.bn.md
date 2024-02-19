{
  "date": "2021-09-06",
  "keywords": [
    "btr",
    "extension",
    "file",
    "file format",
    "Database File Type",
    "Database File Format",
    "Btrieve Database"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "বিটিআর ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা বিটিআর ফাইল তৈরি এবং খুলতে পারে।",
  "title": "BTR - Btrieve ডাটাবেস ফাইল",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-btr-bn"
    }
  },
  "lastmod": "2021-09-06"
}

## একটি BTR ফাইল কি?

.btr এক্সটেনশন সহ একটি ফাইল হল একটি ডাটাবেস ফাইল যা [Btrieve](https://www.actian.com/) লেনদেন ডেটাবেস অ্যাপ্লিকেশন দ্বারা তৈরি করা হয়েছে৷ রিলেশনাল ডাটাবেস ম্যানেজমেন্ট সিস্টেম (RBMS) এর বিপরীতে, Btrieve ইন্ডেক্সড সিকোয়েন্সিয়াল এক্সেস মেথড (ISAM) এর উপর ভিত্তি করে, যা দ্রুত পুনরুদ্ধারের জন্য ডেটা সংরক্ষণের একটি উপায়। BTR ফাইল রেকর্ডের একটি সংগ্রহ সঞ্চয় করে এবং প্রয়োজন অনুযায়ী রিপোর্ট তৈরি করতে ব্যবহৃত হয়। বিটিআর ফাইলগুলি পারভ্যাসিভ বিট্রিভ ডেটাবেস ম্যানেজার, পারভেসিভ পিএসকিউএল রক্ষণাবেক্ষণ ইউটিলিটি এবং লিজেন্ড সফটওয়্যার বিট্রিইভ ভিউয়ার ব্যবহার করে খোলা যেতে পারে।

## বিটিআর ফাইল স্ট্রাকচার - আরও তথ্য

একটি BTR ফাইলের কাঠামোতে প্রতিটি বাইটের অভ্যন্তরীণ ডেটা কাঠামো এবং প্রান্তিককরণ সর্বজনীনভাবে উপলব্ধ নয়। যাইহোক, Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * এমবারকাডেরো ডেলফি
 * GNU C/C++
 * মাইক্রো ফোকাস COBOL
 * মাইক্রোসফট ভিজ্যুয়াল বেসিক
 * মাইক্রোসফট ভিজ্যুয়াল সি++
 * ওয়াটকম সি/সি++

একটি BTR ফাইল থেকে ডেটা পুনরুদ্ধার করা এটির সাথে সম্পর্কিত DDF ফাইলের উপর নির্ভরশীল। DDF ছাড়া, এই ধরনের ফাইল থেকে তথ্য পুনরুদ্ধার করা সহজ হবে না।

## তথ্যসূত্র

* [Btrieve - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

