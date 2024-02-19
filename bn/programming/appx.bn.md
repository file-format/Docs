{
  "date": "2021-04-22",
  "keywords": [
    "appx file",
    "extension",
    "format",
    "how to open appx file",
    "appx file format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "APPX - একটি APPX ফাইল কি?",
  "description": "APPX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি APPX ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-appx-bn"
    }
  },
  "lastmod": "2021-12-16"
}

## একটি APPX ফাইল কি?

একটি APPX ফাইল একটি বিতরণযোগ্য প্যাকেজ ফাইল বিন্যাস যা একটি অ্যাপ্লিকেশন বিতরণ এবং ইনস্টলেশনের জন্য ব্যবহৃত হয়। মাইক্রোসফ্ট উইন্ডোজ স্টোরে প্রকাশিত হওয়ার জন্য এটি উইন্ডোজ 8 এর সাথে প্রবর্তন করা হয়েছিল। এটিতে একটি উইন্ডোজ অ্যাপ্লিকেশন ইনস্টল করার জন্য প্রয়োজনীয় সমস্ত ফাইল রয়েছে। এর মধ্যে রয়েছে মেটাডেটা, ফাইল এবং শংসাপত্রের তথ্য। একটি আরও আধুনিক প্যাকেজিং ফাইল ফর্ম্যাট হল MSIX যা বর্তমানে APPX এর তুলনায় বেশি ব্যবহৃত হয়।

## APPX ফাইল ফরম্যাট - আরও তথ্য

APPX ফাইলগুলি [ZIP](/compression/zip/) ফাইল ফর্ম্যাটে সংকুচিত ফাইল হিসাবে সংরক্ষিত হয়৷ এটি সম্পূর্ণ প্যাকেজটিকে একটি আর্কাইভ ফাইল হিসাবে তৈরি করে যা ফাইলের আকার হ্রাস করে যা মাইক্রোসফ্ট স্টোরে আপলোড করা সহজ।

## কিভাবে একটি APPX ফাইলে ফাইল দেখতে?

একটি APPX ফাইলের মধ্যে বিষয়বস্তু বা ফাইলগুলি দেখতে, নিম্নলিখিত পদক্ষেপগুলি অনুসরণ করা উচিত৷

 1. যেহেতু APPX ফাইলগুলি সংকুচিত জিপ ফাইল হিসাবে সংরক্ষণ করা হয়, তাই ফাইলটির নাম পরিবর্তন করে .zip এক্সটেনশন করুন
 1. APPX ফাইলে থাকা ফাইলগুলি বের করতে 7-Zip, WinZip, বা WinRAR-এর মতো যেকোনো ডিকম্প্রেশন টুল ব্যবহার করুন

## কিভাবে একটি APPX ফাইল তৈরি করবেন?

APPX ফাইল তৈরি করতে দুটি পদ্ধতি ব্যবহার করা যেতে পারে।

 1. MakeApp.exe ব্যবহার করে - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) উভয় অ্যাপ প্যাকেজ (.msix বা .appx) এবং অ্যাপ প্যাকেজ বান্ডেল ফাইল .msixbundle বা .appxbundle) তৈরি করতে ব্যবহৃত হয়। উপরন্তু, এটি একটি অ্যাপ্লিকেশন প্যাকেজ থেকে ফাইল নিষ্কাশন করতে পারেন. MakeApp.exe Windows 10 SDK এর সাথে উপলব্ধ এবং কমান্ড প্রম্পট থেকে ব্যবহার করা যেতে পারে।
 1. মাইক্রোসফট ভিজ্যুয়াল স্টুডিও ব্যবহার করা - ডেভেলপাররা সাধারণত [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) Microsoft ভিজ্যুয়াল স্টুডিও ব্যবহার করে। অ্যাপ্লিকেশন ডেভেলপমেন্ট সম্পূর্ণ হয়ে গেলে এবং অ্যাপটি প্রকাশের জন্য প্রস্তুত হলে, APPX প্যাকেজ ফাইলটি ভিজ্যুয়াল স্টুডিও থেকে প্রকাশ করে তৈরি করা যেতে পারে।

## তথ্যসূত্র

 * [MakeAppx.exe দিয়ে একটি MSIX প্যাকেজ বা বান্ডেল তৈরি করুন](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Microsoft Visual Studio ব্যবহার করে APPX ফাইল তৈরি করুন](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

