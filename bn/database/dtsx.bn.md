{
  "date" : "2020-11-11",
  "keywords" : [ "DTSX", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DTSX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DTSX ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "DTSX ফাইল ফরম্যাট - SQL সার্ভার DTS সেটিংস ফাইল",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## একটি DTSX ফাইল কি?

.dtsx (ডেটা ট্রান্সফরমেশন সার্ভিসেস প্যাকেজ এক্সএমএল) এক্সটেনশন সহ একটি ফাইল হল একটি ডেটা ট্রান্সফরমেশন সার্ভিসেস (ডিটিএস) ফাইল যা মাইক্রোসফ্ট এসকিউএল ব্যবহার করে ডেটা মাইগ্রেশনের ধাপ/নিয়মগুলি এক ডাটাবেস থেকে অন্য ডাটাবেসে স্থানান্তর করার জন্য। এর মধ্যে রয়েছে রূপান্তর এবং যে কোনো ঐচ্ছিক প্রক্রিয়াকরণ পদক্ষেপ যা উৎপত্তিস্থল এবং গন্তব্য বিন্দুর মধ্যে ডেটা স্থানান্তরের সময় প্রয়োজন হতে পারে। SQL সার্ভার ইন্টিগ্রেশন সার্ভিসেস (SSIS), মাইক্রোসফ্ট SQL সার্ভারের একটি উপাদান, ডাটাবেস সার্ভারের মধ্যে ডেটা প্রক্রিয়াকরণের পদক্ষেপগুলি সনাক্ত করতে DTSX ফাইলগুলি ব্যবহার করে। DTSX ফাইলগুলি Microsoft SQL Server 2019 দিয়ে খোলা যাবে।

## DTSX ফাইল ফরম্যাট

এই অপারেশন চলাকালীন ডেটার অখণ্ডতা নিশ্চিত করতে ডাটাবেস সার্ভারের মধ্যে ডেটা চলাচলের নিয়ম এবং প্রক্রিয়াকরণের পদক্ষেপের প্রয়োজন। SSIS নিশ্চিত করে যে এই সমস্ত ক্রিয়াকলাপগুলি, একটি এন্টারপ্রাইজে বিভিন্ন উত্স থেকে ডেটা স্থানান্তর এবং সামঞ্জস্য করার জন্য, সুবিধাজনকভাবে সঞ্চালিত হয়। এখানেই DTSX আসে যা SSIS-এর দ্বারা ব্যবহার করা কাঠামোগুলিকে সংজ্ঞায়িত করে যেখানে এই ধাপগুলি অনুসরণ করে ডেটা প্রক্রিয়া করা যেতে পারে।

DTSX দ্বারা বর্ণিত ডেটা প্রবাহ নিম্নলিখিত ছবিতে দেখানো হয়েছে।

{{< figure src="../DataFlowDTSX.png" alt="ডেটা ফ্লো DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## তথ্যসূত্র

 * [DTSX ফর্ম্যাট - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2 ফর্ম্যাট - Microsoft দ্বারা](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

