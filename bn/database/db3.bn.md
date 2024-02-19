{
  "date": "2019-12-12",
  "keywords": [
    "DB3",
    "DB3 ফাইল ফরম্যাট",
    "DB3 File",
    "SQLite",
    "extension",
    "file",
    "file format",
    "Database File Type",
    "Database File Format",
    "Database Files"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "DB3 ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা DB3 ফাইল তৈরি এবং খুলতে পারে।",
  "title": "DB3 ফাইল ফরম্যাট",
  "linktitle": "DB3",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db3-bn"
    }
  },
  "lastmod": "2020-11-09"
}

## একটি DB3 ফাইল কি?
DB3 ফাইলটি SQLite সফ্টওয়্যার দ্বারা তৈরি একটি ডাটাবেস ফাইল যা একটি হালকা, স্বয়ংসম্পূর্ণ ডাটাবেস প্রোগ্রাম যা প্লেইন ফাইল ব্যবহার করে ডেটাবেস তৈরি করে; ডাটাবেস অ্যানাটমি পাশাপাশি ডেটা রেকর্ড রয়েছে; সাধারণত SQL ব্যবহার করে স্ট্রাকচার্ড ডেটা পুনরুদ্ধার বা সংরক্ষণের জন্য ব্যবহৃত হয়। এই ফাইলগুলি স্মার্ট ডিভাইসগুলিতে ব্যবহার করা যেতে পারে বা যেখানে রেকর্ড রাখা বা অন্যান্য ডেটা পরিচালনার প্রয়োজন হয় তবে কম জায়গার পরিবেশে।


## DB3 ফাইল ফরম্যাট
DB3 ফাইল ফরম্যাটটি RDBMS (রিলেশনাল ডেটাবেস ম্যানেজমেন্ট সিস্টেম) SQLite এর সাথে যুক্ত, এটি এমবেডেড ডাটাবেসের জন্য একটি জনপ্রিয় পছন্দ। SQLite_3 এর স্পেসিফিকেশনে সংজ্ঞায়িত কোনো নির্দিষ্ট ফাইল এক্সটেনশন নেই, এটি [.dbf](/database/dbf/) এবং [.sqlite](/database/sqlite/) সহ এক্সটেনশন ব্যবহার করতে পারে।

### ডাটাবেস নির্দিষ্টকরণ
Commonly SQLite, version 3 related db file format can be considered as the DB3 file format used as the publicly documented native format for the SQLite database engine since June 2004. DB3 ফাইল ফরম্যাট হল একটি ক্রস-প্ল্যাটফর্ম, বড়-এন্ডিয়ান এবং লিটল-এন্ডিয়ান আর্কিটেকচার বা 32-বিট এবং 64-বিট সিস্টেমের মধ্যে স্থানান্তরযোগ্য। এই বৈশিষ্ট্যগুলি DB3 একটি অ্যাপ্লিকেশন ফাইল বিন্যাস হিসাবে একটি জনপ্রিয় পছন্দ করে তোলে। প্রধান SQLite_3 ডাটাবেস (DB3) ফাইল এক বা একাধিক পৃষ্ঠা নিয়ে গঠিত। সমস্ত পৃষ্ঠার সমস্ত আকার একই ডাটাবেসে সমান। বাইটে পৃষ্ঠার আকার হল 512 এবং 65536 এর মধ্যে দুটি শক্তি।



## তথ্যসূত্র ##

* [SQLite - উইকিপিডিয়া](https://en.wikipedia.org/wiki/SQLite)

* [SQLite, সংস্করণ 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)


