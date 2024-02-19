{
  "date": "2021-04-08",
  "keywords": [
    "oar file",
    "oar file format",
    "what is an oar file",
    "file",
    "oar example",
    "oar file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "OAR - OpenSimulator আর্কাইভ ফাইল ফরম্যাট",
  "description": "OAR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা OAR ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oar-bn"
    }
  },
  "lastmod": "2021-04-15"
}

## একটি OAR ফাইল কি?

.oar এক্সটেনশন সহ একটি ফাইল হল একটি সংরক্ষণাগার ফাইল যা OpenSimulator অ্যাপ্লিকেশন দ্বারা ব্যবহৃত হয় যা একটি ওপেন-সোর্স 3D অ্যাপ্লিকেশন সার্ভার যা নেটওয়ার্কে বহু-ব্যবহারকারীর জন্য অ্যাক্সেসযোগ্য একটি ভার্চুয়াল পরিবেশ তৈরি করার জন্য। OAR ফাইল বিন্যাস একটি ভিন্ন সিস্টেমে ভূখণ্ড, অবজেক্ট টেক্সচার এবং ইনভেন্টরিগুলি সম্পূর্ণরূপে লোড করার জন্য প্রয়োজনীয় সম্পদ ডেটা সরবরাহ করে। OpenSimulator এছাড়াও ঐচ্ছিক হাইপারগ্রিড আছে যা ব্যবহারকারীদের ওয়েব জুড়ে অন্যান্য OpenSimulator ইনস্টলেশন দেখার অনুমতি দেয়। OAR ফাইলগুলিতে ইন্টারনেট MIME প্রকারের অ্যাপ্লিকেশন/oar থাকে এবং এতে এক বা একাধিক সংরক্ষণাগারভুক্ত ফাইল থাকে।


## OAR ফাইল ফরম্যাট

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. একটি OAR ফাইল হল একটি জিজিপড টার ফাইল (tar.gz) মূল ইউনিক্স টার ফরম্যাটে (USTAR নয়)।

## OAR অঞ্চলের উদাহরণ
AOR ফাইলে একাধিক অঞ্চল থাকতে পারে। সংরক্ষণাগারের গঠন নিম্নরূপ (এই উদাহরণে 4টি অঞ্চল রয়েছে):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

সংরক্ষণাগার নিয়ন্ত্রণ ফাইলে ভবিষ্যত বিন্যাস পরিবর্তনের সাথে সামঞ্জস্যতা নির্ধারণের জন্য একটি প্রধান সংস্করণ নম্বর রয়েছে। একটি OAR বিন্যাসে সম্পদের উপস্থিতি বুলিয়ান উপাদান দ্বারা নির্দেশিত হয়<assets_included> . অন্তর্ভুক্ত অঞ্চলগুলির তথ্য একটি ম্যানিফেস্টে রয়েছে যা নিয়ন্ত্রণ ফাইলে উপস্থিত রয়েছে। Archive.xml এর একটি উদাহরণ নিম্নরূপ।

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## তথ্যসূত্র

 * [OAR ফরম্যাট v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [ওপেনসিমুলেটর](http://opensimulator.org/wiki/Main_Page)

