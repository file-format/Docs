{
  "date" : "2021-12-09",
  "keywords" : [ "aro",".aro file", "aro file format", "an file type", "file", "type", "what is a .aro file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ARO ফাইল ফরম্যাট - SteelArrow ওয়েব অ্যাপ্লিকেশন ফাইল",
  "description" : "একটি ARO ফাইল এবং APIগুলি কী যা ARO ফাইলগুলি তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## একটি ARO ফাইল কি?

একটি ARO ফাইল হল একটি সার্ভার সাইড ওয়েব পেজ ফাইল যা SteelArrow ওয়েব অ্যাপ্লিকেশন দিয়ে তৈরি করা হয়। এটিতে [HTML](/web/html/) এবং SteelArrow ট্যাগ এবং স্ক্রিপ্ট রয়েছে৷ এগুলি ব্যবহারকারীর ব্রাউজারে পাঠানোর আগে সম্পূর্ণ প্রতিক্রিয়া পৃষ্ঠা তৈরি করতে সার্ভারে কার্যকর করা হয়। ARO ফাইলগুলিতে HTML সামগ্রীর প্রায় 95% থাকে এবং বাকিগুলি SteelArrow কোড নিয়ে থাকে। ARO ফাইলগুলি আপনার জন্য কাজ করার জন্য, SteelArrow ওয়েব অ্যাপ্লিকেশন সার্ভারটি ইনস্টল করা উচিত এবং ওয়েব সার্ভার মেশিনে চলছে৷

## ARO ফাইল ফরম্যাট

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web pages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### ARO ট্যাগের উদাহরণ

দ্য<SAOUTPUT> ARO ট্যাগ ডেভেলপারদের একটি স্ক্রিপ্টের মধ্যে যেকোনো স্থানে ডেটা মান আউটপুট করতে দেয়। উদাহরণস্বরূপ, এটি PARAM টেবিলের আউটপুট পেতে ব্যবহার করা যেতে পারে<SAOUTPUT VALUE=PARAM[]> যেটি HTML এর মধ্যে প্রদর্শিত হতে পারে<BODY> ট্যাগ

## তথ্যসূত্র

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)

