{
  "date" : "2020-11-11",
  "keywords" : [ "ACCDT", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : "ACCDT ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা ACCDT ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "ACCDT - Microsoft Access 2007 টেমপ্লেট ডাটাবেস ফাইল ফরম্যাট",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## একটি ACCDT ফাইল কি?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT ফাইল ফরম্যাট

ACCDT টেমপ্লেট ফাইলগুলি অফিস ওপেন XML স্পেসিফিকেশনের উপর ভিত্তি করে এবং সমস্ত ডেটা একটি জিপ প্যাকেজে থাকে। ডাটাবেসের কাঠামো এবং বিষয়বস্তু তথ্য [XML](/web/xml/) ফাইল এবং পাঠ্য ফাইলগুলিতে রয়েছে এবং সম্পর্কের মাধ্যমে একে অপরের সাথে লিঙ্ক করা হয়েছে। আপনি একটি ACCDT ফাইলকে [.zip](/compression/zip/) এক্সটেনশনে পুনঃনামকরণ করতে পারেন এবং জিপ আর্কাইভের বিষয়বস্তু বের করতে যেকোনো কম্প্রেশন সফ্টওয়্যার ব্যবহার করতে পারেন৷

### ফাইল স্ট্রাকচার

ACCDT ফাইলগুলি এমন প্যাকেজ যা সম্পর্কিত অংশগুলির একটি সংগ্রহ ধারণ করে। প্রতিটি **অংশ** XML, পাঠ্য এবং বাইনারি বিন্যাস ব্যবহার করে একটি ডাটাবেস অ্যাপ্লিকেশনের বিষয়বস্তু সম্পর্কে তথ্য সঞ্চয় করে, যার মধ্যে রয়েছে:

 * ডাটাবেস অবজেক্ট
 * সংশ্লিষ্ট মেটাডেটা
 * প্যাকেজের গঠন

#### প্যাকেজ

একটি প্যাকেজ হল একটি [ZIP](/compression/zip/) সংরক্ষণাগার যাতে একাধিক অংশ থাকে এবং [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html)-এ উল্লেখিত ওপেন প্যাকেজিং কনভেনশনগুলির সাথে সামঞ্জস্যপূর্ণ৷ ACCDT ফাইলগুলিতে কমপক্ষে একটি টেমপ্লেট মেটাডা অংশ থাকতে হবে যা একটি সম্পর্কের লক্ষ্য হওয়া উচিত। এই টেমপ্লেট মেটাডেটা হল একটি ACCDT ফাইলের শুরুর অংশ।

#### অংশ

একটি অংশ হল বাইটের একটি স্ট্রীম যার মধ্যে সংরক্ষিত বিষয়বস্তুর প্রকৃতি এবং ধরন উল্লেখ করার জন্য একটি সংশ্লিষ্ট প্রকার রয়েছে। অংশ গণনা বৈধ অংশ, বৈধ বিষয়বস্তুর প্রকার, এবং একটি প্যাকেজের সমস্ত অংশের মধ্যে প্রয়োজনীয় সম্পর্ক নির্দিষ্ট করে।

#### সম্পর্ক

প্যাকেজ রিলেশনশিপ' - যেখানে লক্ষ্য হল একটি অংশ এবং উৎস হল পুরো প্যাকেজ৷

`পার্ট-টু-পার্ট রিলেশনশিপ` - যেখানে লক্ষ্য একটি অংশ এবং উত্সটি প্যাকেজের একটি অংশ।

`স্পষ্ট সম্পর্ক` - যেখানে কোনো সম্পদকে কোনো উৎসের অংশের বিষয়বস্তু থেকে তার আইডি অ্যাট্রিবিউটের মান দ্বারা কোনো সম্পর্ক উপাদানকে উল্লেখ করে উল্লেখ করা হয়।

অন্তর্নিহিত সম্পর্ক' - একটি সম্পর্ক যা স্পষ্ট নয়।

`অভ্যন্তরীণ সম্পর্ক` - যেখানে লক্ষ্য প্যাকেজের একটি অংশ।

`বাহ্যিক সম্পর্ক` - যেখানে লক্ষ্য হল একটি বাহ্যিক সম্পদ যা প্যাকেজে নেই।

## তথ্যসূত্র ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

