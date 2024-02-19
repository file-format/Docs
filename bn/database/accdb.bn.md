{
  "date": "2020-11-11",
  "keywords": [
    "ACCDB",
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
  "description": "ACCDB ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি ACCDB ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title": "ACCDB ফাইল ফরম্যাট - Microsoft Access 2007 ডাটাবেস ফাইল",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accdb-bn"
    }
  },
  "lastmod": "2020-11-12"
}

## একটি ACCDB ফাইল কি?

.accdb এক্সটেনশন সহ একটি ফাইল হল একটি Microsoft Access 2007 ডাটাবেস ফাইল যা ব্যবহারকারীদের ডেটা টেবিলে সংরক্ষণ করে। এটি সংরক্ষণ সমর্থন করে
কাস্টম ফর্ম, SQL কোয়েরি, এবং অন্যান্য ডেটা। Microsoft XML ভিত্তিক ফাইল কাঠামোতে স্থানান্তরিত হওয়ার পর ACCDB ফাইলগুলি [MDB](/database/mdb/) ফাইলগুলিকে প্রতিস্থাপন করেছে৷ ACCDB ফাইলগুলি এখনও পুরানো সামঞ্জস্যের সাথে MDB তে রূপান্তর করা যেতে পারে। যাইহোক, ACCDB এখন বহুল ব্যবহৃত অ্যাক্সেস ডাটাবেস ফাইল ফরম্যাট। মাইক্রোসফ্ট ACCDB ফরম্যাটে অতিরিক্ত বৈশিষ্ট্যগুলিকে সমর্থন করে যেমন ফাইল সংযুক্তি, বাইনারি ডেটা এবং বহু-মূল্যবান ক্ষেত্র সমর্থন সংরক্ষণের সম্ভাবনা।

## ACCDB ফাইল ফরম্যাট

MDB এর মত, ACCDB ফাইল ফরম্যাটের জন্য কোন পাবলিক স্পেসিফিকেশন উপলব্ধ নেই। Microsoft ওপেন ডেটাবেস কানেক্টিভিটি (ODBC) স্ট্যান্ডার্ড এবং ভিজ্যুয়াল বেসিক ফর অ্যাপ্লিকেশান (VBA) এর মাধ্যমে প্রোগ্রামেটিকভাবে এই ফাইলগুলি অ্যাক্সেস করতে সমর্থন করে।

### অন্তর্দৃষ্টি

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. ACCDB ফাইলগুলিতে, এই সূচকটি ফাইলটি তৈরি করতে ব্যবহৃত ACE ইঞ্জিনের সংস্করণের পরিবর্তে ফাইলটির সামঞ্জস্যতা প্রতিফলিত করে বলে মনে হয়।

## তথ্যসূত্র

* [অ্যাক্সেস 2016 স্পেসিফিকেশন](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [মাইক্রোসফ্ট জেট ডেটাবেস ইঞ্জিন](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [আমি কোন অ্যাক্সেস ফাইল ফর্ম্যাট ব্যবহার করব?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


