---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LRM ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা RM ফাইল তৈরি এবং খুলতে পারেs.
title: Rএম ফাইল ফর্মat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## একটি RM ফাইল কি? ##

RealMedia হল RealNetworks দ্বারা তৈরি একটি মালিকানাধীন মাল্টিমিডিয়া কন্টেইনার ফর্ম্যাট যা .rm এক্সটেনশন ব্যবহার করে। এটি ইন্টারনেটে স্ট্রিমিংয়ের জন্য [RealAudio (RA)](/audio/ra/) এবং [RealVideo(RV)](/video/rv/) এর সংমিশ্রণে ব্যবহৃত হয়। এই স্ট্রীম ধ্রুবক বিটরেট হয়. পরিবর্তনশীল বিটরেটের জন্য, RealNetworks RealMedia ভেরিয়েবল বিটরেট (RMVB) বিন্যাস তৈরি করেছে। RealMedia ইন্টারনেটে সামগ্রী স্ট্রিম করার জন্য উপযুক্ত এবং উদাহরণস্বরূপ লাইভ টেলিভিশন স্ট্রিমিং এর জন্য ব্যবহার করা যেতে পারে।

## রিয়েলমিডিয়া ফাইলের গঠন ##

একটি RealMedia ফাইলে কয়েকটি খণ্ডের সিরিজ থাকে, যার প্রতিটির নিম্নলিখিত কাঠামো থাকে:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

RealMedia ফাইলে উপস্থিত খণ্ডগুলির প্রকারগুলি নিম্নরূপ:

- **রিয়েলমিডিয়া ফাইল হেডার (.RMF)**: এটি অবশ্যই রিয়েলমিডিয়া ফাইলের প্রথম অংশ হতে হবে। একটি ফাইলে শুধুমাত্র একটি RMF খণ্ড রয়েছে। এতে হেডারের সংখ্যা সম্পর্কে তথ্য রয়েছে।
- **ফাইল প্রপার্টি হেডার (PROP)**: এতে RealMedia ফাইলের সাধারণ বৈশিষ্ট্য সম্পর্কে তথ্য রয়েছে। প্রতিটি RealMedia ফাইলে এই ধরনের শুধুমাত্র একটি অংশ আছে।
- **মিডিয়া বৈশিষ্ট্য শিরোনাম (MDPR)**: এই খণ্ডটিতে স্ট্রিম বৈশিষ্ট্য সম্পর্কে তথ্য রয়েছে। এতে স্ট্রিমের ধরন এবং ব্যবহৃত কোডেক সম্পর্কে তথ্য রয়েছে। ফাইলটিতে প্রতিটি স্ট্রিমের জন্য একটি MDPR খণ্ড রয়েছে।
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **ডেটা হেডার (DATA): এই খণ্ডটিতে ডেটা প্যাকেটের একটি গ্রুপ রয়েছে।
- **ইনডেক্স হেডার (INDX): এই খণ্ডটি সমস্ত ডেটা খণ্ডের পরে আসে এবং এতে ইনডেক্স এন্ট্রি থাকে। একটি ফাইলে একাধিক INDX খণ্ড থাকতে পারে।

## সমর্থিত অডিও এবং ভিডিও ফরম্যাট ##

### অডিও ফরম্যাট ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- সিপ্র: সিপ্রো
- রান্না: রান্না
- atrc: ATRAC3
- ralf: রিয়েলঅডিও লসলেস ফরম্যাট
- raac: LC-AAC
- racp: HE-AAC

### ভিডিও ফরম্যাট ###

- CLV1: ক্লিয়ারভিডিও
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 অগ্রদূত
- RV40: H.264 অগ্রদূত, RV40
- RVTR: H.263+ (RV20)

## তথ্যসূত্র ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

