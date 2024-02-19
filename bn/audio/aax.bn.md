{
  "date": "2021-06-08",
  "keywords": [
    "AAX",
    "file",
    "extension",
    "format",
    "AAX file",
    "audio",
    "AAX file format",
    "what is an aax file",
    "AAX file format specifications"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "AAX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা AAX ফাইল তৈরি এবং খুলতে পারে।",
  "title": "AAX - উন্নত অডিও কোডিং ফাইল",
  "linktitle": "AAX",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aax-bn"
    }
  },
  "lastmod": "2021-06-08"
}

## একটি AAX ফাইল কি?
.aax এক্সটেনশন সহ ফাইলগুলি [Audible](https://www.audible.com/) দ্বারা বিকাশিত অডিওবুক; Amazon.com Inc-এর মালিকানাধীন একটি আমেরিকান অনলাইন পডকাস্ট পরিষেবা এবং অডিওবুক। এই ফাইলগুলি Audiblekids, Audible.com এবং iTune স্টোর ব্যবহার করতে পারে। AAX ফাইল হল ডিজিটাল মাল্টিমিডিয়া অডিওবুক যার মধ্যে গ্রাফিক্স, ভিডিও, বুকমার্ক এবং একটি ভিডিও টাইমলাইনের মতো বৈশিষ্ট্য থাকতে পারে; বাচ্চাদের জন্য **ছবির বই** এবং **গ্রাফিক নভেল** এর জন্য তাদের আরও উপযোগী এবং উপযুক্ত পছন্দ করে তোলা। AAX ফাইলগুলিকে AA ফাইলের উন্নত সংস্করণ হিসাবে বিবেচনা করা হয়।

## AAX ফাইল বিন্যাস
AAX হল একটি অডিওবুক ফাইল ফরম্যাট, যা একটি M4B ফাইল যার পরিবর্তনশীল-বিটরেটের কারণে উচ্চ মানের এবং ডিআরএম (ডিজিটাল রাইটস ম্যানেজমেন্ট) এনক্রিপশন অ্যালগরিদম দিয়ে এনক্রিপ্ট করা। বেশিরভাগ ইবুক 64 kbit/s, 22.050 kHz, স্টেরিওতে এনকোড করা হয়, কিছু 32k এর মতো কম, মনো এবং রেডিও প্লে সাধারণত 128kbit/s এবং 44.1 kHz এ এনকোড করা হয়। AAX ফাইল ফরম্যাটের অডিও AAC ফরম্যাটে (ভেরিয়েবল কোয়ালিটি) এনকোড করা হয়েছে।

### AAX ফাইল ফরম্যাট স্পেসিফিকেশন
শ্রবণযোগ্য AAX ফাইল ফর্ম্যাট মানের চশমা সম্পর্কে বিস্তারিত নীচে দেখানো হয়েছে:

- **বিটরেট:** 32 - 128 kbit/s
- **নমুনা হার:** 22.050 - 44.10 kHz
- **বিট গভীরতা:** অজানা
- **চ্যানেল:** মনো বা স্টেরিও
- **MBytes/hour:** 28.8
- **ধারক:** MPEG-4 পর্ব 14
- **Quality description:** AAC sound

### ডিজিটাল রাইটস ম্যানেজমেন্ট (ডিআরএম)
Audible file formats encapsulate the encoded sounds but they also include the prevention for un-authorized playbacks by means of an Audible username and password, which can be used by-default on up to four computers and three smartphones at a time. Schools and libraries may be offered different types of licenses. The DRM is responsible to control:
- অননুমোদিত ব্যবহারকারী অ্যাক্সেস
- অনিয়ন্ত্রিত প্লেব্যাকের জন্য সীমিত সংখ্যক সিডি বার্ন করুন
- সীমিত সংখ্যক ডিভাইসের জন্য শ্রবণযোগ্য সামগ্রী সক্ষম করুন
কিন্তু আপনি এখনও অনেক অন্যান্য সফ্টওয়্যার সরঞ্জাম খুঁজে পেতে পারেন যা সহজেই Audible এর DRM নিয়ন্ত্রণকে বাইপাস করতে পারে। Audible এখন বিষয়বস্তু লেখকদের জন্য DRM-মুক্ত শিরোনাম অফার করছে। FFmpeg 2.8.1 বা তার চেয়ে বড় সংস্করণগুলি .aax ফাইল বিন্যাস স্থানীয়ভাবে চালাতে পারে।


## তথ্যসূত্র ##

* [শ্রবণযোগ্য (পরিষেবা) - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Audible_(service))

* [অডিও ফাইল ফরম্যাট - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Audio_file_format)


