{
  "date": "2023-06-12",
  "keywords": [
"বক",
"bak ফাইল",
"BAK ক্রোমিয়াম বুকমার্কস",
"একটি bak ফাইল কি?",
"কিভাবে bak ফাইল খুলবেন",
"ফাইল",
"bak ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK ফাইল ফরম্যাট - Chromium বুকমার্কস ব্যাকআপ",
  "description": "BAK Chromium বুকমার্ক ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি BAK ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-bn",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## একটি BAK ফাইল কি?

ক্রোমিয়াম-ভিত্তিক ওয়েব ব্রাউজারগুলির প্রসঙ্গে একটি .bak ফাইল, যেমন Google Chrome এবং Microsoft Edge, মূলত আপনার বুকমার্কগুলির একটি ব্যাকআপ ফাইল৷ এই বুকমার্কগুলি একটি প্লেইন টেক্সট তালিকা হিসাবে সংরক্ষিত হয়, এবং ব্যবহৃত ফাইল বিন্যাস হল JSON। এই .bak ফাইলগুলির উদ্দেশ্য হল একটি ব্যাকআপ প্রদান করে আপনার বুকমার্কগুলিকে সুরক্ষিত করা যা দুর্ঘটনাজনিত মুছে ফেলা বা হারানোর ক্ষেত্রে পুনরুদ্ধার করা যেতে পারে।

Google Chrome সহ ক্রোমিয়াম-ভিত্তিক ব্রাউজারগুলি নিয়মিতভাবে এই ব্যাকআপ ফাইলগুলি তৈরি করে এবং সাধারণত তাদের নাম দেয় Bookmarks.bak। এগুলি মূলত নির্দিষ্ট সময়ে আপনার বুকমার্কগুলির একটি স্ন্যাপশট।

## আপনার বুকমার্ক পুনরুদ্ধার করতে কিভাবে একটি .bak ফাইল ব্যবহার করবেন

1. **ব্যাকআপ ফাইলটি খুঁজুন:** এটি সাধারণত আপনার Chromium প্রোফাইলের সাথে যুক্ত একটি নির্দিষ্ট ফোল্ডারে অবস্থিত। সঠিক অবস্থান আপনার অপারেটিং সিস্টেমের উপর নির্ভর করে পরিবর্তিত হতে পারে।

উইন্ডোজে: `C:\Users\ এ দেখুন<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`।

macOS-এ: `~/Library/Application Support/Chromium/Default/Bookmarks.bak`-এ অনুসন্ধান করুন।

লিনাক্সে: `~/.config/chromium/Default/Bookmarks.bak` চেক করুন।

3. আপনার Chromium ব্রাউজার বন্ধ আছে তা নিশ্চিত করুন।
4. .bak এক্সটেনশনটি সরিয়ে Bookmarks.bak ফাইলের নাম পরিবর্তন করুন, তাই এটিকে সহজভাবে Bookmarks বলা হয়।
5. Chromium শুরু করুন।

.bak ফাইলটিকে বুকমার্কস এ পুনঃনামকরণ করার মাধ্যমে, Chromium এটিকে বর্তমান বুকমার্ক ফাইল হিসাবে ব্যবহার করবে এবং আপনার পূর্ববর্তী বুকমার্কগুলি পুনরুদ্ধার করা উচিত৷

## Chromium বুকমার্কস ব্যাকআপ

আপনি আপনার গুরুত্বপূর্ণ সংরক্ষিত ওয়েব পৃষ্ঠা এবং URL গুলি হারাবেন না তা নিশ্চিত করার জন্য আপনার Chromium বুকমার্কগুলির ব্যাক আপ নেওয়া একটি বুদ্ধিমান সতর্কতা। ক্রোমিয়াম হল একটি ওপেন সোর্স ব্রাউজার যা অন্যান্য ব্রাউজার যেমন Google Chrome এবং Microsoft Edge এর জন্য ভিত্তি হিসেবে কাজ করে। আপনার Chromium বুকমার্ক ব্যাক আপ করতে, এই পদক্ষেপগুলি অনুসরণ করুন:

## পদ্ধতি 1: ম্যানুয়াল ব্যাকআপ

1. **Chromium খুলুন**: আপনার কম্পিউটারে Chromium ব্রাউজার চালু করুন।

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **অবস্থান চয়ন করুন**: আপনি আপনার কম্পিউটারে এক্সপোর্ট করা বুকমার্ক ফাইলটি কোথায় সংরক্ষণ করতে চান তা চয়ন করুন৷ ডিফল্ট ফাইলের নাম হল bookmarks.html, কিন্তু আপনি চাইলে এটি পরিবর্তন করতে পারেন। আপনার মনে থাকবে এমন একটি স্থানে সংরক্ষণ করুন।

6. **সংরক্ষণ**: আপনার বুকমার্কগুলিকে একটি HTML ফাইল হিসাবে সংরক্ষণ করতে সংরক্ষণ করুন বা রপ্তানি বোতামে ক্লিক করুন৷

আপনার বুকমার্কগুলি এখন একটি HTML ফাইল হিসাবে ব্যাক আপ করা হয়েছে৷ আপনি নিরাপদ রাখার জন্য এই ফাইলটিকে একটি বাহ্যিক ড্রাইভ বা ক্লাউড স্টোরেজে অনুলিপি করতে পারেন৷

## পদ্ধতি 2: Google অ্যাকাউন্টের সাথে সিঙ্ক করুন (যদি প্রযোজ্য হয়)

আপনি যদি Chromium-এ একটি Google অ্যাকাউন্টে সাইন ইন করে থাকেন, তাহলে আপনি আপনার বুকমার্কগুলিকে সুরক্ষিত রাখতে এবং ডিভাইস জুড়ে সিঙ্ক্রোনাইজ করার জন্য অন্তর্নির্মিত সিঙ্কিং বৈশিষ্ট্যটিও ব্যবহার করতে পারেন৷ এইভাবে, আপনার বুকমার্কগুলি স্বয়ংক্রিয়ভাবে আপনার Google অ্যাকাউন্টে ব্যাক আপ করা হবে৷

1. **Chromium খুলুন**: Chromium ব্রাউজার চালু করুন এবং নিশ্চিত করুন যে আপনি আপনার Google অ্যাকাউন্টে সাইন ইন করেছেন।

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **সিঙ্ক এবং Google পরিষেবাগুলি**: সেটিংস ট্যাবে, বাম সাইডবারে সিঙ্ক এবং Google পরিষেবাগুলি এ ক্লিক করুন৷

4. **আপনার ডেটা সিঙ্ক করুন**: সিঙ্ক এর অধীনে নিশ্চিত করুন যে বুকমার্কস চালু আছে। এটি আপনার বুকমার্কগুলিকে আপনার Google অ্যাকাউন্টের সাথে সিঙ্ক করবে৷

আপনার বুকমার্কগুলি এখন স্বয়ংক্রিয়ভাবে ব্যাক আপ করা হবে এবং আপনার Google অ্যাকাউন্টের সাথে সিঙ্ক্রোনাইজ করা হবে৷ আপনি Chromium বা Google সিঙ্কিং সমর্থন করে এমন অন্য ব্রাউজার দিয়ে যেকোনো ডিভাইসে আপনার Google অ্যাকাউন্টে সাইন ইন করে সেগুলি অ্যাক্সেস করতে পারেন।

পর্যায়ক্রমে আপনার বুকমার্কগুলিকে ম্যানুয়ালি ব্যাক আপ করতে মনে রাখবেন, বিশেষ করে যদি আপনি একটি স্থানীয় অনুলিপি চান যা আপনার Google অ্যাকাউন্টের সিঙ্কিংয়ের উপর সম্পূর্ণ নির্ভরশীল নয়৷

## কিভাবে একটি BAK ফাইল খুলবেন

আপনি যদি আপনার বুকমার্ক ব্যাকআপের কাঁচা ডেটা অন্বেষণ করতে চান, আপনি Bookmarks.bak ফাইলটি বিভিন্ন পাঠ্য সম্পাদক যেমন Microsoft Visual Studio Code (একাধিক প্ল্যাটফর্মে উপলব্ধ), Microsoft Notepad (Windows ব্যবহারকারীদের জন্য), Apple TextEdit সহ খুলতে পারেন। (ম্যাক ব্যবহারকারীদের জন্য), বা আপনার পছন্দের অন্য কোনো পাঠ্য সম্পাদক। এটি করার ফলে আপনি ফাইলটিতে থাকা বুকমার্ক এবং মেটাডেটা দেখতে পারবেন।

আপনি Bookmarks.bak ফাইলটি খুলতে পারেন এবং বিভিন্ন টেক্সট এডিটিং সফটওয়্যার এবং কোড এডিটর ব্যবহার করে এর বিষয়বস্তু দেখতে পারেন। এখানে কিছু সাধারণভাবে ব্যবহৃত বিকল্প রয়েছে:

1. ভিজ্যুয়াল স্টুডিও কোড (ভিএস কোড)
2. নোটপ্যাড (উইন্ডোজ)
3. টেক্সট এডিট (ম্যাক)
4. সাবলাইম টেক্সট
5. নোটপ্যাড++
6. পরমাণু
7. ন্যানো এবং ভিম (লিনাক্স)
8. ওয়ার্ডপ্যাড (উইন্ডোজ)

## অন্যান্য BAK ফাইল

এখানে অন্যান্য ফাইলের ধরন রয়েছে যা **.bak** ফাইল এক্সটেনশন ব্যবহার করে।

**তথ্যশালা**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**খেলা**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**বিবিধ**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**সেটিংস**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## তথ্যসূত্র
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
