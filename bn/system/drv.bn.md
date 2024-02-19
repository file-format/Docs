{
  "date": "2021-07-08",
  "keywords": [
    "DRV",
    "extension",
    "file",
    "format",
    "system",
    "Driver",
    "Windows Device Driver",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "DRV - উইন্ডোজ ডিভাইস ড্রাইভার",
  "description": "DRV ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DRV ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-drv-bn"
    }
  },
  "lastmod": "2021-07-08"
}

## একটি DRV ফাইল কি? ##

.drv এক্সটেনশন সহ ফাইলগুলি উইন্ডোজ ডিভাইস ড্রাইভারের অন্তর্গত। উইন্ডোজ অপারেটিং সিস্টেম অভ্যন্তরীণ এবং বাহ্যিক হার্ড ডিভাইসগুলিকে সংযুক্ত করতে এই ফাইলগুলি ব্যবহার করে। ডিআরভি ফাইলগুলি একটি ডিভাইস এবং অপারেটিং সিস্টেমকে কীভাবে একত্রিত করে তার জন্য নির্দেশাবলী এবং পরামিতিগুলি নিয়ে গঠিত। এই ফাইলগুলি উইন্ডোজের সাথে সঠিকভাবে কাজ করার জন্য ডিভাইস ড্রাইভার ইনস্টল করতে সাহায্য করে। এছাড়াও, বাস বা তারের মাধ্যমে পিসির মাদারবোর্ডের সাথে সংযুক্ত ডিভাইসগুলির জন্য DRV ফাইলের প্রয়োজন হয়।


## DRV ফাইল ফরম্যাট ##

DRV ফাইলগুলি সাধারণত ডায়নামিক লাইব্রেরি ([DDL](/system/dll/) ফাইল) বা [EXE](/executable/exe/) ফাইল হিসাবে প্যাকেজ করা হয়৷ এই ফাইলগুলি সমস্ত সিস্টেম প্ল্যাটফর্মে সমর্থিত হতে পারে, যেমন স্মার্টফোন, এবং কোনও নিশ্চয়তা নেই যে প্রতিটি প্ল্যাটফর্ম এই ফাইলগুলিকে সঠিকভাবে সমর্থন করবে৷ যাইহোক, কিছু সাধারণ ডিভাইস যা .drv ফাইল এক্সটেনশন ব্যবহার করে:

* সাউন্ড কার্ড
* গ্রাফিক কার্ড
* প্রিন্টার
* জমাকৃত যন্ত্রসমুহ
* নেটওয়ার্ক অ্যাডাপ্টার
* কম্পিউটার হার্ডওয়্যার আনুষাঙ্গিক

ইমেলের মাধ্যমে পাঠানো DRV ফাইলগুলি না খোলার পরামর্শ দেওয়া হচ্ছে কারণ এই ফাইল ফর্ম্যাটে ভাইরাস এবং অন্যান্য ক্ষতিকারক প্রোগ্রাম রয়েছে৷ কোনো অজানা DRV ফাইল খোলার আগে একটি ব্যাপক স্ক্যান করা নিশ্চিত করুন।


## DRV উদাহরণ ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

