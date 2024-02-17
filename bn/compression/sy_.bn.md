{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SY_ ফাইল ফরম্যাট - সংকুচিত SYS ফাইল",
  "description":"SY_ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি SY_ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## একটি SY_ ফাইল কি?

একটি SY_ ফাইল হল একটি সংকুচিত .sys ফাইল যা সফ্টওয়্যার ইনস্টলাররা ইনস্টলারের ভিতরে প্যাকেজ করা ইনস্টলেশন ফাইলের আকার কমাতে ব্যবহার করে। এটি ইনস্টলারের সামগ্রিক আকার হ্রাস করে। SY_ ফাইলগুলিকে Microsoft Expand কমান্ড লাইন ইউটিলিটি ব্যবহার করে প্রসারিত করা যেতে পারে যা এক বা একাধিক সংকুচিত ফাইলকে প্রসারিত করে।

## SY_ ফাইল ফরম্যাট - আরও তথ্য

SY_ ফাইলগুলি সংকুচিত বাইনারি ফাইল হিসাবে ডিস্কে সংরক্ষণ করা হয়। যাইহোক, তাদের অভ্যন্তরীণ ফাইল বিন্যাস সর্বজনীনভাবে উপলব্ধ নয়। Microsoft Expand কমান্ড লাইন ইউটিলিটি নিম্নলিখিত কমান্ড লাইনগুলির একটি ব্যবহার করে SY_ ফাইলগুলিকে প্রসারিত করতে পারে।

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
প্রসারিত হলে, SY_ ফাইলগুলি [SYS](/system/sys/) ফাইলে রূপান্তরিত হয়৷

SY_ ফাইলগুলি EX_ এবং DL_ ফাইলগুলির অনুরূপ৷

## তথ্যসূত্র

 * [StuffIt - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/StuffIt)
 * [মাইক্রোসফ্ট প্রসারিত](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

