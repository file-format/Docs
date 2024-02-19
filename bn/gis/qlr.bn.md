{
  "date": "2019-10-11",
  "keywords": [
    "qlr file",
    "qlr file format",
    "what is an qlr file",
    "file",
    "qlr example",
    "qlr file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QLR - QGIS লেয়ার ডেফিনিশন ফাইল",
  "description": "QLR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা QLR ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "QLR",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qlr-bn"
    }
  },
  "lastmod": "2021-03-14"
}

## একটি QLR ফাইল কি?

.qlr এর সাথে একটি ফাইল হল একটি লেয়ার ডেফিনিশন ফাইল যাতে লেয়ার ডেটা সোর্সের একটি পয়েন্টার থাকে। এটি স্তরটির জন্য [QGIS](https://www.qgis.org/en/site/) শৈলী তথ্যের অতিরিক্ত। সমস্ত সম্পর্কিত শৈলীর রেফারেন্স থাকার কারণে, এই ফাইলটি স্টাইলিং তথ্য পাওয়ার জন্য ডেটা ব্যবহার করার জন্য একটি একক উত্স হিসাবে ব্যবহৃত হয়। QLR ফাইলগুলি ব্যবহার করে, ডেটা উত্সগুলির তথ্য এই একক ফাইলে রাখা যেতে পারে যা স্টাইলিং তথ্য লোড করার জন্য অন্যান্য অ্যাপ্লিকেশনগুলি পড়তে পারে। QLR ফাইল যেকোন টেক্সট এডিটর যেমন নোটপ্যাড++ দিয়ে খোলা যায়।

## QLR ফাইল ফরম্যাট

QLR, [QGS](/gis/qgs/)-এর মতো, একটি XML ফাইল যাতে XML ট্যাগ আকারে স্তর ডেটা উৎসের পয়েন্টার থাকে। এটি ArcGIS .lyr ফাইলের অনুরূপ। একটি QML ফাইলের শীর্ষ স্তরের ট্যাগগুলি নীচের ছবিতে দেখানো হয়েছে৷

{{< figure src="../qlr.png" title="" >}}

## তথ্যসূত্র

* [QGIS](https://www.qgis.org/en/site/)

* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

