{
  "date" : "2019-12-16",
  "keywords" : [ "OTS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "OTS ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি OTS ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "OTS - OpenDocument Spreadsheet টেমপ্লেট ফাইল ফরম্যাট",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## একটি OTS ফাইল কি?

.ots এক্সটেনশন সহ একটি ফাইল হল একটি OpenDocument স্প্রেডশীট টেমপ্লেট ফাইল যা Apache OpenOffice-এ অন্তর্ভুক্ত Calc অ্যাপ্লিকেশন সফ্টওয়্যার দিয়ে তৈরি করা হয়। ক্যালক অ্যাপ্লিকেশন সফ্টওয়্যার মাইক্রোসফ্ট অফিসে উপলব্ধ এক্সেলের অনুরূপ। OTS ফাইল ফরম্যাট টেমপ্লেট তৈরি করতে ব্যবহৃত হয় যাতে শৈলী, ফন্ট, ডেটা, স্প্রেডশীট লেআউট এবং বিন্যাস সম্পর্কিত পূর্বনির্ধারিত সেটিংস রয়েছে। OTF ফাইলে `mime-type application/vnd.oasis.opendocument.spreadsheet-template` আছে। এই টেমপ্লেট ফাইলগুলিকে [ODS file format](/spreadsheet/ods/)-এ সংরক্ষিত প্রকৃত ডেটা ফাইলগুলি তৈরি এবং সংরক্ষণ করার জন্য একটি সূচনা পয়েন্ট হিসাবে ব্যবহার করা যেতে পারে৷ ওটিএস ফাইলগুলি OpenOffice এবং LibreOffice এর মতো অ্যাপ্লিকেশনগুলির সাথে ব্যবহার করা যেতে পারে।

## OTS ফাইল ফরম্যাট

OTS ফাইলগুলি OASIS-এর OpenDocument XML-ভিত্তিক ফাইল ফর্ম্যাটে সংরক্ষিত হয় যা একটি [ZIP](/compression/zip/) সংরক্ষণাগার হিসাবে একটি প্যাকেজ সহ বেশ কয়েকটি সাব ডকুমেন্টের একটি সংগ্রহ নিয়ে গঠিত। প্রতিটি জিপ আর্কাইভ সম্পূর্ণ নথির অংশ সঞ্চয় করে এবং প্রতিটি সাব ডকুমেন্ট নথির একটি বিশেষ দিক সংরক্ষণ করে। উদাহরণস্বরূপ, একটি সাবডকুমেন্টে শৈলীর তথ্য থাকে এবং অন্য একটি সাবডকুমেন্টে নথির বিষয়বস্তু থাকে। একটি সাধারণ ODF নথিতে নিম্নলিখিত উপাদান রয়েছে:

### OTS Content.xml

content.xml ফাইলে নথির প্রকৃত বিষয়বস্তু থাকে। এটি যদিও বাইনারি ডেটা যেমন ইমেজ অন্তর্ভুক্ত করে না।
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS ফাইল ফরম্যাটের Styles.xml

styles.xml ফাইলে স্টাইলিং তথ্য রয়েছে এবং এটি ফরম্যাটিং এবং লেআউটের জন্য ব্যাপকভাবে ব্যবহৃত হয়। শৈলীর প্রকারগুলি অন্তর্ভুক্ত:

 * অনুচ্ছেদের শৈলী
 * পৃষ্ঠা শৈলী
 * চরিত্র শৈলী
 * ফ্রেমের শৈলী
 * শৈলী তালিকা

### Meta.xml

meta.xml ফাইলটিতে ফাইলের মেটাডেটা সম্পর্কে তথ্য থাকে যেমন লেখক, শেষ পরিবর্তিত তারিখ ইত্যাদি।
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

`settings.xml` ফাইলে ডকুমেন্ট লেভেল সেটিংস যেমন জুম ফ্যাক্টর এবং কার্সার পজিশন অন্তর্ভুক্ত থাকে।

## তথ্যসূত্র ##

* [OpenDocument 1.2 স্পেসিফিকেশন](https://www.oasis-open.org/standards#opendocumentv1.2)

* [ওপেন ডকুমেন্ট - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/OpenDocument)


