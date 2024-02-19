
{
  "date": "2022-02-06",
  "keywords": [
    ".apks file",
    "extension",
    "format",
    "APK Set Archive",
    "how to open .apks file",
    "apks file format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "APKS ফাইল - APK সেট আর্কাইভ",
  "description": "একটি APKS ফাইল কি সম্পর্কে জানুন?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apks-bn"
    }
  },
  "lastmod": "2022-02-06"
}

## একটি APKS ফাইল কি?

.apks এক্সটেনশন সহ একটি ফাইল হল একটি সংরক্ষণাগার ফাইল যা Android প্যাকেজ **APK** ফাইলগুলির একটি সংগ্রহ৷ APKS ফাইলের প্রতিটি পৃথক APK ফাইল ডিভাইসের বিভিন্ন দিক বিবেচনা করে তৈরি করা হয়। এর মধ্যে রয়েছে আর্কিটেকচার, ভাষা, পর্দার ঘনত্ব এবং অন্যান্য ডিভাইসের বৈশিষ্ট্য। APKS ফাইলগুলি **bundletool** দ্বারা তৈরি করা হয়। এটি অ্যান্ড্রয়েড অ্যাপ বান্ডেল তৈরি করতে এবং ডিভাইসে স্থাপনের জন্য অ্যাপ বান্ডিলকে ভিন্ন ভিন্ন APK-এ রূপান্তর করতে ব্যবহৃত হয়।

## APKS ফাইল ফরম্যাট - আরও তথ্য

APKS ফাইলগুলি [ZIP](/compression/zip/) ফাইল ফর্ম্যাট ব্যবহার করে সংকুচিত ফাইল হিসাবে সংরক্ষিত হয়৷

## কিভাবে একটি APKS ফাইল তৈরি করতে হয়?

অ্যান্ড্রয়েড অ্যাপ বান্ডেল (AAB) প্রস্তুত হলে, Google Play Store-এ এর আচরণ একটি ডিভাইসে স্থাপনের জন্য পরীক্ষা করা যেতে পারে। APKS ফাইলগুলি তৈরি করা যেতে পারে, এই উদ্দেশ্যে, AAB ফাইল থেকে এবং Google এর Android [bundletool](https://developer.android.com/tools/bundletool) ব্যবহার করে পরীক্ষা ডিভাইসে ইনস্টল করা যেতে পারে৷ এটি নিম্নলিখিত কমান্ড ব্যবহার করে APKs থেকে APKS সংরক্ষণাগার ফাইল তৈরি করতে কমান্ড লাইন সরঞ্জাম সরবরাহ করে।

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

একটি ডিভাইসে APK গুলি স্থাপন করার জন্য, APKS ফাইলটি অনুসরণ করে ডিভাইস সাইনিং তথ্যের সাথে স্বাক্ষর করা যেতে পারে।

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## তথ্যসূত্র

 * [bundletool - কমান্ডলাইন](https://developer.android.com/tools/bundletool)

