{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OAM ফাইল - Adobe Edge অ্যানিমেট উইজেট ফাইল ফরম্যাট",
  "description" : "একটি OAM ফাইল এবং APIগুলি কী যা OAM ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন।",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-bn",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## একটি OAM ফাইল কি?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
ব্যবহারকারীরা একটি এজ অ্যানিমেট প্রকল্প (.AN ফাইল) থেকে প্রকাশ করে OAM ফাইল তৈরি করতে পারে।

## OAM ফাইল ফরম্যাট

একটি OAM ফাইল সংকুচিত [ZIP](/compression/zip/) সংরক্ষণাগার হিসাবে ডিস্কে সংরক্ষিত হয়৷ এটি বোঝায় যে আপনি ফাইল এক্সটেনশনের নাম পরিবর্তন করে .zip করতে পারেন এবং WinZIP বা WinRAR-এর মতো যেকোনো কম্প্রেশন ইউটিলিটি দিয়ে এক্সট্রাক্ট করতে পারেন। ফাইলের আকার হ্রাস করার ফলে ইন্টারনেটে অন্যান্য ব্যবহারকারীদের সাথে অ্যানিমেশন স্থানান্তর এবং ভাগ করা সহজ হয়।

### OAM ফাইল স্ট্রাকচার

একটি .oam ফাইলের অভ্যন্তরীণ ফাইল কাঠামো মালিকানাধীন এবং Adobe দ্বারা সর্বজনীনভাবে নথিভুক্ত করা হয় না। যাইহোক, এটা জানা যায় যে .oam ফাইলগুলিতে ফাইল এবং সংস্থানগুলির (যেমন গ্রাফিক্স, অডিও এবং অ্যাকশনস্ক্রিপ্ট কোড) একটি একক ফাইলে প্যাকেজ করা থাকে। একটি .oam ফাইলের বিষয়বস্তুতে [XML](/web/xml/) ফাইল, SWF ফাইল এবং অন্যান্য রিসোর্স ফাইল থাকতে পারে। .oam ফাইলের সঠিক কাঠামো এটি তৈরি করতে ব্যবহৃত Adobe Animate-এর নির্দিষ্ট সংস্করণ, সেইসাথে ফাইলটিতে অন্তর্ভুক্ত অ্যানিমেশন এবং সম্পদের প্রকারের উপর নির্ভর করে।

একটি OAM ফাইলে নিম্নলিখিত তথ্য রয়েছে।

`সম্পদ:` অ্যানিমেশনে ব্যবহৃত গ্রাফিক্স, অডিও এবং ভিডিও সম্পদ সম্পর্কে তথ্য।

`আচরণ:` অ্যানিমেশনে ঘটে যাওয়া ক্রিয়া এবং মিথস্ক্রিয়াগুলির বর্ণনা।

`ActionScript কোড:` অ্যানিমেশনের আচরণ এবং ইন্টারঅ্যাক্টিভিটি নিয়ন্ত্রণ করতে ব্যবহৃত কোড।

`প্রকাশ সেটিংস:` যে প্ল্যাটফর্ম এবং বিন্যাসে অ্যানিমেশন প্রকাশ করা হবে সে সম্পর্কে তথ্য, যেমন HTML5 বা AIR৷

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## কিভাবে OAM ফাইল খুলবেন?

আপনি OAM ফাইল খুলতে নিম্নলিখিত অ্যাপ্লিকেশন ব্যবহার করতে পারেন।

 * Adobe Edge অ্যানিমেট CC (বন্ধ)
 * অ্যাডোব অ্যানিমেট 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## তথ্যসূত্র

* [OAM পাবলিশিং](https://helpx.adobe.com/animate/using/OAM-publishing.html)


