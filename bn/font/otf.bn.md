{
  "date": "2020-08-20",
  "keywords": [
    "otf file",
    "otf file format",
    "what is a otf file",
    "file",
    "otf example",
    "otf file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "OTF - TrueType ফন্ট ফাইল ফরম্যাট",
  "description": "OTF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা OTF ফাইল তৈরি করতে এবং খুলতে পারে।",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-otf-bn"
    }
  },
  "lastmod": "2020-09-21"
}

## একটি OTF ফাইল কি?

.otf এক্সটেনশন সহ একটি ফাইল OpenType ফন্ট ফরম্যাটকে বোঝায়। OTF ফন্ট ফরম্যাট আরও মাপযোগ্য এবং ডিজিটাল টাইপোগ্রাফির জন্য [TTF](/font/ttf/) ফর্ম্যাটের বিদ্যমান বৈশিষ্ট্যগুলিকে প্রসারিত করে৷ Microsoft এবং Adobe দ্বারা তৈরি, OTF পোস্টস্ক্রিপ্ট এবং TrueType ফন্ট ফর্ম্যাটের বৈশিষ্ট্যগুলিকে একত্রিত করে৷ এটি সংখ্যাগরিষ্ঠ লেখার সিস্টেমগুলিকে মিটমাট করার জন্য OTF ফর্ম্যাট তৈরি করে এবং সেই কারণেই এটি প্রধান কম্পিউটার প্ল্যাটফর্মগুলিতে সমানভাবে ব্যবহৃত হয়। OpenType ফন্ট ফরম্যাট Mac OS X এবং Windows 2000 এবং পরবর্তীতে সমর্থিত।

## সংক্ষিপ্ত ইতিহাস

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. অ্যাডোবের টাইপ 1 (পোস্টস্ক্রিপ্ট) ফন্ট ফরম্যাটের বৈশিষ্ট্যগুলি পূরণ করে এমন আরও উপযুক্ত ফন্ট ফর্ম্যাট প্রবর্তন করার জন্য পরিবর্তনগুলি অন্তর্ভুক্ত করা হয়েছে।

অ্যাডোব, 1996 সালে, অ্যাপলের ট্রু টাইপ এবং নিজস্ব টাইপ 1 ফন্ট ফরম্যাট উভয়কেই ছাড়িয়ে যাওয়ার প্রচেষ্টায় মাইক্রোসফটে যোগ দেয়। এর ফলে সীমাবদ্ধতা কাটিয়ে উঠতে এবং নতুন এক্সটেনশন যোগ করতে উভয় অন্তর্নিহিত ফন্ট ফরম্যাটের সমন্বয় ঘটেছে। এই নতুন প্রযুক্তিটি একই বছর **ওপেনটাইপ** নামে চালু করা হয়েছিল।

## OTF ফাইল ফরম্যাট স্পেসিফিকেশন

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF ডেটা প্রকার
OTF ফাইলগুলি নিম্নলিখিত ডেটা প্রকারগুলি ব্যবহার করে যা সমস্ত বিগ এন্ডিয়ানে রয়েছে৷

