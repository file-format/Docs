---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lএসইসি ফাইল ফরম্যাট এবং এপিআই সম্পর্কে আয় করুন যা এসইসি ফাইল তৈরি এবং খুলতে পারেs.
title: SEC ফাইল ফরম্যাট - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## একটি SEC ফাইল কি?

একটি এসইসি ফাইল হল একটি ভিডিও ফাইল যা স্যামসাং ডিভিআর নজরদারি সিস্টেমের সাথে তৈরি করা হয়। ভিডিও নজরদারি ক্যামেরা থেকে ধারণ করা হয় এবং SEC ফরম্যাটে ডিস্কে সংরক্ষণ করা হয়। রেকর্ড করা SEC ভিডিও স্যামসাং এর ভিডিও সফ্টওয়্যার দিয়ে প্লে করা যেতে পারে যা একাধিক ক্যামেরা থেকে ভিডিও ফিড পরিচালনা করতে পারে।

## এসইসি ফাইল ফরম্যাট - আরও তথ্য

মালিকানাধীন ফাইল বিন্যাস ব্যবহার করে SEC ফাইলগুলিতে h264/AVC স্ট্রীম থাকে। একটি SEC ফাইলের হেডার SRD-1670D এর মডেল নম্বর দিয়ে শুরু হয়। তারিখ এবং সময় তথ্য ফাইলের শেষে রাখা হয়.

### SEC ফাইলকে AVI-তে রূপান্তর করুন

SEC ফাইলটিকে FFmpeg ব্যবহার করে স্ট্যান্ডার্ড [AVI](/video/avi/) ফাইল ফর্ম্যাটে রূপান্তর করা যেতে পারে।

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## তথ্যসূত্র ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

