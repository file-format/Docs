{
  "date": "2020-01-11",
  "keywords": [
    "x file",
    "x file format",
    "what is an x file",
    "file",
    "x example",
    "x file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "X - DirectX 2.0 ফাইল ফরম্যাট",
  "description": "DirectX X ফাইল ফরম্যাট এবং APIগুলি সম্পর্কে জানুন যা DirectX X ফাইলগুলি খুলতে এবং তৈরি করতে পারে৷",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-x-bn"
    }
  },
  "lastmod": "2020-01-11"
}

## একটি X ফাইল কি?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. এটি গেমগুলিতে 3D গ্রাফিক্স রেন্ডারিংয়ের জন্য ব্যবহার করা হয়েছিল এবং মেশ, টেক্সচার, অ্যানিমেশন এবং ব্যবহারকারী-সংজ্ঞায়িত বস্তুর কাঠামো নির্দিষ্ট করে। অটোডেস্ক FBX ফাইল ফরম্যাট আরও আধুনিক ফরম্যাট হিসেবে আরও ভাল পরিবেশন করায় 2014 সাল থেকে এটিকে অবমূল্যায়ন করা হয়েছে। X টেমপ্লেট-চালিত এবং কোনো ব্যবহারের জ্ঞান মুক্ত।

আপনি Microsoft DirectX এবং সাধারণ পাঠ্য সম্পাদক ব্যবহার করে DirectX X ফাইল খুলতে পারেন।

## এক্স ফাইল ফরম্যাট

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) এ API উপাদানগুলির জন্য রেফারেন্স তথ্য রয়েছে যা DirectX .x ফাইলগুলির সাথে কাজ করতে ব্যবহৃত হয়৷ বিন্যাস নিম্ন-স্তরের ডেটা আদিম প্রদান করে যা অন্যান্য অ্যাপ্লিকেশন দ্বারা ডেটা টেমপ্লেটের মাধ্যমে উচ্চ-স্তরের আদিম সংজ্ঞায়িত করতে ব্যবহৃত হয়। DirectX 6.0 ইন্টারফেস এবং পদ্ধতিগুলি চালু করেছে যা .x ফাইলগুলি থেকে পড়তে এবং লিখতে সক্ষম করে। DirectX 3.0 এই ফাইল ফরম্যাটের একটি বাইনারি সংস্করণ চালু করেছে।

DirectX 9 দ্বারা সংজ্ঞায়িত [X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)-এ বাইনারি এবং টেক্সট এনকোডিং-এর .x ফাইলগুলির জন্য রেফারেন্স তথ্য রয়েছে৷

### বাইনারি এনকোডিং

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) ডাইরেক্টএক্স এক্স ফর্ম্যাটটিকে টেক্সট ফর্ম্যাটের একটি টোকেনাইজড উপস্থাপনা হিসাবে সংজ্ঞায়িত করে৷ এই টোকেনগুলি ব্যাকরণগত কাঠামো দেওয়ার জন্য স্বতন্ত্র হতে পারে বা প্রয়োজনীয় ডেটা সরবরাহকারী রেকর্ড-বহনকারী টোকেন হতে পারে।

#### হেডার

বাইনারি হেডার নিম্নলিখিত সংজ্ঞা ব্যবহার করে পড়া এবং লেখা যেতে পারে।

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### টেক্সট এনকোডিং

DirectX .x ফাইলগুলি কীভাবে ফাইলটি ব্যবহার করা হয় তার উপর নির্ভর করে না এবং এটি কোনও অ্যাপ্লিকেশনের জন্য নির্দিষ্ট নয়। এই টেমপ্লেট-চালিত পদ্ধতিটি .x ফাইল বিন্যাসকে যেকোনো ক্লায়েন্ট অ্যাপ্লিকেশন দ্বারা ব্যবহার করার অনুমতি দেয়।


#### হেডার

পরিবর্তনশীল-দৈর্ঘ্যের শিরোনামটি বাধ্যতামূলক এবং ডেটা স্ট্রিমের শুরুতে হতে হবে। হেডারে নিম্নলিখিত ডেটা রয়েছে।

|প্রকার |সাব টাইপ |আকার
---|---|---|---|---|
|ম্যাজিক নম্বর (প্রয়োজনীয়)| | 4 বাইট |xof |
|সংস্করণ নম্বর (প্রয়োজনীয়) |মেজর নম্বর |2 বাইট |03 |মেজর সংস্করণ 3|
| | মাইনর নাম্বার | 2 বাইট | 02 | মাইনর সংস্করণ 2 |
|ফর্ম্যাটের ধরন (প্রয়োজনীয়)| |4 বাইট |txt  |টেক্সট ফাইল |
| | | |বিন | বাইনারি ফাইল|
| | | |tzip| MSZip কম্প্রেসড টেক্সট ফাইল|
| | | |bzip| MSZip সংকুচিত বাইনারি ফাইল|
|ফ্লোট সাইজ (প্রয়োজনীয়)| |4 বাইট| 0064| 64-বিট ফ্লোটস|
| | | |0032 |32-বিট ফ্লোটস|


## তথ্যসূত্র

 * [এক্স ফাইলের উত্তরাধিকার](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 ফাইল ফরম্যাট রেফারেন্স](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

