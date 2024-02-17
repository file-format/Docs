---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LMXL ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা MXL ফাইল তৈরি এবং খুলতে পারেs.
title: MXL ফাইল ফরম্যাট - সংকুচিত MusicXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## একটি MXL ফাইল কি?

একটি MXL ফাইল হল মিউজিকএক্সএমএল ফাইল ফরম্যাটের সংকুচিত ফর্ম যা ডিজিটাল শিট মিউজিক বিনিময়ের জন্য একটি ওপেন স্ট্যান্ডার্ড ফরম্যাট। প্লেইন টেক্সট মিউজিকএক্সএমএল ফাইল আকারে বড় এবং শীট ডিস্ট্রিবিউশন ফরম্যাটের মতো ফাইলের ব্যবহার বড় ফাইলের আকারের সাথে প্রভাবিত হয়েছিল। এই সমস্যাটি [MusicXML](https://www.musicxml.com/) 2.0 দিয়ে MXL ফাইল ফরম্যাট প্রবর্তনের মাধ্যমে চিকিত্সা করা হয়েছিল যা ফাইলগুলিকে যথেষ্ট পরিমাণে সংকুচিত করে যা আসল MIDI ফাইলগুলির মতো ফাইলের আকার কমাতে পারে৷ MXL ফাইলগুলির জন্য প্রস্তাবিত মিডিয়া প্রকার হল application/vnd.recordare.musicxml৷

## MXL ফাইল ফরম্যাট

MXL ফাইল .mxl ফাইল এক্সটেনশন সহ [ZIP](/compression/zip/) সংকুচিত [XML](/web/xml/) ফাইল হিসাবে সংরক্ষণ করা হয়। MXL ফাইলগুলিকে [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)-এ উল্লেখ করা ডিফ্লেট অ্যালগরিদম দিয়ে সংকুচিত করা হয়।

### MXL ফাইল স্ট্রাকচার

প্রতিটি MXL ফাইলের একটি ZIP-ভিত্তিক XML ফর্ম্যাট থাকে যার একটি META-INF/container.xml ফাইল থাকতে হবে যা ফাইলের MusicXML সংস্করণের শুরুর বিন্দু বর্ণনা করে৷ MXL ফাইল ফরম্যাটের জন্য সংজ্ঞায়িত কোন সংশ্লিষ্ট .xsd ফাইল নেই।

একটি সাধারণ container.xml ফাইলের বিষয়বস্তু অনুসরণ করা হয়। এই উদাহরণটি MakeMusic ওয়েব সাইটে উপলব্ধ Dichterliebe01.mxl ফাইল থেকে নেওয়া হয়েছে৷

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
এই উদাহরণে,<container> উপাদান হল নথির উপাদান। দ্য<rootfiles> উপাদান এক বা একাধিক ধারণ করতে পারে<rootfile> উপাদান, প্রথম সঙ্গে<rootfile> মিউজিকএক্সএমএল রুট বর্ণনাকারী উপাদান। একটি মিউজিকএক্সএমএল ফাইল একটি হিসাবে ব্যবহৃত হয়<rootfile> থাকতে পারে<score-partwise> ,<score-timewise> , বা<opus> এর নথি উপাদান হিসাবে।

## তথ্যসূত্র

* [সংকুচিত MXL ফাইল](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


