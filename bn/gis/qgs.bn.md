{
  "date" : "2019-10-11",
  "keywords" : [ "qgs file", "qgs file format", "what is a qgs file", "file", "qgs example", "qgs file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "QGS - QGIS প্রকল্প ফাইল বিন্যাস",
  "description":"QGS ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি QGS ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## একটি QGS ফাইল কি?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS ফাইল ফরম্যাট

QGS ফাইলগুলি [XML](/web/xml/) ফর্ম্যাটে থাকে এবং XML ট্যাগ হিসাবে প্রকল্পের ডেটা সঞ্চয় করে৷ একটি QGS ফাইলে তথ্য রয়েছে যেমন:

 * প্রকল্প শিরোনাম
 * প্রকল্প সিআরএস
 * স্তর গাছ
 * স্ন্যাপিং সেটিংস
 * সম্পর্ক
 * মানচিত্র ক্যানভাস ব্যাপ্তি
 * প্রকল্প মডেল
 * কিংবদন্তি
 * ম্যাপভিউ ডক (2D এবং 3D)
 * অন্তর্নিহিত ডেটাসেটগুলির লিঙ্ক সহ স্তরগুলি (ডেটা উত্স) এবং ব্যাপ্তি, এসআরএস, যোগদান, শৈলী, রেন্ডারার, ব্লেন্ড মোড, অপাসিটি এবং আরও অনেক কিছু সহ অন্যান্য স্তর বৈশিষ্ট্য।
 * প্রকল্প বৈশিষ্ট্য

### QGS টপ লেভেল এক্সএমএল ট্যাগ

{{< figure src="../qgstoplevel.png" title="" >}}

### সম্প্রসারিত টপ লেভেল প্রজেক্ট লেয়ার ট্যাগ

{{< figure src="../qgstoplevel.png" title="" >}}

## তথ্যসূত্র

* [QGIS](https://www.qgis.org/en/site/)


