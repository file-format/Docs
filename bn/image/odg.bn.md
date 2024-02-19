{
  "date": "2019-10-11",
  "keywords": [
    "odg file",
    "odg file format",
    "what is an odg file",
    "file",
    "odg example",
    "odg file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ODG ফাইল ফরম্যাট",
  "description": "ODG ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি ODG ফাইল তৈরি করতে এবং খুলতে পারে৷",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-odg-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি ODG ফাইল কি?

ODG ফাইল ফরম্যাট Apache OpenOffice-এর ড্র অ্যাপ্লিকেশন দ্বারা ভেক্টর ইমেজ হিসাবে অঙ্কন উপাদানগুলিকে সংরক্ষণ করতে ব্যবহৃত হয়। এটি অ্যাডভান্সমেন্ট অফ স্ট্রাকচারাল ইনফরমেশন স্ট্যান্ডার্ডস (ওএএসআইএস) দ্বারা বর্ণিত XML ভিত্তিক ফাইল ফর্ম্যাট স্পেসিফিকেশন অনুসরণ করে। ODG পয়েন্ট, রেখা এবং বক্ররেখা ব্যবহার করে ভেক্টর ইমেজ হিসাবে অঙ্কনকে উপস্থাপন করে। OpenOffice ছাড়াও LibreOffice এবং অন্যান্য অ্যাপ্লিকেশনগুলি ওডিজি ফাইল ফরম্যাটের সাথে কাজ করার জন্য সমর্থন প্রদান করে। OpenOffice দ্বারা সমর্থিত অন্যান্য ফরম্যাট, উদাহরণস্বরূপ, [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) এবং [ODS](/spreadsheet/ods/) অন্তর্ভুক্ত।


## ODG ফাইল ফরম্যাট স্পেসিফিকেশন

ODG ফাইল ফরম্যাট OpenDocument ফরম্যাটের উপর ভিত্তি করে যা সুসংজ্ঞায়িত স্কিমা সহ স্ট্রাকচার্ড XML ডকুমেন্ট ফরম্যাট।
একটি OpenDocument ফরম্যাটের প্রতিটি কাঠামোগত উপাদান একটি উপাদান দ্বারা উপস্থাপিত হয় যা সম্পর্কিত বৈশিষ্ট্য রয়েছে। XML ভিত্তিক কাঠামো সব ধরনের নথির জন্য সাধারণ যেমন টেক্সট নথি, স্প্রেডশীট বা অঙ্কন ফাইল। একটি নথিতে বিভিন্ন শৈলী থাকতে পারে। একটি OpenDocument ফাইল স্ট্রাকচার নিম্নলিখিত উপাদান নিয়ে গঠিত।
  * ডকুমেন্ট রুট
  * নথি মেটাডেটা
  * বডি এলিমেন্ট এবং ডকুমেন্টের ধরন
  * আবেদন নির্ধারণ
  * স্ক্রিপ্ট
  * ফন্ট ফেস ঘোষণা
  * শৈলী
  * পৃষ্ঠা শৈলী এবং বিন্যাস

##  নথির মূল ##

একটি নথির মূল উপাদান সম্পূর্ণ নথি ধারণ করে এবং OpenDocument বিন্যাসে একটি ফাইলের প্রাথমিক উপাদান। একই ধরণের নথির মূল উপাদানগুলি সমস্ত ধরণের নথিতে যেমন পাঠ্য, নথি, স্প্রেডশীট এবং অঙ্কন নথিতে প্রযোজ্য।

### মূল উপাদান ###
একটি একক XML নথির নিজস্ব মূল উপাদান দ্বারা প্রতিনিধিত্ব করা হয়। পাঁচটি ভিন্ন সমর্থিত মূল উপাদান নিম্নরূপ।

`<office:document> ` - একটি একক এক্সএমএল নথিতে সম্পূর্ণ অফিস নথি।
`<office:document-content> ` - বিষয়বস্তুতে ব্যবহৃত নথির বিষয়বস্তু এবং স্বয়ংক্রিয় শৈলী।
`<office:document-styles> ` - নথির বিষয়বস্তুতে ব্যবহৃত শৈলী এবং শৈলীতে ব্যবহৃত স্বয়ংক্রিয় শৈলী।
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - অ্যাপ্লিকেশন-নির্দিষ্ট সেটিংস, যেমন উইন্ডোর আকার বা প্রিন্টার তথ্য।

### ODG নথি মেটাডেটা ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### বডি এলিমেন্ট এবং ডকুমেন্টের ধরন ###
ডকুমেন্ট বডি ডকুমেন্ট টাইপ এলিমেন্ট ব্যবহার করে ডকুমেন্টে থাকা বিষয়বস্তুর ধরন নির্দেশ করে। এই নথির প্রকারগুলি হল:
  * পাঠ্য নথি
  * অঙ্কন নথি
  * উপস্থাপনা নথি
  * স্প্রেডশীট নথি
  * চার্ট নথি
  * ছবি নথি

### আবেদন নির্ধারণ ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * ডকুমেন্ট সেটিংস যেমন ডিফল্ট প্রিন্টার
  * সেটিংস দেখুন যেমন জুম লেভেল

### স্ক্রিপ্ট ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### ফন্ট ফেস ঘোষণা ###

একটি ফন্ট ফেস ঘোষণায় একটি নথির লেখক দ্বারা ব্যবহৃত ফন্ট সম্পর্কে তথ্য রয়েছে। এই তথ্য অন্যান্য সিস্টেমে এই ফন্টগুলি সনাক্ত করতে সাহায্য করে।
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### শৈলী ###
নিম্নলিখিত শৈলী OpenDocument বিন্যাস দ্বারা সমর্থিত.

সাধারণ শৈলী' - এই ধরনের শৈলীগুলির XML উপস্থাপনাগুলিকে শৈলী হিসাবে উল্লেখ করা হয়
`স্বয়ংক্রিয় শৈলী` - ফর্ম্যাটিং বৈশিষ্ট্যগুলি ধারণ করে যেগুলি, একটি নথির ব্যবহারকারী ইন্টারফেস ভিউতে, একটি অনুচ্ছেদের মতো একটি বস্তুকে বরাদ্দ করা হয়৷
`মেটার শৈলী` - একটি সাধারণ শৈলী যাতে বিন্যাস তথ্য এবং অতিরিক্ত সামগ্রী থাকে যা নথির বিষয়বস্তুর সাথে প্রদর্শিত হয় যখন শৈলী প্রয়োগ করা হয়। একটি মাস্টার শৈলী একটি উদাহরণ মাস্টার পেজ হয়.

## তথ্যসূত্র ##
  * [অফিস অ্যাপ্লিকেশনের জন্য OASIS ওপেন ডকুমেন্ট ফরম্যাট](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [ওপেন ডকুমেন্ট ফরম্যাট - উইকিপিডিয়া](https://en.wikipedia.org/wiki/OpenDocument)

