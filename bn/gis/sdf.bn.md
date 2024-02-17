{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF ফাইল - স্থানিক ডেটা বিন্যাস ফাইল",
  "description":"SDF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি SDF ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-bn",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## একটি SDF ফাইল কি?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. এটি স্থানিক তথ্যের বড় ডেটাসেটের জন্য একটি অপ্টিমাইজ করা ফাইল বিন্যাস হিসাবে বিবেচিত হয়।

আপনি Autodesk AutoCAD Map 3D 2022 এবং Autodesk AutoCAD Civil 3D 2023 ব্যবহার করে একটি SDF ফাইল খুলতে পারেন।

## SDF ফাইল ফরম্যাট - আরও তথ্য

SDF ফাইল ফরম্যাট বাইনারি ফাইল হিসাবে ডিস্কে সংরক্ষণ করা হয়। এটি SQLite ডাটাবেসের উপর ভিত্তি করে যা ডেটার বাইনারি সিরিয়ালাইজেশনের জন্য নিম্ন-স্তরের স্টোরেজ উপাদান ব্যবহার করে। একটি SDF ফাইলে ফাইল প্রতি একাধিক ফিচার ক্লাস এবং প্রতিটি ফিচার ক্লাসের জন্য একাধিক জ্যামিতি বৈশিষ্ট্য থাকে। একটি আর-ট্রি ব্যবহার করে প্রতিটি জ্যামিতি সম্পত্তির সূচীকরণের কারণে একটি SDF ফাইলের ডেটা উচ্চ গতিতে অ্যাক্সেসযোগ্য।

## তথ্যসূত্র

* [SDF ডেটা ফরম্যাট](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

