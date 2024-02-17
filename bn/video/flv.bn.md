---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LFLV ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা FLV ফাইল তৈরি এবং খুলতে পারেs.
title: Fএলভি ফাইল ফর্মat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## একটি FLV ফাইল কি? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. FLV এর সীমাবদ্ধতার কারণে 2007 সালে Adobe সিস্টেম F4V তৈরি করেছিল।

### এনকোডিং ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. On2 TrueMotion VP6 ভিডিও বিটস্ট্রিমের জন্য ফ্ল্যাশ প্লেয়ার সমর্থনের সংস্করণ 8। এটি Flash Player 8 এবং উচ্চতর জন্য প্রস্তাবিত কম্প্রেশন বিন্যাস। FLV MP3, Nellymoser Asao Codec, এবং open-source Speex codec-এ অডিও সমর্থন করে। এটি আনকম্প্রেসড অডিও বা ADPCM ফরম্যাট অডিও সমর্থন করে। AAC (HE-AAC/AAC SBR, AAC প্রধান প্রোফাইল, এবং AAC-LC) ফ্ল্যাশ প্লেয়ার 9 এর সাম্প্রতিক সংস্করণ দ্বারা সমর্থিত।

## গঠন ##

FLV ফাইলে হেডার এবং প্যাকেট থাকে। একটি FLV ফাইল হেডার দিয়ে শুরু হয়। হেডারে নিম্নলিখিত ক্ষেত্র রয়েছে।

- **স্বাক্ষর**: এর মান হল FLV
- **Version**: Its default value is 1. শুধুমাত্র 0x01 বৈধ।
- **পতাকা**: অডিওর জন্য 0x04 এবং ভিডিওর জন্য 0x01 ব্যবহার করা হয় তাই অডিও এবং ভিডিও উভয়ের জন্য 0x05 ব্যবহার করা হয়।
- **Header Size**: The default value is 9. এটি একটি নতুন প্রসারিত হেডার এড়িয়ে যাওয়ার জন্য ব্যবহৃত হয়।

হেডারের পর প্যাকেট আসে। FLV ফাইলটিকে FLV ট্যাগ নামে একাধিক প্যাকেটে বিভক্ত করা হয়েছে যার 15-বাইট হেডার রয়েছে। প্যাকেটগুলিতে অডিও, ভিডিও, স্ক্রিপ্ট, এনক্রিপশন তথ্য এবং পেলোডের জন্য মেটাডেটা রয়েছে। FLV প্যাকেটগুলিতে নিম্নলিখিত ক্ষেত্রগুলি রয়েছে৷

- **সংরক্ষিত**: এটি FMS এর জন্য সংরক্ষিত এবং 0 হওয়া উচিত।
- **ফিল্টার**: প্যাকেটগুলি ফিল্টার করা হয়েছে কিনা তা নির্দেশ করে।
  - "**0**: কোন প্রিপ্রসেসিং এর প্রয়োজন নেই। এটি এনক্রিপ্ট করা ফাইলগুলির জন্য ব্যবহৃত হয়।"
  - "**1**: প্রি-প্রসেসিং প্রয়োজন। এটি এনক্রিপ্ট করা ফাইলের জন্য ব্যবহৃত হয়"
- **প্যাকেটের ধরন**: এটি প্যাকেটের বিষয়বস্তুর ধরণকে সংজ্ঞায়িত করে।
  - "**8**: অডিও"
  - "**9**: ভিডিও"
  - "**18**: স্ক্রিপ্ট ডেটা"
- **ডেটা সাইজ**: এটি বার্তার দৈর্ঘ্য নির্দেশ করে।
- **টাইমস্ট্যাম্প নিম্ন**: এটি মিলিসেকেন্ডে টাইমস্ট্যাম্প সংরক্ষণ করে যেখানে ট্যাগ ডেটা প্রযোজ্য হয়। এটি প্রথম প্যাকেটের জন্য NULL এ সেট করা হয়েছে।
- **টাইমস্ট্যাম্প আপার**: একটি uint32_be মান তৈরি করতে এক্সটেনশন।
- **স্ট্রিম আইডি**: এটি প্রথম স্ট্রিমের জন্য NULL এ সেট করা হয়েছে।
- **পেলোড ডেটা**: এটি প্যাকেটের প্রকারের উপর ভিত্তি করে ডেটা।

## তথ্যসূত্র ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

