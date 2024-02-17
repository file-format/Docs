{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW - ভিজিও গ্রাফিক্স সার্ভিস ফাইল ফরম্যাট",
  "description":"VDW ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা VDW ফাইলগুলি তৈরি এবং খুলতে পারে।",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-bn",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## একটি VDW ফাইল কি?

VDW হল ভিজিও গ্রাফিক্স সার্ভিস ফাইল ফরম্যাট যা ওয়েব ড্রয়িং রেন্ডার করার জন্য প্রয়োজনীয় স্ট্রিম এবং স্টোরেজ নির্দিষ্ট করে। একটি ওয়েব অঙ্কন হল অঙ্কন পৃষ্ঠা, আকার, ফন্ট, চিত্র, ডেটা সংযোগ এবং ডায়াগ্রাম আপডেট তথ্যের একটি সংগ্রহ যা একটি ভেক্টর বা রাস্টার অঙ্কন হিসাবে রেন্ডার করা যেতে পারে। VDW ফাইলগুলি মাইক্রোসফ্ট ভিসিওতেও খোলা যেতে পারে তবে প্রাথমিকভাবে ওয়েবে ব্যবহারের জন্য সংরক্ষণ করা হয়। মাইক্রোসফ্ট ভিসিও ভিসিও ফাইলগুলিকে [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) এবং অন্যান্য সহ বিভিন্ন ফাইল ফর্ম্যাটে রূপান্তর করার ক্ষমতা প্রদান করে৷

## **VDW** ফাইল ফরম্যাট

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|![Possible Implementation of a File](/web/vdw.png "Possible Implementation of a File")

## তথ্যসূত্র

* [[MS-VGSFF]: ভিজিও গ্রাফিক্স সার্ভিস (.vdw) ফাইল ফরম্যাট](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


