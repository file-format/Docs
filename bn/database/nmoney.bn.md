{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "NMONEY ফাইল ফর্ম্যাট এবং APIগুলি সম্পর্কে জানুন যা NMONEY ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title" : "NMONEY ফাইল - Denaro অ্যাকাউন্ট ফাইল ফর্ম্যাট",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## একটি NMONEY ফাইল কি?

একটি NMONEY ফাইল হল একটি আর্থিক ডেটা স্টোরেজ ডাটাবেস ফাইল যাতে আর্থিক লেনদেনের ট্র্যাক রেকর্ড থাকে। এটি নিকভিশন দ্বারা তৈরি করা হয়েছিল এবং নিকভিশন ডেনারো সফ্টওয়্যার ব্যবহার করা হয়েছিল যা একটি ব্যক্তিগত আর্থিক সফ্টওয়্যার অ্যাপ্লিকেশন। একটি NOMONEY ফাইলের মধ্যে সংরক্ষিত ডেটা একটি অ্যাকাউন্টে ক্রেডিট এবং ডেবিট লেনদেনের তথ্য অন্তর্ভুক্ত করে।

NOMONEY ফাইলগুলি [Github](https://github.com/NickvisionApps/Denaro) অ্যাপ্লিকেশন দিয়ে খোলা যাবে৷

## Denaro সফটওয়্যার সম্পর্কে

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Denaro দ্বারা অফার করা বৈশিষ্ট্য

 * এর সবচেয়ে জনপ্রিয় এবং পরিচিত ট্যাব ইন্টারফেসের সাথে একসাথে একাধিক অ্যাকাউন্ট পরিচালনা করুন
 * প্রকার, গোষ্ঠী বা তারিখ অনুসারে লেনদেন ফিল্টার করুন
 * লেনদেনের পুনরাবৃত্তি করুন যেমন বিলগুলি প্রতি মাসে ঘটে
 * এক অ্যাকাউন্ট থেকে অন্য অ্যাকাউন্টে অর্থ স্থানান্তর করুন
 * একটি অ্যাকাউন্ট থেকে একটি CSV ফাইল হিসাবে ডেটা রপ্তানি করুন এবং একটি অ্যাকাউন্টে লেনদেন যোগ করতে একটি CSV, OFX বা QIF ফাইল আমদানি করুন

## Denaro ফাইল বিন্যাস - আরো তথ্য

Denaro ফাইল বাইনারি ফাইল ফরম্যাটে ডিস্কে সংরক্ষিত হয়। আর্থিক তথ্য **.SQLITE3** ফাইল বিন্যাসে একটি ডাটাবেস ফাইল হিসাবে সংরক্ষণ করা হয়। SQLITE হল একটি লাইটওয়েট SQL ডাটাবেস ফাইল যা SQLite সফ্টওয়্যার দিয়ে তৈরি করা হয়েছে। এটি স্বয়ংসম্পূর্ণ ডাটাবেস ইঞ্জিন সরবরাহ করে যা সম্পূর্ণ বৈশিষ্ট্যযুক্ত এবং অত্যন্ত নির্ভরযোগ্য ডাটাবেস প্রদান করতে সক্ষম। SQLite ডাটাবেস ফাইলগুলি নেটওয়ার্কের মাধ্যমে এই ফাইলগুলিকে কেবল বিনিময় করে সিস্টেমগুলির মধ্যে সমৃদ্ধ বিষয়বস্তু ভাগ করে নেওয়ার জন্য ব্যবহার করা যেতে পারে। সি, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/), এবং আরও অনেকের মতো প্রোগ্রামিং ভাষার জন্য SQLite বাইন্ডিং বিদ্যমান।

## তথ্যসূত্র

 * [নিকভিশন](https://nickvision.org/)
 * [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

