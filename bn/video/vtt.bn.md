---
date: 2022-01-06
keywords: vtt, .vtt, vtt file format, .vtt file format, .vtt extension, vtt extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: L.vtt ফাইল এবং এপিআই সম্পর্কে আয় করুন যা VTT ফাইল তৈরি এবং খুলতে পারেs.
title: VTT ফাইল ফরম্যাট - ওয়েব ভিডিও টেক্সট ট্র্যাক File
linktitle: VTT
menu:
  docs:
    identifier: "video-vt-bnt"
    parent: "video"
lastmod: 2022-01-06
---

## একটি VTT ফাইল কি?

A VTT file is a text file that contains information for displaying timed text tracks (such as subtitles or captions) using the Web Video Text Tracks (WebVTT) format. The timed text tracks includes information such as subtitles or captions. The purpose of VTT file is to add text overlays to a <video>. The format is somewhat similar to the SRT files. WebVTT based text files are encoded using UTF-8. A VTT file contains information such as subtitles, descriptions, captions, descriptions, chapters, and metadata. Being plain text files, VTT files can be opened using text editors such as Microsoft Notepad, Apple TextEdit, and Notepad++.

## VTT ফাইল ফরম্যাট - আরও তথ্য

VTT ফাইলগুলি ক্রমিক পাঠ্য ট্র্যাকের তথ্য সংরক্ষণের জন্য WebVTT ফাইল বিন্যাস ব্যবহার করে। প্রতিটি টাইমড টেক্সট ট্র্যাক একটি একক লাইন বা একাধিক লাইন নিয়ে গঠিত, যা নিম্নলিখিত উদাহরণে দেখানো হিসাবে একটি `কিউ` নামেও পরিচিত।

### VTT ফাইলের উদাহরণ

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT ফাইলের কাঠামো

নিম্নলিখিত একটি VTT ফাইলের গঠন প্রয়োজনীয়তা আছে.

 * একটি ঐচ্ছিক বাইট অর্ডার মার্ক (BOM)।
 * স্ট্রিং WEBVTT।
 * WEBVTT এর ডানদিকে একটি ঐচ্ছিক পাঠ্য শিরোনাম।
 * একটি ফাঁকা লাইন, যা পরপর দুটি নতুন লাইনের সমতুল্য।
 * শূন্য বা তার বেশি ইঙ্গিত বা মন্তব্য।
 * শূন্য বা তার বেশি ফাঁকা লাইন।

## তথ্যসূত্র

 * [VTT - W3 স্কুল](https://www.w3.org/TR/webvtt1/)
 * [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) 

