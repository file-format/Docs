{
  "date" : "2019-10-11",
  "keywords" : [ "tbz file", "tbz file format", "what is a tbz file", "file", "tbz example", "tbz file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TBZ - Bzip কম্প্রেসড টার আর্কাইভ",
  "description":"TBZ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা TBZ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## একটি TBZ ফাইল কি?

.tbz এক্সটেনশন সহ একটি ফাইল হল একটি সংকুচিত সংরক্ষণাগার যা বিষয়বস্তু ফাইলের আকার হ্রাস করার জন্য BZIP কম্প্রেশন ব্যবহার করে। TBZ ফাইলগুলি আসলে UNIX [TAR](/compression/tar/) আর্কাইভ করা ফাইল যা BZIP এর সাথে সংকুচিত হয়। সাম্প্রতিকতম দ্বিতীয় স্তরের কম্প্রেশন হল [BZIP2](/compression/bz2/) যা BZIP প্রতিস্থাপন করেছে। TBZ ফাইল ফরম্যাট বড় ফাইল স্থানান্তর করার জন্য উপযুক্ত। TBZ ফাইলগুলি 7-Zip, PeaZip, এবং jZip-এর মতো সফ্টওয়্যার অ্যাপ্লিকেশন ব্যবহার করে খোলা/এক্সট্র্যাক্ট করা যেতে পারে। Linux এবং macOS ব্যবহারকারীরা একটি টার্মিনাল উইন্ডো থেকে BZIP2 কমান্ড দিয়ে একটি TBZ খুলতে পারে।

## TBZ ফাইল ফরম্যাট

TBZ ফাইলগুলি আসলে BZIP/[BZIP2](/compression/bz2/) কম্প্রেশন দিয়ে তৈরি করা সংকুচিত আর্কাইভ। এই ফাইল ফরম্যাটের জন্য কোন আনুষ্ঠানিক স্পেসিফিকেশন উপলব্ধ নেই। যাইহোক, একটি অনানুষ্ঠানিক [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) দেখায় যে একটি .bz2 স্ট্রিম একটি 4-বাইট হেডার নিয়ে গঠিত যা শূন্য বা তার বেশি সংকুচিত ব্লক দ্বারা অনুসরণ করা হয়।

## তথ্যসূত্র ##

* [BZIP2 ফর্ম্যাট স্পেসিফিকেশন](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


