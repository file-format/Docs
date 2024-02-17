{
  "date" : "2019-10-11",
  "keywords" : [ "u3d file", "u3d file format", "what is an u3d file", "file", "u3d example", "u3d file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "U3D - ইউনিভার্সাল 3D ফাইল ফরম্যাট",
  "description":"U3D ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা U3D ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## একটি U3D ফাইল কি?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/) নথিগুলি U3D অবজেক্ট এম্বেডিং সমর্থন করে এবং Adobe Reader এ দেখা যায় (সংস্করণ 7 এবং পরবর্তী)।

U3D ফরম্যাটটি ত্রিমাত্রিক ডেটা স্টোরেজ এবং বিনিময়ের জন্য একটি সর্বজনীন মান প্রতিষ্ঠার লক্ষ্যকে সামনে রেখে তৈরি করা হয়েছিল। যাইহোক, ফরম্যাটটি ইন্টারচেঞ্জ ফরম্যাট হিসাবে ব্যবহার করার পরিবর্তে 3D পিডিএফের জন্য এনকোডিংয়ে এর প্রধান ব্যবহার খুঁজে পায়। Acrobat 3D একটি সমর্থিত 3D ফাইল টাইপকে PDF এ রূপান্তর করার পরে U3D বা PRC তে রূপান্তর করে।

## U3D ফাইল ফরম্যাট

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

U3D এর প্রথম সংস্করণটি 3D গ্রাফিক্স বৈশিষ্ট্য যেমন জ্যামিতি, রঙ, টেক্সচার, আলো, হাড় এবং রূপান্তর-ভিত্তিক অ্যানিমেশনের মূল উপস্থাপনাগুলির উপর দৃষ্টি নিবদ্ধ করেছিল। দ্বিতীয় এবং তৃতীয় সংস্করণগুলি প্রথম সংস্করণে কিছু ত্রুটি-বিচ্যুতি সংশোধন করেছে, তৃতীয় সংস্করণটি শিল্প সফ্টওয়্যারে সর্বাধিক ব্যবহৃত প্রকার। চতুর্থ সংস্করণ উচ্চ-ক্রম আদিম (বাঁকা পৃষ্ঠ) জন্য সংজ্ঞা প্রদান করে। ECMA ওয়েবসাইটে ব্যবহারকারীর রেফারেন্সের জন্য [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) অনলাইনে উপলব্ধ৷

### U3D ফাইলে ডেটা টাইপ

বাইনারি ফাইলে নিম্নলিখিত প্রকারগুলি থাকবে: U8, U16, U32, U64, I16, I32, F32, F64 এবং স্ট্রিং।

 * U8 : একটি স্বাক্ষরবিহীন 8 বিট পূর্ণসংখ্যা
 * U16 : একটি স্বাক্ষরবিহীন 16 বিট পূর্ণসংখ্যা
 * U32 : একটি স্বাক্ষরবিহীন 32 বিট পূর্ণসংখ্যা
 * U64 : একটি স্বাক্ষরবিহীন 64 বিট পূর্ণসংখ্যা
 * I16 : একটি স্বাক্ষরিত 16 বিট পূর্ণসংখ্যা
 * F32: একটি IEEE একক নির্ভুলতা ফ্লোট।
 * F64: একটি IEEE ডাবল নির্ভুল ফ্লোট।
 * স্ট্রিং: একটি U3D ফাইলের স্ট্রিংগুলি একটি স্বাক্ষরবিহীন 16-বিট পূর্ণসংখ্যা দিয়ে শুরু হয় যা স্ট্রিংয়ের অক্ষরের মোট দৈর্ঘ্যকে সংজ্ঞায়িত করে। স্ট্রিং সবসময় কেস সংবেদনশীল হিসাবে প্রক্রিয়া করা হয়.

## U3D ফাইল স্ট্রাকচার

একটি U3D ফাইলে ব্লকের একটি ক্রম থাকে। প্রতিটি U3D ফাইলে 3টি ভিন্ন ধরনের ব্লক রয়েছে।

 * ফাইল হেডার ব্লক
 * ঘোষণা ব্লক
 * ধারাবাহিকতা ব্লক

লোডার একটি ব্লকের শেষ নির্ধারণ করে যদি সেই ব্লকের ডেটার প্রয়োজন না হয় বা যদি সেই ব্লকের প্রকারের জন্য একটি ডিকোডার উপলব্ধ না হয়।

{{< figure src="../u3d.png" alt="U3D ফাইল ফরম্যাট" >}}

### ফাইল হেডার ব্লক
একটি ফাইল হেডার ব্লকে ফাইলের তথ্য থাকে যা ফাইলটি কীভাবে পড়তে হয় তা নির্ধারণ করতে লোড দ্বারা ব্যবহৃত হয়।

### ঘোষণা ব্লক

ঘোষণা ব্লক ফাইলের বস্তু সম্পর্কে তথ্য ধারণ করে. একটি ঘোষণা ব্লকের বস্তুগুলিকে অবশ্যই সংজ্ঞায়িত করতে হবে।

### ধারাবাহিকতা ব্লক

একটি ঘোষণা ব্লকে ঘোষিত বস্তুর জন্য অতিরিক্ত তথ্য ধারাবাহিকতা ব্লকে প্রদান করা হয়। প্রতিটি ধারাবাহিকতা ব্লক অবশ্যই একটি ঘোষণা ব্লকের সাথে যুক্ত হতে হবে।


## তথ্যসূত্র ##

* [U3D ফাইল ফরম্যাট - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D ফাইল ফর্ম্যাট স্পেসিফিকেশন](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


