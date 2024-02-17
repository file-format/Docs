{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ONETOC2 - Microsoft OneNote ফাইল ফরম্যাট",
  "description":"ONETOC2 ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা ONETOC2 ফাইল তৈরি করতে এবং খুলতে পারে।",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2 কি? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

আপনি যখন OneNote 2016-এ একটি নোটবুক তৈরি করেন, তখন এটি স্বয়ংক্রিয়ভাবে নতুন 2010-2016 ফাইল ফর্ম্যাটে সংরক্ষিত হয়৷ আপনি যদি OneNote 2016-এর সমস্ত বৈশিষ্ট্য যেমন গণিত সমীকরণ এবং লিঙ্কযুক্ত নোটগুলি সঠিকভাবে কাজ করতে চান তবে আপনার এই বিন্যাসের প্রয়োজন হবে৷

## ONETOC2 ফাইল ফরম্যাট ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### ফাইল স্ট্রাকচার ###

একটি রিভিশন স্টোর ফাইল একটি **হেডার** কাঠামো দিয়ে শুরু হওয়া আবশ্যক। ফাইলের অবশিষ্ট অংশটি বাইটের ব্লকে বিভক্ত করা হয়, যেখানে প্রতিটি ব্লকের আকার এবং গঠন ক্ষেত্র দ্বারা নির্দিষ্ট করা হয় যা এটিকে উল্লেখ করে। একটি ব্লক পৌঁছানো যায় যদি এটি **শিরোনাম** কাঠামোর দ্বারা উল্লেখ করা হয়, অথবা যদি এটি অন্য একটি পৌঁছানোর যোগ্য ব্লকের একটি ক্ষেত্র দ্বারা উল্লেখ করা হয়। **শিরোনাম** কাঠামোর বাইরের ডেটা এবং যেকোনও পৌঁছানো যায় এমন ব্লক অবশ্যই উপেক্ষা করা উচিত।

সমস্ত কাঠামো 1-বাইটের সীমানায় সারিবদ্ধ। অন্যথায় নির্দিষ্ট না হলে সমস্ত পূর্ণসংখ্যা স্বাক্ষরিত হয়। সমস্ত ক্ষেত্র হল [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) যদি না অন্যথায় নির্দিষ্ট করা হয়৷

#### হেডার ####

.ONE ফাইলের শিরোনামটি এমন খণ্ডগুলি নিয়ে গঠিত যাতে ফাইলের তথ্য উপস্থাপনের জন্য বিভিন্ন অনন্য আইডি এবং ক্ষেত্র রয়েছে:

`guidFileType (16 bytes):` একটি GUID যা রিভিশন স্টোর ফাইলের ধরন নির্দিষ্ট করে। নিম্নলিখিত সারণী থেকে মানগুলির মধ্যে একটি হতে হবে৷

|ফাইল বিন্যাস|মান
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` একটি GUID যা এই রিভিশন স্টোর ফাইলের পরিচয় নির্দিষ্ট করে। বিশ্বব্যাপী অনন্য হতে হবে.

`guidLegacyFileVersion (16 বাইট):` অবশ্যই {00000000-0000-0000-0000-000000000000} হতে হবে এবং অবশ্যই উপেক্ষা করা উচিত।

`guidFileFormat (16 বাইট):` একটি GUID যা নির্দিষ্ট করে যে ফাইলটি একটি রিভিশন স্টোর ফাইল। {109ADD3F-911B-49F5-A5D0-1791EDC8AED8} হতে হবে।

`ffvLastCodeThatWroteToThisFile (4 বাইট):` একটি স্বাক্ষরবিহীন পূর্ণসংখ্যা। ফাইলের প্রকারের উপর নির্ভর করে নিম্নলিখিত টেবিলের মানগুলির মধ্যে একটি হতে হবে।

|ফাইল বিন্যাস|মান
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 বাইট):` একটি স্বাক্ষরবিহীন পূর্ণসংখ্যা। এই ফাইলের ফাইল ফর্ম্যাটের উপর নির্ভর করে নিম্নলিখিত টেবিলের মানগুলির মধ্যে একটি হতে হবে৷


|ফাইল বিন্যাস|মান
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 বাইট):` একটি স্বাক্ষরবিহীন পূর্ণসংখ্যা। এই ফাইলের ফাইল ফর্ম্যাটের উপর নির্ভর করে নিম্নলিখিত টেবিলের মানগুলির মধ্যে একটি হতে হবে৷
:


|ফাইল বিন্যাস|মান
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 বাইট):` একটি স্বাক্ষরবিহীন পূর্ণসংখ্যা। এই ফাইলের ফাইল ফর্ম্যাটের উপর নির্ভর করে নিম্নলিখিত টেবিলের মানগুলির মধ্যে একটি হতে হবে৷


|ফাইল বিন্যাস|মান
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## তথ্যসূত্র ##

* [[MS-ONESTORE] - OneNote ফাইল ফরম্যাট](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [মাইক্রোসফ্ট ওয়ান নোট - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


