{
  "date": "2021-06-09",
  "keywords": [
    "cue",
    "file",
    "extension",
    "format",
    "what is a cue file",
    "music",
    "cue file format",
    "cue file format specification",
    "cue sheet",
    "CDRWIN"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "CUE ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা CUE ফাইল তৈরি, রূপান্তর এবং খুলতে পারে।",
  "title": "CUE - কিউ শীট ফাইল",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cue-bn"
    }
  },
  "lastmod": "2021-07-01"
}

## একটি CUE ফাইল কি?

.cue এক্সটেনশন সহ একটি ফাইল, যা কিউ শীট ফাইল নামেও পরিচিত, এটি একটি মেটাডেটা ফাইল যা একটি সিডি বা ডিভিডিতে ট্র্যাকগুলির বিন্যাস সম্পর্কে তথ্য ধারণ করে। এগুলি মিডিয়া প্লেয়ার এবং অপটিক্যাল ডিস্ক অথরিং অ্যাপ্লিকেশন দ্বারা সমর্থিত। সিডিতে সংরক্ষিত প্রধান অডিও ডেটা ট্র্যাকের দৈর্ঘ্য, ডিস্ক শিরোনাম এবং পারফর্মারগুলির বৈশিষ্ট্য সহ কিউ ফাইল দ্বারা উল্লেখ করা হয়। এইভাবে যদি একটি একক অডিও ফাইলে একাধিক ট্র্যাক থাকে তবে কিউ ফাইলটি অডিওটিকে একাধিক ফাইলে ভাগ করতে বা বিভিন্ন ট্র্যাকের উল্লেখ করতে ব্যবহার করা যেতে পারে।

## CUE ফাইল ফরম্যাট

CUE বা কিউ শীট ফাইলগুলি সাধারণ পাঠ্য বিন্যাসে সংরক্ষণ করা হয় যা মানুষের পাঠযোগ্য। একটি কিউ ফাইলের তথ্য হল এক বা একাধিক প্যারামিটার সহ কমান্ড। এই কমান্ডগুলি হয় সম্পূর্ণ ফাইলে বা একটি পৃথক ট্র্যাকের জন্য প্রযোজ্য, নির্দিষ্ট কমান্ড এবং প্রেক্ষাপটের উপর নির্ভর করে। CDRWIN ব্যবহারকারী নির্দেশিকা ক্যু শীট সিনট্যাক্স এবং শব্দার্থবিদ্যার স্পেসিফিকেশন বর্ণনা করে।

## CUE শীট অপরিহার্য আদেশ

|কমান্ড|বর্ণনা|
---|---|
|ফাইল| ডেটা এবং এর বিন্যাস যেমন [MP3](/audio/mp3/), [WAV](/audio/wav/), বা প্লেইন বাইনারি ডিস্ক চিত্র)|
|ট্র্যাক| ট্র্যাক প্রসঙ্গ তথ্য যেমন এর সংখ্যা এবং প্রকার বা মোড সংজ্ঞায়িত করে।|
|INDEX| FILE-এর মধ্যে একটি সূচক হিসাবে অবস্থানটি উপস্থাপন করে। বিন্যাস হল mm:ss:ff (মিনিট-সেকেন্ড-ফ্রেম)।|
|PREGAP এবং POSTGAP|এটি একটি ট্র্যাকের প্রিগ্যাপ বা পোস্ট-গ্যাপ নির্দেশ করে, যা কোনো ডেটা ফাইলে সংরক্ষণ করা হয় না। দৈর্ঘ্যটি INDEX-এর মতো একই মিনিট-সেকেন্ড-ফ্রেম বিন্যাসে নির্দিষ্ট করা হয়েছে।|

### CUE শিটের উদাহরণ

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## অন্যান্য CUE ফাইল

এখানে অন্যান্য ফাইলের ধরন রয়েছে যা **.cue** ফাইল এক্সটেনশন ব্যবহার করে।

**ডিস্ক এবং মিডিয়া**
- [CUE - কিউ শীট ফাইল](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## তথ্যসূত্র

* [.cda ফাইল - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/.cda_file)


