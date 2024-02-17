{
  "date" : "2020-08-20",
  "keywords" : [ "sdf file", "sdf file format", "what is a sdf file", "file", "sdf example", "sdf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SFD - স্প্লাইন ফন্ট ডেটাবেস বিন্যাস",
  "description":"SFD ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি SFD ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "SFD",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-24"
}

## একটি SFD ফাইল কি?

.sfd (Spline Font Database) এক্সটেনশন সহ একটি ফাইল হল ফন্ট এডিটিং সফ্টওয়্যারের জন্য নেটিভ ASCII ফন্ট ফরম্যাট - FontForge। সফ্টওয়্যার সমর্থন করে অন্যান্য অনেক সাধারণ ফন্ট ফর্ম্যাট সমর্থন করে এবং অবাধে উপলব্ধ। সফ্টওয়্যারটি লিনাক্স, উইন্ডোজ এবং ম্যাকওএস সহ প্রায় সমস্ত আধুনিক অপারেটিং সিস্টেমের জন্য ব্যবহার করা যেতে পারে।

## **SFD ফাইল ফরম্যাট**
SFD ফাইলগুলি হল ASCII ফাইল যা মানুষের পাঠযোগ্য এবং সহজেই ইন্টারনেট জুড়ে স্থানান্তরিত হয়৷ এটি অ্যাপ্লিকেশন/vnd.font-fontforget-sfd দ্বারা এর MIME প্রকার হিসাবে চিহ্নিত করা হয়েছে।

### হেডার
একটি সাধারণ SFD ফাইল হেডার নিচের উদাহরণে দেখানো হয়েছে।

```
SplineFontDB: 3.0
FontName: Ambrosia
FullName: Ambrosia
FamilyName: Ambrosia
DefaultBaseFilename: Ambrosia-1.0
Weight: Medium
Copyright: Copyright (C) 1995-2000 by George Williams
Comments: This is a funny font.
UComments: "This is a funny font."
FontLog: "Create Jan 2008"
Version: 001.000
ItalicAngle: 0
UnderlinePosition: -133
UnderlineWidth: 20
Ascent: 800
Descent: 200
sfntRevision: 0x00078106
WidthSeparation: 140
LayerCount: 4
Layer: 0 0 "Back" 1
Layer: 1 1 "Fore" 0
Layer: 2 0 "Cubic_Fore" 0
Layer: 3 0 "Test" 1
DisplaySize: -24
DisplayLayer: 1
AntiAlias: 1
WinInfo: 64 16 4
FitToEm: 1
UseUniqueID: 0
UseXUID: 1
XUID: 3 18 21
Encoding: unicode
Order2: 1
OnlyBitmaps: 0
MacStyle: 0
TeXData: 1 10485760 0 269484 134742 89828 526385 1048576 89828
CreationTime: 1151539072
ModificationTime: 11516487392
GaspTable 3 8 2 16 1 65535 3 0
DEI: 91125
ExtremaBound: 30
```


## **তথ্যসূত্র**

 * [SFD File Format by FontForge](https://fontforge.org/docs/techref/sfdformat.html)

