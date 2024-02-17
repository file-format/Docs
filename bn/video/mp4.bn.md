---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LMP4 ফাইল ফরম্যাট এবং APIs সম্পর্কে উপার্জন করুন যা MP4 ফাইল তৈরি এবং খুলতে পারেs.
title: MP4 ফাইল ফর্মat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## একটি MP4 ফাইল কি? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## সংক্ষিপ্ত ইতিহাস ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. MP4 এর প্রথম সংস্করণ (ISO/IEC 14496-1:2001) ছিল MPEG-4 অংশ 1: 1999 সালে প্রকাশিত সিস্টেম স্পেসিফিকেশনের একটি সংশোধন। MP4 ফাইল ফরম্যাটটি ISO/IEC 14496-12 তে সাধারণীকরণ করা হয়েছিল। :2004 যা সময়-ভিত্তিক মিডিয়া ফাইলগুলির জন্য সাধারণ কাঠামো সংজ্ঞায়িত করে। ফলস্বরূপ, এটি অন্যান্য ফাইল ফরম্যাটের জন্য একটি ভিত্তি হিসাবে ব্যবহৃত হয়।

## MP4 ফাইলের গঠন ##

MP4 হল একটি এক্সটেনসিবল কন্টেইনার ফাইল, যার অর্থ এটি একটি কঠোর কাঠামো সংজ্ঞায়িত করে না এবং প্রতিটি মিডিয়া প্রকারের জন্য কাস্টম কাঠামো এবং শ্রেণিবিন্যাসকে অনুমতি দেয়। MP4 ফাইলের ডেটা দুটি বিভাগে বিভক্ত, প্রথমটিতে মিডিয়া-সম্পর্কিত ডেটা এবং দ্বিতীয়টিতে মেটাডেটা রয়েছে৷ মিডিয়া ডেটাতে অডিও বা ভিডিও থাকে এবং মেটাডেটা র্যান্ডম অ্যাক্সেস, টাইমস্ট্যাম্প ইত্যাদির জন্য পতাকা নির্দেশ করে।
MP4 এর কাঠামোগুলিকে সাধারণত পরমাণু বা বাক্স হিসাবে উল্লেখ করা হয়। একটি পরমাণুর সর্বনিম্ন আকার 8 বাইট (প্রথম 4 বাইট আকার নির্দিষ্ট করে এবং পরবর্তী 4 বাইট প্রকার নির্দিষ্ট করে)। এমপি ফাইলগুলিতে থাকা রুট স্তরের পরমাণুর একটি তালিকা এখানে রয়েছে:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: প্রগতিশীল ভিডিও লোডিং/ডাউনলোডিং তথ্য রয়েছে।
- **moov**: সমস্ত মুভি মেটাডেটার জন্য ধারক।
- **moof**: ভিডিও টুকরা সহ ধারক।
- **mfra**: ভিডিও খণ্ডে র্যান্ডম অ্যাক্সেস সহ ধারক
- **mdat**: মিডিয়ার জন্য ডেটা ধারক।
- **stts**: নমুনা-টু-টাইম টেবিল।
- **stsc**: নমুনা থেকে খণ্ড টেবিল।
- **stsz**: নমুনার আকার (ফ্রেমিং)
- **মেটা**: মেটাডেটা তথ্য সহ ধারক।

এখানে MP4 এ ব্যবহৃত দ্বিতীয়-স্তরের পরমাণুর একটি তালিকা রয়েছে:

- **mvhd**: ভিডিওর সম্পূর্ণ বিবরণ সহ ভিডিও শিরোনামের তথ্য রয়েছে৷
- **ট্র্যাক**: পৃথক ট্র্যাক সহ ধারক।
- **udta**: ব্যবহারকারী এবং ট্র্যাক তথ্য সহ ধারক।
- **iods**: MP4 ফাইল বর্ণনাকারী

## তথ্যসূত্র ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

