{
  "date" : "2019-10-11",
  "keywords" : [ "qml file", "qml file format", "what is an qml file", "file", "qml example", "qml file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "QML - QGIS শৈলী ফাইল বিন্যাস",
  "description":"QML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি QML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## একটি QML ফাইল কি?

.qml এক্সটেনশন সহ একটি ফাইল হল একটি XML ফাইল যা QGIS স্তরগুলির জন্য লেয়ার স্টাইলিং তথ্য সংরক্ষণ করে। QGIS হল একটি ওপেন-সোর্স ক্রস-প্ল্যাটফর্ম GIS অ্যাপ্লিকেশন যা স্তরের আকারে ডেটা সংগঠিত করার ক্ষমতা সহ ভূ-স্থানিক ডেটা প্রদর্শন করতে ব্যবহৃত হয়। QML ফাইলগুলিতে এমন তথ্য রয়েছে যা QGIS দ্বারা প্রতীক সংজ্ঞা, আকার এবং ঘূর্ণন, লেবেলিং, অস্বচ্ছতা, ব্লেন্ড মোড এবং আরও অনেক কিছু সহ বৈশিষ্ট্য জ্যামিতি রেন্ডার করতে ব্যবহৃত হয়। QLR ফাইলগুলির বিপরীতে, QML ফাইলগুলি নিজেই সমস্ত স্টাইলিং তথ্য ধারণ করে। QML ফাইল যেকোন টেক্সট এডিটর যেমন Notepad++ এ খোলা যায়।

## QML ফাইল ফরম্যাট

QLR, [QGS](/gis/qgs/) এবং [QLR](/gis/qlr/) এর মতো, একটি XML ফাইল যাতে স্তরগুলির জন্য স্টাইলিং তথ্য রয়েছে৷

নীচের চিত্রটি একটি QML ফাইলের শীর্ষ স্তরের ট্যাগগুলি দেখায় (শুধুমাত্র renderer_v2 এবং এর প্রতীক ট্যাগ প্রসারিত)।

{{< figure src="../qml.png" title="" >}}

## তথ্যসূত্র

* [QGIS](https://www.qgis.org/en/site/)

* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

