{
  "date": "2019-12-09",
  "keywords": [
    "3mf file",
    "3mf file format",
    "what is an 3mf file",
    "file",
    "3mf example",
    "3mf file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "3MF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা 3MF ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3mf-bn"
    }
  },
  "lastmod": "2019-12-09"
}

## একটি 3MF ফাইল কি?

3MF, 3D ম্যানুফ্যাকচারিং ফরম্যাট, বিভিন্ন অ্যাপ্লিকেশন, প্ল্যাটফর্ম, পরিষেবা এবং প্রিন্টারে 3D অবজেক্ট মডেল রেন্ডার করতে অ্যাপ্লিকেশন দ্বারা ব্যবহৃত হয়। এটি 3D প্রিন্টারের সর্বশেষ সংস্করণগুলির সাথে কাজ করার জন্য [STL](/cad/stl/) এর মতো অন্যান্য 3D ফাইল ফর্ম্যাটে সীমাবদ্ধতা এবং সমস্যাগুলি এড়াতে তৈরি করা হয়েছিল৷ 3MF তুলনামূলকভাবে একটি নতুন ফাইল বিন্যাস যা 3MF কনসোর্টিয়াম দ্বারা তৈরি এবং প্রকাশিত হয়েছে। এটি একটি মডেলকে সম্পূর্ণরূপে বর্ণনা করার জন্য যথেষ্ট সমৃদ্ধ, অভ্যন্তরীণ তথ্য, রঙ এবং অন্যান্য বৈশিষ্ট্য ধরে রাখে যা 3D প্রিন্টিং-এ নতুন উদ্ভাবনকে সমর্থন করার জন্য এটিকে সম্প্রসারণযোগ্য করে তোলে। ফরম্যাটটি এক্সটেনসিবল, ব্যাপকভাবে গৃহীত হতে সক্ষম এবং অন্যান্য বহুল ব্যবহৃত ফাইল ফরম্যাটগুলিকে ঘিরে সমস্যামুক্ত।

## 3MF ফাইল ফরম্যাটের সংক্ষিপ্ত ইতিহাস

উপলব্ধ মডেল বর্ণনামূলক ফাইল ফর্ম্যাটে বিদ্যমান সীমাবদ্ধতা, যেমন STL এবং অন্যান্য, নেতৃস্থানীয় ব্র্যান্ডগুলিকে একত্রিত হতে এবং 3D প্রিন্টিংয়ের জন্য আরও এক্সটেনসিবল ফাইল ফর্ম্যাট তৈরি করতে নেতৃত্ব দেয়। একটি গুরুত্বপূর্ণ বিবেচনা ছিল কিভাবে অ্যাপ্লিকেশনগুলিকে 3D প্রিন্টারে মডেল ডেটা পাস করা উচিত। 3MF কনসোর্টিয়াম, তাই, 3D প্রিন্টিংয়ের প্রয়োজন মেটাতে এটিকে যথেষ্ট প্রসারিত করার লক্ষ্যে 3MF নামক একটি নতুন 3D ফাইল ফর্ম্যাটকে ব্যাক করার জন্য তৈরি হয়েছিল। Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP এবং অন্যান্য সহ বেশ কয়েকটি কোম্পানি এই কনসোর্টিয়ামের অংশ ছিল। 3MF কনসোর্টিয়ামের সহযোগিতামূলক স্পেসিফিকেশনের আরও উন্নয়নের সূচনা পয়েন্ট হিসাবে মাইক্রোসফ্ট তার 3D ফাইল ফর্ম্যাট ওয়ার্ক-ইন-প্রোগ্রেস দান করেছে।

## 3MF ফাইল ফরম্যাট - আরও তথ্য

3MF হল একটি XML-ভিত্তিক ডেটা ফর্ম্যাট - মানব-পাঠযোগ্য সংকুচিত XML - এতে 3D উত্পাদন সম্পর্কিত ডেটার সংজ্ঞা রয়েছে, কাস্টম ডেটার জন্য তৃতীয়-পক্ষের এক্সটেনসিবিলিটি সহ। 3MF ফাইল ফরম্যাটটি অন্যান্য 3D ফাইল ফরম্যাটের সীমাবদ্ধতা এবং সমস্যার কথা মাথায় রেখে ডিজাইন করা হয়েছে। এটি 3MF ফাইল বিন্যাস গঠনের দিকে নিয়ে যায় যা হল:

