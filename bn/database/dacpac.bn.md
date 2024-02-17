{
  "date" : "2021-09-06",
  "keywords" : [ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DACPAC ফাইল ফরম্যাট এবং APIগুলি সম্পর্কে জানুন যা DACPAC ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title" : "DACPAC - ডেটা টিয়ার অ্যাপ্লিকেশন প্যাকেজ",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## একটি DACPAC ফাইল কি?

.dacpac (ডেটা টিয়ার অ্যাপ্লিকেশান প্যাকেজ) এক্সটেনশন সহ একটি ফাইল হল একটি ডাটাবেস ফাইল, যা মাইক্রোসফ্ট এসকিউএল সার্ভার ডেটা টিয়ার অ্যাপ্লিকেশনের সাহায্যে তৈরি করা হয়েছে, যেটিতে ডেটাবেস অবজেক্টের উপস্থাপনার জন্য ডাটাবেস মডেল রয়েছে। যেহেতু এটি ডাটাবেসের সম্পূর্ণ মডেল ধারণ করে, এটি মডেলে উপলব্ধ বিবরণ থেকে একটি ডাটাবেস পুনরুদ্ধার করতে ব্যবহৃত হয়। DACPAC ফাইলগুলি সাধারণত ডেটাবেস পুনরুদ্ধার করার জন্য গ্রাহকের প্রাঙ্গনে ইনস্টলেশনের জন্য স্থাপনার দলগুলির কাছে হস্তান্তর করা হয়। এগুলো দিয়ে খোলা যাবে
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019)

## DACPAC ফাইল ফরম্যাট - আরও তথ্য

DACPAC ডেটা প্যাকেজ ফাইলগুলি আসলে কম্প্রেস করা জিপ ফাইল যাতে ডাটাবেস মডেল সম্পর্কে তথ্য রয়েছে, যেমন টেবিল এবং ভিউ, একটি ডাটাবেস পুনরুদ্ধার করতে ব্যবহৃত হয়। DACPAC ফাইলগুলির বিষয়বস্তু দেখার জন্য, ফাইলগুলির নাম .dacpac থেকে [.zip](/compression/zip/) এ পুনঃনামকরণ করুন এবং যেকোনো ডিকম্প্রেশন ইউটিলিটি ব্যবহার করে জিপ সংরক্ষণাগারটি বের করুন৷

নিম্নলিখিত কয়েকটি ফাইল রয়েছে যা একটি DACPAC ফাইলের মধ্যে পাওয়া যায়।

 * [Content_Types].xml
```
<?xml version=1.0 encoding=utf-8?>
<Types
xmlns=http://schemas.openxmlformats.org/package/2006/content-types>
<Default Extension=xml ContentType=text/xml />
</Types>
```
 * DacMetadata.xml

```
<?xml version=1.0 encoding=utf-8?>
<DacType xmlns=http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02>
<Name>সিআরএম</Name>
<Version>1.0.0.0</Version>
</DacType>
```
 * Origin.xml

 * model.xml

উল্লেখ্য যে DACPAC-এ DATA এবং অন্যান্য সার্ভার-স্তরের বস্তু থাকে না। ফাইলটিতে সমস্ত বস্তুর ধরন থাকতে পারে যা SSDT প্রকল্পে রাখা যেতে পারে।

## তথ্যসূত্র

* [ডেটা টিয়ার অ্যাপ্লিকেশন - সুবিধাগুলি](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [একটি ডেটা টিয়ার অ্যাপ্লিকেশন স্থাপন করা হচ্ছে - মাইক্রোসফ্ট](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
