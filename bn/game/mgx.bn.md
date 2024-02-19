{
  "date": "2021-09-08",
  "keywords": [
    "mgx file",
    "mgx file format",
    "what is a mgx file",
    "file",
    "mgx example",
    "mgx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Age of Empires 2 সম্প্রসারণ রিপ্লে MGX ফাইল ফরম্যাট এবং APIs সম্পর্কে জানুন যা MGX ফাইল তৈরি ও খুলতে পারে।",
  "title": "MGX - সাম্রাজ্যের বয়স 2 সম্প্রসারণ রিপ্লে",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mgx-bn"
    }
  },
  "lastmod": "2021-09-08"
}

## একটি MGX ফাইল কি?

.mgx এক্সটেনশন সহ একটি ফাইল হল Age of Empires II: The Conquerors গেমের একটি রেকর্ড করা ফাইল যা Age of Empires II প্রোগ্রামের মধ্যে রিপ্লে করা যেতে পারে। এতে ব্যবহারকারীর দ্বারা চালানো প্রচারাভিযানের সম্পূর্ণ রেকর্ডিং রয়েছে। এটি এজ অফ এম্পায়ার II প্রোগ্রামের মধ্যে লোড করা এবং প্লে করা যেতে পারে। একবার রিপ্লে করা হলে, গেমটি সমস্ত ইভেন্ট এবং দৃশ্যকল্প দেখায় যা ব্যবহারকারী প্রচারণার জন্য পরিকল্পনা করেছিলেন এবং খেলেছিলেন।

## MGX ফাইল ফরম্যাট - আরও তথ্য

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### কাঠামোর সংজ্ঞা

GPX ফাইল ফরম্যাটের কাঠামোর সংজ্ঞাগুলি [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki) এর উপর ভিত্তি করে বলে মনে করা হয় যা স্ট্রাকচার্ড বাইনারি ডেটা পড়ার এবং লেখার একটি উপায় প্রদান করে। এটি প্রোগ্রামারকে বাইনারি ডেটার বিন্যাস নির্দিষ্ট করতে দেয় যা পরে বিনডাটা দ্বারা পড়তে এবং লিখতে পারে।

### MGX মেসেজিং

MGX মেসেজিং দুই ধরনের বার্তার উপর ভিত্তি করে।

 * GAMESTART - গেম স্টার্ট কমান্ড নির্দিষ্ট করে এবং আজ পর্যন্ত বৈধ করা হয়নি
 * চ্যাট - ইন-গেম চ্যাট বার্তা বর্ণনা করে। উভয়, খেলোয়াড় এবং গেম নিজেই (Gaia) ইন-গেম বার্তা নির্গত করতে পারে।

### গেমপ্লে অ্যাকশন

অনেকগুলি [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) আছে যেগুলি পুনরুদ্ধার করা হয়েছে এবং যার বিবরণ পাওয়া যায়৷

## তথ্যসূত্র

* [এজ অফ এম্পায়ারস 2: দ্য কন্কারার্স — সেভগেম ফাইল ফরম্যাট স্পেসিফিকেশন](https://github.com/stefan-kolb/aoc-mgx-format)


