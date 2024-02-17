---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - সফ্টওয়্যার প্রকাশক সার্টিফিকেট File
linktitle: SPC
description: Lএকটি SPC ফাইল ফরম্যাট এবং APIs যা SPC ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে উপার্জন করুনs.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## একটি SPC ফাইল কি?

.spc এক্সটেনশন সহ একটি ফাইল হল একটি ডিজিটাল নিরাপত্তা শংসাপত্র ফাইল যা PKCS # 7 ফর্ম্যাটে তৈরি করা হয়েছে। বেশ কিছু অ্যাপ্লিকেশন, তথ্যের নিরাপদ বিনিময়ের জন্য এই সার্টিফিকেট ফাইলগুলি তৈরি করুন। এই ধরনের কয়েকটি অ্যাপ্লিকেশনের মধ্যে OpenSSL এবং Signcode.exe অ্যাপ্লিকেশন রয়েছে যা Microsoft এর .NET ফ্রেমওয়ার্কের সাথে অন্তর্ভুক্ত। অন্যান্য সার্টিফিকেট ফাইলের মতো যেমন [.cer](/web/cer/), [.p7c](/web/p7c/), এবং [.ssp](/web/ssp/), SPC ফাইলগুলিতে সর্বজনীন কী তথ্য থাকে যা একটি ব্যক্তিগত কী দিয়ে এনক্রিপ্ট করা হয়। এই সর্বজনীন কী ব্যবহারকারীদের সাথে সর্বজনীনভাবে ভাগ করা যেতে পারে যখন ব্যক্তিগত কীটি গোপন রাখা হয়।

## SPC ফাইল ফরম্যাট - আরও তথ্য

এসপিসি ফাইলগুলি বাইনারি ফাইল হিসাবে ডিস্কে সংরক্ষিত হয় যা যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে তবে মানুষের পাঠযোগ্য নয়। এগুলি PKCS # 7 এর সর্বশেষ সংস্করণের উপর ভিত্তি করে যা উপলব্ধ [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315)৷

## তথ্যসূত্র

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [এসএসপি রেফারেন্স](https://scalate.github.io/scalate/documentation/ssp-reference.html)


