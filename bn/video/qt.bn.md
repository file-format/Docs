{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QT ফাইল ফরম্যাট - দ্রুত মুভি ফাইল",
  "keywords": [
    "QT",
    "QuickTime video",
    "qt format",
    "how to play qt files",
    "Quick Movie File",
    "QTFF",
    "video",
    "Apple"
  ],
  "description": "QT ফাইল বিন্যাস এবং API সম্পর্কে জানুন যেগুলি QT ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-qt-bn"
    }
  },
  "lastmod": "2021-02-16"
}

## একটি QT ফাইল কি?

একটি .qt এক্সটেনশন সহ একটি ফাইল হল একটি মাল্টিমিডিয়া কন্টেইনার ফাইল যা কুইকটাইম ফ্রেমওয়ার্ক মাল্টিমিডিয়া ফাইল বিষয়বস্তু সংরক্ষণ করতে ব্যবহার করে। অ্যাপল ইনকর্পোরেটেড দ্বারা ডেভেলপ করা হয়েছে। কুইকটাইম ফাইল ফরম্যাট (QTFF) হল একটি মাল্টিমিডিয়া কন্টেইনার ফাইল যাতে পরে প্লেব্যাকের জন্য অডিও, ভিডিও বা টেক্সট থাকে। এটি ডিভাইস, অ্যাপ্লিকেশন এবং অপারেটিং সিস্টেমের মধ্যে ডিজিটাল মিডিয়া বিনিময়ের জন্য পছন্দের ফর্ম্যাট। QT ফাইলগুলিও [MOV](/video/mov/) ফর্ম্যাটে সংরক্ষিত হয় যা Apple Inc দ্বারাও তৈরি করা হয়েছিল৷ কিছু অ্যাপ্লিকেশন যেগুলি QT ফাইলগুলি খুলতে পারে তার মধ্যে রয়েছে Apple QuickTime প্লেয়ার, VLC মিডিয়া প্লেয়ার, এবং K-Lite কোডেক প্যাক সহ মিডিয়া প্লেয়ার ক্লাসিক৷

## QT ফাইল ফরম্যাট

QTFF অবজেক্ট-ওরিয়েন্টেড যা পার্সিং এবং প্রসারণের সহজতার জন্য বস্তুর একটি নমনীয় সংগ্রহ প্রকাশ করে। একটি QT ফাইলের প্রতিটি ট্র্যাকে একটি ডিজিটাল-এনকোডেড মিডিয়া স্ট্রীম বা অন্য ফাইলে অবস্থিত মিডিয়া স্ট্রীমের একটি ডেটা রেফারেন্স রয়েছে। পরমাণু নামক বস্তুর সমন্বয়ে শ্রেণীবদ্ধ তথ্য কাঠামো ট্র্যাক পাত্র হিসাবে কাজ করে। [QT file format](https://developer.apple.com/documentation/quicktime-file-format)-এর জন্য ফাইল ফর্ম্যাট স্পেসিফিকেশন ডেভেলপারের রেফারেন্সের জন্য Apple Inc দ্বারা আনুষ্ঠানিকভাবে উপলব্ধ৷

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### পরমাণু

এটম হল কুইকটাইম ফাইলের মৌলিক একক। যেকোনো পরমাণুর অন্য কোনো ক্ষেত্রের আগে দুটি প্রধান ক্ষেত্র রয়েছে: আকার এবং প্রকার ক্ষেত্র। আকার ক্ষেত্রটি পরমাণুর আকার দেখায় যখন টাইপ ক্ষেত্রটি পরমাণুতে সংরক্ষিত ডেটার ধরণ নির্দেশ করে। প্রকৃতির দ্বারা, পরমাণুগুলি শ্রেণিবদ্ধ যার মানে হল যে একটি পরমাণুতে অন্য পরমাণু থাকতে পারে যা এখনও অন্যকে ধারণ করতে পারে। একটি নমুনা পরমাণুর বিন্যাস নিম্নলিখিত ছবিতে দেখানো হয়েছে।

প্রতিটি পরমাণুর দুটি অংশ, শিরোনাম এবং ডেটা থাকে। হেডারে আকার এবং টাইপ ক্ষেত্র রয়েছে এবং ডেটা অংশে প্রকৃত ডেটা রয়েছে। আরও, প্রতিটি ক্ষেত্র নীচে ব্যাখ্যা করা হয়েছে:

#### পরমাণুর আকার

পরমাণুর হেডার এবং বিষয়বস্তু একটি 32-বিট পূর্ণসংখ্যা দ্বারা নির্দেশিত হয় যা পরমাণুর আকার হিসাবে পরিচিত। সাইজ ফিল্ডে বাইটে পরমাণুর আকার থাকে, একটি 32-বিট স্বাক্ষরবিহীন পূর্ণসংখ্যাতে প্রকাশ করা হয়।

#### পরমাণুর প্রকার

পরমাণুর ধরনটি একটি 32-বিট পূর্ণসংখ্যা দ্বারাও দেখানো হয়, যেটিকে বেশিরভাগই চার-অক্ষরের ক্ষেত্র হিসাবে ধরা হয় নিমোনিক মান সহ, যেমন একটি মুভি পরমাণুর জন্য 'moov' (0x6D6F6F76), বা 'ট্রাক' (0x7472616B) একটি ট্র্যাক পরমাণু। একবার পরমাণুর ধরন জানা গেলে, এটি তার ডেটা ব্যাখ্যা করার অনুমতি দেয়।

![alt text](../QT_Sample_Atom.png "QT File Format")

## ফাইলের গঠন ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV সাব-টাইপ দ্বারা সংজ্ঞায়িত যা অবশ্যই qt হতে হবে। MOV ফাইল রচনা করার জন্য, অজানা প্রকার সনাক্ত না হওয়া পর্যন্ত পুনরাবৃত্ত অংশ প্রয়োজন।

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. অফসেট 32-এ (হেক্স: 20) দ্বিতীয় খণ্ডটি অবস্থিত, যার আকার 8 এবং টাইপ করুন **mdat** (হেক্স: 6D 64 61 74)।

পরবর্তী খণ্ডটি অফসেট 32+8#40 (হেক্স: 28) এ অবস্থিত এবং এর আকার 3,263,028 (হেক্স: 00 31 CA 34) এবং অফসেট 44 (হেক্স) এ **mdat** (হেক্স: 6D 64 61 74) টাইপ করুন : 2C)। পরবর্তী খণ্ডটি অফসেট 40 + 3,263,028#3,263,068 (হেক্স: 00 31 CA 5C) এ অবস্থিত এবং এর আকার 21,189 (হেক্স: 00 00 52 C5) এবং টাইপ করুন **moov** (হেক্স: 6D 6F 6F 6F 6F সেট) 1,836,019,574 (হেক্স: 00 31 CA 60)। এটি শেষ অংশ, তাই মোট ফাইলের আকার হল 3,263,068+21,189#3,284,257 বাইট।

## তথ্যসূত্র ##

* [QT ফাইল ফরম্যাট - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [কুইকটাইম ফাইল ফরম্যাট - উইকিপিডিয়া](https://en.wikipedia.org/wiki/QuickTime_File_Format)