|ডেটা টাইপ| বর্ণনা|
---|---|
|uint8| 8-বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা
|int8| 8-বিট স্বাক্ষরিত পূর্ণসংখ্যা
|uint16| 16-বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা।|
|int16| 16-বিট স্বাক্ষরিত পূর্ণসংখ্যা
|uint24| 24-বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা।|
|uint32| 32-বিট স্বাক্ষরবিহীন পূর্ণসংখ্যা।|
|int32| 32-বিট স্বাক্ষরিত পূর্ণসংখ্যা
|স্থির | 32-বিট স্বাক্ষরিত ফিক্সড-পয়েন্ট নম্বর (16.16)|
|FWORD| int16 যা ফন্ট ডিজাইন ইউনিটে একটি পরিমাণ বর্ণনা করে।|
|UFWORD| uint16 যা ফন্ট ডিজাইন ইউনিটে একটি পরিমাণ বর্ণনা করে।|
|F2DOT14| কম 14 বিট ভগ্নাংশ (2.14) সহ 16-বিট স্বাক্ষরিত নির্দিষ্ট সংখ্যা।|
|LONGDATETIME| তারিখ এবং সময় 12:00 মধ্যরাত থেকে সেকেন্ডের সংখ্যায়, 1 জানুয়ারী, 1904, UTC। মানটিকে একটি স্বাক্ষরিত 64-বিট পূর্ণসংখ্যা হিসাবে উপস্থাপন করা হয়।|
|ট্যাগ| চারটি uint8s (দৈর্ঘ্য = 32 বিট) এর অ্যারে একটি টেবিল, নকশা-প্রকরণ অক্ষ, স্ক্রিপ্ট, ভাষা ব্যবস্থা, বৈশিষ্ট্য বা বেসলাইন সনাক্ত করতে ব্যবহৃত হয়|
|অফসেট16| একটি টেবিলের সংক্ষিপ্ত অফসেট, uint16 এর মতো, NULL অফসেট = 0x0000|
|অফসেট32| একটি টেবিলে লম্বা অফসেট, uint32 এর মতো, NULL অফসেট = 0x00000000|
|সংস্করণ16ডট16| বড় এবং ছোট সংস্করণ নম্বর সহ 32-বিট মান প্যাক করা। (টেবিল সংস্করণ সংখ্যা দেখুন।) |

### OTF টেবিল ডিরেক্টরি

একটি OTF ফাইল একটি টেবিল ডিরেক্টরি দিয়ে শুরু হয়। এই ডিরেক্টরিটি ফন্ট ফাইলের টেবিলের শীর্ষ-স্তরের সংগ্রহ। একটি ফাইলের ফন্টের সংখ্যার উপর নির্ভর করে, টেবিল ডিরেক্টরিটি ফাইলের বিভিন্ন স্থানে অবস্থিত হতে পারে। উদাহরণস্বরূপ, যদি ফন্ট ফাইলে শুধুমাত্র একটি ফন্ট থাকে, টেবিল ডিরেক্টরিটি ফাইলের বাইট 0 থেকে শুরু হয়। একাধিক OpenType ফন্ট সংগ্রহের ক্ষেত্রে,
টেবিল ডিরেক্টরির শুরুটি TTCHeader-এ নির্দেশিত হয়েছে।

|প্রকার |নাম |বিবরণ |
---|---|---|
|uint32 |sfntVersion | 0x00010000 বা 0x4F54544F ('OTTO')|
|uint16| numTables |সারণীর সংখ্যা।|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, যেখানে ** একটি সূচক অপারেটর)|
|uint16 | entrySelector Log2 সর্বাধিক পাওয়ারের 2 কম বা numTables এর সমান (log2(searchRange/16), যা ফ্লোর(log2(numTables)))।|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - অনুসন্ধান রেঞ্জ)
|টেবিলরেকর্ড| tableRecords[numTables] |টেবিল রেকর্ড অ্যারে—ফন্টের প্রতিটি টপ-লেভেল টেবিলের জন্য একটি|


### টেবিল রেকর্ড

ফন্টের প্রতিটি শীর্ষ-স্তরের টেবিলের জন্য, একটি টেবিল রেকর্ড রয়েছে যা নিম্নলিখিত ক্ষেত্রগুলি নিয়ে গঠিত।

|প্রকার| নাম| বর্ণনা|
---|---|---|
|ট্যাগ| টেবিলট্যাগ| টেবিল শনাক্তকারী
|uint32| চেকসাম| এই টেবিলের জন্য চেকসাম।|
|অফসেট32| অফসেট| ফন্ট ফাইলের শুরু থেকে অফসেট।|
|uint32| দৈর্ঘ্য এই টেবিলের দৈর্ঘ্য।|

OpenType ফন্ট ফাইলের প্রতিটি টেবিল টেবিল ট্যাগ নামে পরিচিত নাম দ্বারা প্রতিনিধিত্ব করা হয়। অ্যারের সমস্ত রেকর্ডের জন্য ট্যাগ দ্বারা আরোহী ক্রমে সাজানো আবশ্যক।

## তথ্যসূত্র
 * [Microsoft-এর ওপেনটাইপ ফন্ট স্পেসিফিকেশন](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [ট্রু টাইপ ওভারভিউ](https://learn.microsoft.com/en-us/typography/truetype/)

