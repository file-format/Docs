{
  "date": "2019-12-09",
  "keywords": [
    "zl file",
    "zl file format",
    "what is a zl file",
    "file",
    "zl example",
    "zl file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ZL - ZLIP সংকুচিত ফাইল বিন্যাস",
  "description": "ZL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি ZL ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zl-bn"
    }
  },
  "lastmod": "2021-04-14"
}

## একটি ZL ফাইল কি?

.zl এক্সটেনশন সহ একটি ফাইল হল একটি ZLIP সংকুচিত ফাইল বিন্যাস যা ফাইল কম্প্রেস করার জন্য DEFLATE কম্প্রেশন অ্যালগরিদমের একটি বৈকল্পিক ব্যবহার করে। এটি সিপিইউ টাইপ, অপারেটিং সিস্টেম, ফাইল সিস্টেম এবং অক্ষর সেট থেকে স্বাধীন, এবং তাই তথ্য বিনিময়ের জন্য ব্যবহার করা যেতে পারে। ZLIP কম্প্রেশনের প্রযুক্তিগত স্পেসিফিকেশন [IETF site](https://tools.ietf.org/html/rfc1950) এ উপলব্ধ এবং বিকাশকারীর দৃষ্টিকোণ থেকে উল্লেখ করা যেতে পারে।

## ZL ফাইল ফরম্যাট

একটি zlib স্ট্রিম নিম্নলিখিত গঠন আছে:

 * `CMF (কম্প্রেশন মেথড এবং ফ্ল্যাগস)` - এই বাইটটি কম্প্রেশন পদ্ধতির উপর নির্ভর করে একটি 4-বিট কম্প্রেশন পদ্ধতি এবং একটি 4-বিট তথ্য ক্ষেত্রে বিভক্ত।
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * `CM (কম্প্রেশন পদ্ধতি)` - এটি ফাইলে ব্যবহৃত কম্প্রেশন পদ্ধতি সনাক্ত করে। এর মান এবং সংশ্লিষ্ট কম্প্রেশন পদ্ধতি নিম্নরূপ।

| CM মান| কম্প্রেশন|
|---|---|
|CM = 8|32K| পর্যন্ত একটি উইন্ডোর আকার সহ ডিফ্লেট করুন৷
|CM = 15|সংরক্ষিত|

 * `CINFO (কম্প্রেশন ইনফো)` - CM = 8 এর জন্য, CINFO হল LZ77 উইন্ডো সাইজের বেস-2 লগারিদম, মাইনাস আট (CINFO=7 একটি 32K উইন্ডো সাইজ নির্দেশ করে)।

 * `FLG (FLaGs)` - এই পতাকা বাইটটি নিম্নরূপ বিভক্ত:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## তথ্যসূত্র ##

* [Zlib ফাইল ফরম্যাট স্পেসিফিকেশন](https://tools.ietf.org/html/rfc1950)


