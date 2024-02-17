{
  "date" : "2022-03-21",
  "keywords" : [ "xpr file", "xpr file format", "what is an xpr file", "file", "xpr example", "xpr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XPR ফাইল ফরম্যাট - মাইক্রোসফট এক্সপ্রেশন ডিজাইন গ্রাফিক ফাইল",
  "description":"XPR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি XPR ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## একটি XPR ফাইল কি?

একটি XPR ফাইল হল একটি ভেক্টর ইমেজ ফাইল যা এখন বন্ধ করা Microsoft Expression Graphics (EGD) সফ্টওয়্যার দিয়ে তৈরি করা হয়েছে। এটিতে গ্রাফিক্স তথ্য রয়েছে যা ইউজার ইন্টারফেস মকআপ হিসাবে ব্যবহার করা যেতে পারে। XPR ফাইলগুলি পরে মাইক্রোসফট এক্সপ্রেশন ডিজাইনে .design ফাইল দ্বারা প্রতিস্থাপিত হয়। XPR ফাইলগুলি মাইক্রোসফ্ট এক্সপ্রেশন স্টুডিও দিয়ে খোলা যেতে পারে যা বেশ কিছুদিন ধরে বন্ধ হয়ে গেছে।

## XPR ফাইল বিন্যাস দুর্বলতা

XPR ফাইলগুলি মাইক্রোসফ্ট এক্সপ্রেশন ডিজাইনের একটি দুর্বলতাকে উপকৃত করার জন্য চিহ্নিত করা হয়েছিল, যা দূরবর্তী কোড কার্যকর করার অনুমতি দেয়। রিপোর্ট করা ইস্যুতে, যদি একজন ব্যবহারকারী একটি বৈধ .xpr ফাইল খোলে যা নেটওয়ার্ক ডিরেক্টরিতে ডায়নামিক লিঙ্ক লাইব্রেরি (DLL) ফাইলের সাথে lcoated আছে, Microsoft Expression Design DLL ফাইলটি লোড করার চেষ্টা করতে পারে এবং এতে থাকা কোডটি কার্যকর করতে পারে। এটি পরবর্তীতে একটি নিরাপত্তা আপডেটে মাইক্রোসফট দ্বারা সংশোধন করা হয়েছে।

## তথ্যসূত্র

* [Vulnerability in Expression Design Could Allow Remote Code Execution (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