* **সম্পূর্ণ:** একটি একক সংরক্ষণাগারে সমস্ত প্রয়োজনীয় মডেল, উপাদান এবং সম্পত্তির তথ্য রয়েছে

* **মানুষ পাঠযোগ্য:** উন্নয়ন সহজ করতে OPC, [ZIP](/compression/zip/), এবং XML এর মতো সাধারণ কাঠামো ব্যবহার করে

* **সহজ:** একটি সংক্ষিপ্ত, স্পষ্ট স্পেসিফিকেশন, উন্নয়নকে সহজ করে এবং দ্রুত বৈধতা দেয়

* **এক্সটেনসিবল:** এক্সএমএল নেমস্পেস ব্যবহার করে সামঞ্জস্য বজায় রেখে পাবলিক এবং প্রাইভেট উভয় এক্সটেনশনের অনুমতি দেয়

* **অস্পষ্ট:** পরিষ্কার ভাষা এবং কনফারমেন্স পরীক্ষা নিশ্চিত করে যে একটি ফাইল সর্বদা ডিজিটাল থেকে শারীরিক পর্যন্ত সামঞ্জস্যপূর্ণ

* **বিনামূল্যে:** 3MF স্পেসিফিকেশনের অ্যাক্সেস এবং বাস্তবায়ন সবসময় রয়্যালটি, পেটেন্ট এবং লাইসেন্সিং মুক্ত থাকবে


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF ফাইল ফরম্যাট স্পেসিফিকেশন

3MF ফাইল ফরম্যাট তার শারীরিক মডেলের জন্য জিপ আর্কাইভ আকারে ওপেন প্যাকেজিং স্পেসিফিকেশন ব্যবহার করে। এতে অংশ এবং সম্পর্কের একটি সু-সংজ্ঞায়িত সেট রয়েছে যা নথিতে বিশেষ উদ্দেশ্য পূরণ করে। এটি বিন্যাসটিকে ডিজিটাল স্বাক্ষর এবং থাম্বনেইল সহ প্যাকেজ বৈশিষ্ট্য অনুসরণ করে।

### 3MF ডকুমেন্ট - একটি ওভারভিউ

একটি সাধারণ 3MF নথি নিম্নরূপ দেখায়:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**নাম**|**বিবরণ**|**সম্পর্কের উত্স**|**প্রয়োজনীয়/ঐচ্ছিক**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|কোর প্রপার্টিজ
|ডিজিটাল সিগনেচার অরিজিন|ওপিসি অংশ যা প্যাকেজে ডিজিটাল স্বাক্ষরের মূল।
|ডিজিটাল স্বাক্ষর|OPC অংশগুলির প্রতিটিতে একটি ডিজিটাল স্বাক্ষর রয়েছে৷
|ডিজিটাল স্বাক্ষর শংসাপত্র|OPC অংশ যাতে একটি ডিজিটাল স্বাক্ষর শংসাপত্র থাকে।|ডিজিটাল স্বাক্ষর|ঐচ্ছিক
|প্রিন্টটিকেট|3D মডেল অংশে 3D বস্তু(গুলি) আউটপুট করার সময় ব্যবহার করার জন্য সেটিংস প্রদান করে
|থাম্বনেইল
|3D টেক্সচার|3D মডেল অংশে (এক্সটেনশনের জন্য উপলব্ধ)|3D মডেল|ঐচ্ছিক
|কাস্টম পার্টস|OPC অংশ যা মেটাডেটার সাথে যুক্ত|প্যাকেজ|ঐচ্ছিক

স্পেসিফিকেশন নথির [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) এবং [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) বিভাগগুলি 3MF নথি সম্পর্কে বিশদ তথ্য দেয়৷

## তথ্যসূত্র ##

* [3MF ফাইল ফর্ম্যাট স্পেসিফিকেশন](https://github.com/3MFConsortium/spec_core)

* [3MF - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


