{
  "date" : "2021-06-16",
  "keywords" : [ "LZH", "Compressed", "File", "Extension", "File Format", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" : "LZH ফাইল ফরম্যাট",
  "description":"LZH ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি LZH ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## একটি LZH ফাইল কি? ##

A file with .lzh and .lha extension usually relates to archive compression file format. This file format is the same as other file compression formats like [ZIP](/compression/zip/), [RAR](/compression/rar/), etc. The main purpose of these file formats is to reduce the size of the format for easily sending as well as to keep them together in compressed form. AS compare to other western companies LZH files are very popular in Japan and usually used for compressing video game data. The LZH add-on for Windows 7 is built into the Japanese version of Windows 7. Microsoft প্রথম Windows XP এর জাপানি সংস্করণের জন্য Microsoft Compressed (LZH) ফোল্ডার অ্যাড-অন প্রকাশ করেছে। এই ফাইল বিন্যাসটি লেম্পেল-জিভ এবং হারুয়াসু অ্যালগরিদম দ্বারা ব্যবহৃত কম্প্রেশন বিধান এবং বৈশিষ্ট্যগুলির সাথে প্রয়োগ করা হয়েছে

## LZH স্পেসিফিকেশন ##

একটি LZH সংরক্ষণাগারের কম্প্রেশন পদ্ধতি একটি পাঁচ-বাইট পাঠ্য স্ট্রিং হিসাবে দেখানো হয়, যেমন -lz1-। এগুলি সংকুচিত ফাইলের তৃতীয় থেকে সপ্তম বাইট।

| স্পেসিফিকেশন | বর্ণনা |
---|---|
|এক্সটেনশন | .lzh, .lha|
|মিডিয়া টাইপ| অ্যাপ্লিকেশন/x-lzh-সংকুচিত|
|কোড টাইপ করুন| LHA_ (LHA-স্পেস)|
|ইউটিআই| public.archive.lha|
|বিকশিত | হারুয়াসু ইয়োশিজাকি (য়োশি)|
|প্রকার| কম্প্রেশন|
|থেকে বর্ধিত| LArc|

## একটি LZH ফাইল খুলতে সমস্যা ##

নিম্নোক্ত কয়েকটি সমস্যা যা LZH ফাইল ফরম্যাটের দুর্বল কাজের কারণ হতে পারে:
  
* ফাইলটি দূষিত হতে পারে। এই সমস্যাটি সমাধান করতে, ফাইলটি আবার ডাউনলোড করুন বা প্রেরককে ফাইলটি আবার পাঠাতে বলুন
* দ্বিতীয় কারণ হল সংক্রমিত ফাইল এই ক্ষেত্রে ফাইলটি সঠিকভাবে স্ক্যান করুন
* LZH ফাইলের অনুপযুক্ত লিঙ্ক
  *	 Removal of the description of the LZH 
* পর্যাপ্ত হার্ডওয়্যার সংস্থান নেই
* সরঞ্জামের পুরানো ড্রাইভার

## তথ্যসূত্র ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
