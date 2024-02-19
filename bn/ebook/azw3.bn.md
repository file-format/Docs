{
  "date": "2019-12-12",
  "keywords": [
    "KF8",
    "extension",
    "file",
    "format",
    "eBook",
    "Kindle File Format",
    "AZW3 File Structure"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "AZW3 ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা AZW3 ফাইল তৈরি এবং খুলতে পারে।",
  "title": "একটি AZW3 ফাইল কি?",
  "linktitle": "AZW3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-azw3-bn"
    }
  },
  "lastmod": "2021-06-04"
}

## একটি AZW3 ফাইল কি?

AZW3, Kindle Format 8 (**KF8**) নামেও পরিচিত, হল অ্যামাজন কিন্ডল ডিভাইসের জন্য তৈরি করা [AZW](/ebook/azw/) ইবুক ডিজিটাল ফাইল ফরম্যাটের পরিবর্তিত সংস্করণ। ফরম্যাটটি পুরানো AZW ফাইলগুলির একটি বর্ধিতকরণ এবং এটি শুধুমাত্র পূর্বপুরুষ ফাইল ফরম্যাটের যেমন [MOBI](/ebook/mobi/) এবং AZW-এর জন্য ব্যাকওয়ার্ড সামঞ্জস্যের সাথে Kindle Fire ডিভাইসে ব্যবহার করা হয়৷ আমাজন KF8 এর পরে KFX (KF সংস্করণ 10) ফর্ম্যাট চালু করেছে যা সর্বশেষ কিন্ডল ডিভাইসে ব্যবহৃত হয়। AZW3 ফাইলে ইন্টারনেট মিডিয়া টাইপ অ্যাপ্লিকেশন/vnd.amazon.mobi8-ebook আছে। AZW3 ফাইলগুলিকে অন্যান্য ফাইল ফরম্যাটে রূপান্তর করা যেতে পারে যেমন [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/), এবং [RTF](/word-processing/rtf/)৷

## AZ3/KF8 ফাইল ফরম্যাট ##

KF8 ফাইলগুলি বাইনারি প্রকৃতির এবং একটি MOBI ফাইল ফরম্যাটের গঠন PDB ফাইল হিসাবে ধরে রাখে। আগেই উল্লেখ করা হয়েছে, একটি KF8 ফাইলে MOBI এবং পরবর্তীতে EPUB-এর একটি নতুন KF8 সংস্করণ উভয়ই থাকতে পারে। বিন্যাসের অভ্যন্তরীণ বিবরণ [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) দ্বারা ডিকোড করা হয়েছে, এটি একটি পাইথন স্ক্রিপ্ট যা চূড়ান্ত সংকলিত ডাটাবেসকে পার্স করে এবং এটি থেকে MOBI বা AZW সোর্স ফাইলগুলি বের করে। AZW3 (KF8) ফাইলগুলি EPUB3 সংস্করণকে লক্ষ্য করে EPUB-এর জন্যও পশ্চাদগামী সামঞ্জস্যপূর্ণ। KF8 EPUB ফাইল কম্পাইল করে এবং PDB ফাইল ফরম্যাটের উপর ভিত্তি করে একটি বাইনারি স্ট্রাকচার তৈরি করে।

## তথ্যসূত্র ##

* [KF8 - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Kindle_File_Format)

* [কিন্ডল আনপ্যাক](https://github.com/kevinhendricks/KindleUnpack)


