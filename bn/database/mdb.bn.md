{
  "date": "2020-11-11",
  "keywords": [
    "MDB",
    "extension",
    "file",
    "file format",
    "Database File Type",
    "Database File Format",
    "Database Files"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "MDB ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি MDB ফাইল তৈরি এবং খুলতে পারে৷",
  "title": "MDB ফাইল ফরম্যাট - একটি Microsoft Access Database ফাইল",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-mdb-bn"
    }
  },
  "lastmod": "2020-11-11"
}

## একটি MDB ফাইল কি?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. Microsoft Access-এর পাশ্বর্ীয় সংস্করণগুলি [ACCDB](/database/accdb/) ফাইল বিন্যাস ব্যবহার করে যা এখন পর্যন্ত সর্বশেষ ফাইল বিন্যাস। MDB ফাইলগুলি Microsoft Access, MDB Viewer, MDBOpener-এর মতো অ্যাপ্লিকেশন দিয়ে খোলা যেতে পারে এবং ACCDB, [CSV](/spreadsheet/csv/), এক্সেল ফর্ম্যাট ইত্যাদিতে রূপান্তরিত করা যেতে পারে।

## MDB ফাইল ফরম্যাট

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### পৃষ্ঠা

অনানুষ্ঠানিক MDB গাইড অনুসারে, একটি MDB ফাইলে নির্দিষ্ট-আকারের পৃষ্ঠা থাকে (Jeb DB3 এর জন্য 2048 বাইট এবং Jet DB 4 এর জন্য 4096 বাইট)। প্রথম বাইট পৃষ্ঠার ধরন নির্দেশ করে। নিম্নলিখিত মূল পৃষ্ঠার প্রকারগুলি রয়েছে:

`প্রথম পৃষ্ঠা:` এতে ডাটাবেস হেডার তথ্য রয়েছে যা জেট ডিবি সংস্করণের সনাক্তকরণও অন্তর্ভুক্ত করে যার সাথে ফাইলটি সামঞ্জস্যপূর্ণ। উপরন্তু, এটি ফাইল নিরাপত্তা তথ্য এবং পৃষ্ঠা ব্যবহারের একটি মানচিত্র অন্তর্ভুক্ত করে।

`সারণী সংজ্ঞা পৃষ্ঠা:` একটি টেবিল সংজ্ঞা পৃষ্ঠা কলাম, ডেটা প্রকার, সূচক এবং অন্যান্য তথ্য নির্দিষ্ট করে। প্রয়োজনে এটি অতিরিক্ত পৃষ্ঠাগুলি ব্যবহার করে এবং এই টেবিলের জন্য সারি ডেটা ধারণ করে এমন পৃষ্ঠাগুলির একটি মানচিত্র অন্তর্ভুক্ত করে।

`ডেটা পেজ:` ডাটা পেজ হলো প্রকৃত ডাটা কন্টেনার যেখানে ডাটা সারি দ্বারা সংরক্ষণ করা হয়। এটি দীর্ঘ ডেটা মান সংরক্ষণ করতে সহায়ক পৃষ্ঠাগুলি ব্যবহার করে।

একটি একক Microsoft Access ডাটাবেস একাধিক ফাইল নিয়ে গঠিত হতে পারে যা ফাইল এবং টেবিলের আকারের সীমাবদ্ধতা অতিক্রম করতে দেয়। এটি ব্যবহারকারীর ডেস্কটপে ফ্রন্ট-এন্ড MDB ফাইলে ফর্ম এবং কোড এবং নেটওয়ার্কের সাথে সংযুক্ত সার্ভারে অন্য ব্যাকএন্ড MDB ফাইলগুলিতে ডেটা রাখার সুবিধা দেয়৷

## তথ্যসূত্র ##

* [অ্যাক্সেস স্পেসিফিকেশন](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
