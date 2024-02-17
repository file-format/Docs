---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI ফাইল ফর্মat
linktitle: MYI
description: LMYI ফাইল ফরম্যাট এবং APIs সম্পর্কে আয় করুন যা MYI ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## একটি MYI ফাইল কি? ##

MYI MySQL MyISAM Index ফাইল নামেও পরিচিত। এটি MySQL দ্বারা MyISAM টেবিলের জন্য সূচী সংরক্ষণ করতে ব্যবহৃত হয়। MySQL ডাটাবেস সূচক টেবিলের গঠন সংজ্ঞায়িত করে এবং টেবিলের অখণ্ডতা পরীক্ষা করার জন্য নিয়ন্ত্রণ প্রক্রিয়া ধারণ করে।

## MYI ফাইল ফরম্যাট ##

MYI ফাইলের দুটি অংশ আছে, শিরোনাম এবং মূল মান।

### MYI হেডার ###

হেডারে বিকল্প, ফাইলের আকার এবং কী সম্পর্কে তথ্য রয়েছে। মাইএসকিউএল-এর কীগুলি একটি কমান্ড দিয়ে তৈরি করা হয়

```sql
CREATE [UNIQUE] INDEX.
```

যে ফাইলগুলি MYI ফাইলগুলি পড়তে এবং লিখতে পারে সেগুলি ./myisam ডিরেক্টরিতে রয়েছে৷ এটিতে নিম্নলিখিত ফাইলগুলি রয়েছে:

- mi_open.c: এই ফাইলটিতে রুটিন রয়েছে যা হেডারের প্রতিটি অংশ লিখতে পারে।
- mi_create.c: এই ফাইলটিতে এমন রুটিন আছে যেগুলোকে mi_open.c রুটিন বলে।
- myisamdef.h: এই ফাইলটির গঠন সংজ্ঞা আছে।

হেডারে নিম্নলিখিত বিভাগগুলি রয়েছে:

- রাষ্ট্র: রাজ্যটি mi_open.c, mi_state_info_write() দ্বারা লেখা হয়েছে। এই কাঠামোটি ফাইলে একবার ঘটে।
- বেস: বেসটি mi_open.c, mi_base_info_write() দ্বারা লেখা হয়েছে। MI_BASE_INFO হল myisamdef.h-এ বেসের জন্য সংশ্লিষ্ট কাঠামো। এই কাঠামোটি ফাইলে একবার ঘটে।
- keydef: keydef লেখা হয়েছে mi_open.c, mi_keydef_write()। MI_KEYDEF হল myisamdef.h-এ keydef-এর জন্য সংশ্লিষ্ট কাঠামো। এটি একটি একাধিক-ঘটনা কাঠামো যা প্রতিটি সূচকের জন্য প্রদর্শিত হয়।
- recinfo: recinfo লেখা হয়েছে mi_open.c, mi_recinfo_write()। MI_COLUMNDEF হল myisamdef.h-এ recinfo-এর জন্য সংশ্লিষ্ট কাঠামো। এটি একটি মাল্টিপল ইভেন্সেন্স স্ট্রাকচার যা একটি কী-তে প্রদর্শিত প্রতিটি ক্ষেত্রের একবার প্রদর্শিত হয়।

### কী মান ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. একটি সাধারণ ব্লক কমপক্ষে 65% পূর্ণ এবং সাধারণত 80% পূর্ণ।

myisamdef.h ফাইলে ধ্রুবকগুলিতে প্রকাশ করা নিম্নলিখিত তথ্য রয়েছে। কীগুলির সর্বাধিক সংখ্যা হল 32 (MI_MAX_KEY) এবং একটি কী-তে সর্বাধিক সংখ্যক সেগমেন্ট হল 16 (MI_MAX_KEY_SEG)। কীটির সর্বাধিক দৈর্ঘ্য 500 (MI_MAX_KEY_LENGTH)। ব্লকের সর্বোচ্চ দৈর্ঘ্য হল 16384 (MI_MAX_KEY_BLOCK_LENGTH)।

## তথ্যসূত্র ##

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

