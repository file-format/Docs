{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OBML ফাইল ফরম্যাট - অপেরা মিনি সংরক্ষিত ওয়েবপেজ ফাইল",
  "description" : "একটি OBML ফাইল এবং API যা OBML ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন।",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## একটি OBML ফাইল কি?

একটি OBML (Opera Binary Markup Language) ফাইল হল Opera Mini মোবাইল ওয়েব ব্রাউজার দ্বারা সংরক্ষিত একটি ওয়েবপৃষ্ঠার একটি অফলাইন সংস্করণ। এটি [HTML](/web/html/) ফাইলগুলির একটি স্বয়ংসম্পূর্ণ, কম্প্যাক্ট সংস্করণ যা অফলাইনে থাকাকালীন নির্দিষ্ট ডিভাইসগুলিতে প্রদর্শনের জন্য পৃষ্ঠার সমস্ত উপাদান ধারণ করে৷ OBML ফাইল ফরম্যাটটি OBML15 এবং OBML16 ব্যাপকভাবে ব্যবহৃত হওয়ার সাথে বিভিন্ন সংস্করণে আপগ্রেড হয়েছে। বিবেচনায় রাখা একটি গুরুত্বপূর্ণ বিষয় হল যে প্রতিটি অপেরা মিনি সংস্করণ শুধুমাত্র একটি OBML ফর্ম্যাটের সাথে সামঞ্জস্যপূর্ণ। এইভাবে, অপেরা মিনি আপগ্রেড করার ফলে পূর্বে সংরক্ষিত পৃষ্ঠাগুলি পাঠযোগ্য হয়ে যাবে। OBML ফাইলগুলিকে HTML এবং [PDF](/pdf/)-এ রূপান্তর করা যেতে পারে।

## OBML ফাইল ফরম্যাট

OBML ফাইল ফরম্যাট অপেরার মালিকানাধীন ফাইল ফরম্যাটে সংরক্ষিত হয় এবং এর ফাইল ফরম্যাট স্পেসিফিকেশন সর্বজনীনভাবে উপলব্ধ নয়। যাইহোক, [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) এর গঠনকে অনুসরণ করে ডিকোড করার জন্য রিভার্স ইঞ্জিনিয়ার করা হয়েছিল।

### OBML ডেটা প্রকার

বিপরীত প্রকৌশলী ফলাফল অনুযায়ী, OBML নিম্নলিখিত আদিম প্রকারগুলি ব্যবহার করে:

 * `বাইট` - স্বাক্ষরবিহীন পূর্ণসংখ্যা (1 বাইট)
 * `শর্ট` - স্বাক্ষরিত পূর্ণসংখ্যা (2 বাইট, বড়-এন্ডিয়ান)
 * `মাঝারি` - স্বাক্ষরিত পূর্ণসংখ্যা (3 বাইট, বড়-এন্ডিয়ান)
 * `ব্লব` - {দৈর্ঘ্য: সংক্ষিপ্ত, ডেটা: বাইট [দৈর্ঘ্য] }
 * `char` - একটি ASCII অক্ষর ধারণকারী একটি বাইট
 * `স্ট্রিং` – একটি ব্লব যাতে UTF-8 এনকোড করা পাঠ্য থাকে

### OBML হেডার

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## তথ্যসূত্র

* [OMBL ফরম্যাট](https://github.com/grawity/obml-parser/blob/master/obml.md)


