{
  "date": "2019-10-11",
  "keywords": [
    "bz2 file",
    "bz2 file format",
    "what is a bz2 file",
    "file",
    "bz2 example",
    "bz2 file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "BZ2 - সংকুচিত ফাইল বিন্যাস",
  "description": "একটি BZ2 ফাইল এবং API যা BZ2 ফাইল তৈরি এবং খুলতে পারে তা জানতে শিখুন।",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz2-bn"
    }
  },
  "lastmod": "2020-09-05"
}

## একটি BZ2 ফাইল কি?

BZ2 হল কম্প্রেস করা ফাইল যা [BZIP2](http://www.bzip.org/) ওপেন সোর্স কম্প্রেশন পদ্ধতি ব্যবহার করে তৈরি করা হয়, বেশিরভাগ ইউনিক্স বা লিনাক্স সিস্টেমে। এটি একটি একক ফাইলের সংকোচনের জন্য ব্যবহৃত হয় এবং এটি একাধিক ফাইল সংরক্ষণের জন্য নয়। এটি একই প্ল্যাটফর্মে TAR ফাইল বিন্যাসের বিপরীতে যা একাধিক ফাইলকে একটি ফাইলে সংরক্ষণ করে কিন্তু কম্প্রেশন ছাড়াই। BZ2 হিসাবে সংকুচিত ফাইলগুলি [WinZip](https://www.winzip.com/win/en/) এর মতো অ্যাপ্লিকেশনগুলির সাথে ডিকম্প্রেস করা যেতে পারে৷ BZIP2 রান-লেংথ এনকোডিং (RLE) বা [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) কম্প্রেশন অ্যালগরিদম ব্যবহার করে উচ্চ মাত্রার কম্প্রেশন অর্জন করতে।

## BZ2 ফাইল ফরম্যাট

এই ফাইল ফরম্যাটের জন্য কোন আনুষ্ঠানিক স্পেসিফিকেশন উপলব্ধ নেই। যাইহোক, একটি অনানুষ্ঠানিক [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) দেখায় যে একটি .bz2 স্ট্রীমে একটি 4-বাইট হেডার থাকে যা শূন্য বা তার বেশি সংকুচিত ব্লক দ্বারা অনুসরণ করা হয়। এটি অবিলম্বে প্রসেস করা প্লেইন টেক্সট পুরো স্ট্রীমের জন্য একটি 32-বিট সিআরসি ধারণকারী একটি শেষ-অফ-স্ট্রিম মার্কার দ্বারা অনুসরণ করা হয়। সংকুচিত ব্লকগুলির মধ্যে কোনও প্যাডিং নেই এবং সমস্ত ব্লক বিট-সারিবদ্ধ।

## BZ2 ফাইল আনজিপ/এক্সট্র্যাক্ট করুন

আপনি WinZip-এর মতো সফ্টওয়্যার ব্যবহার করে Windows এবং Mac OS-এ একটি BZ2 ফাইল আনজিপ করতে পারেন। লিনাক্সে, টার্মিনালে নিম্নলিখিত কমান্ড।

```
bzip2 -d filename.bz2
```

## তথ্যসূত্র

* [BZIP2 ফর্ম্যাট স্পেসিফিকেশন](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


