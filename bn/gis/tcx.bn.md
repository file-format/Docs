{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX ফাইল ফরম্যাট- প্রশিক্ষণ কেন্দ্র XML ফাইল",
  "description":"TCX ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি TCX ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-bn",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## একটি TCX ফাইল কি?

একটি TCX (প্রশিক্ষণ কেন্দ্র XML) ফাইল হল একটি ডেটা বিনিময় ফর্ম্যাট যা ফিটনেস ডিভাইসগুলির মধ্যে ডেটা ভাগ করতে ব্যবহৃত হয়। এটি 2008 সালে গারমিন'স ট্রেনিং সেন্টার পণ্যের সাথে চালু করা হয়েছিল। হার্ট রেট, রানিং ক্যাডেন্স, সাইকেলের ক্যাডেন্স, ক্যালোরি এবং ল্যাপ টাইমের মতো ওয়ার্কআউট ডেটা TCX ফাইলের মধ্যে [XML](/web/xml/) ফর্ম্যাটে সংরক্ষণ করা হয়। এছাড়াও, ওয়ার্কআউট ট্র্যাক সম্পর্কে সারাংশ ডেটাও TCX ফাইলে অন্তর্ভুক্ত করা হয়েছে। TCX ফাইলগুলি [FIT](/gis/fit/) ফাইলগুলির মতো যা গার্মিন স্পোর্টস পরিধানযোগ্য ডিভাইসগুলির সাথে তৈরি করা হয়৷

## TCX ফাইল ফরম্যাট - আরও তথ্য

TCX ফাইলগুলিকে XML ফাইল হিসাবে ডিস্কে সংরক্ষিত করা হয় এবং প্রতিটি রেকর্ড একটি কার্যকলাপ হিসাবে সংরক্ষিত হয়। একটি ক্রিয়াকলাপে একটি ওয়ার্কআউটের সমস্ত ডেটা থাকে যেমন সময়, ল্যাপ টাইম, আইডি, হার্ট-রেট, তীব্রতা, ক্যাডেন্স এবং ট্র্যাক তথ্য যা {{HYPERLINK1 এর অনুরূপ ল্যাট-লং অবস্থানের জন্য টাইমস্ট্যাম্প সহ অবস্থানের জোড়া রয়েছে }} নথি পত্র.

### TCX ফাইল ফরম্যাট সংস্করণ

গারমিন দ্বারা হোস্ট করা নিজস্ব XML স্কিমা সহ এই বিন্যাসের দুটি সংস্করণ রয়েছে। তাদের মধ্যে কয়েকটি নিম্নরূপ:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX ডেটা প্রোটোকল

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## তথ্যসূত্র ##

* [প্রশিক্ষণ কেন্দ্র XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX ভিউয়ার](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


