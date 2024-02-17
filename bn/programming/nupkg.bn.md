{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NUPKG ফাইল - NuGet প্যাকেজ ফাইল",
  "description":"NUPKG ফাইল ফরম্যাট এবং APIগুলি সম্পর্কে জানুন যা NUPKG ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## একটি NUPKG ফাইল কি?

একটি NUPKG ফাইল হল একটি প্যাকেজ ফাইল যাতে .NET প্রজেক্টে ব্যবহার করার জন্য প্যাকেজ তৈরি করার জন্য NuGet সফ্টওয়্যার দ্বারা ব্যবহার করা সোর্স কোড থাকে। অনলাইন প্যাকেজ হোস্টিং রিপোজিটরি থেকে প্যাকেজগুলি আনার জন্য মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিওর অংশ হিসাবে NuGet প্যাকেজ ম্যানেজার উপাদানটি ইনস্টল করা হয়েছে। NUPKG ফাইলগুলি বিকাশকারীদের ম্যানুয়ালি ডেভেলপমেন্ট প্যাকেজগুলি ডাউনলোড এবং ইনস্টল করার পরিবর্তে NuGet প্যাকেজ ম্যানেজার ব্যবহার করে [Nuget.org](https://nuget.org) থেকে সর্বশেষ প্যাকেজগুলি আনতে সাহায্য করে৷ NUPKG ফাইলগুলি NUSPEC ফাইলগুলি থেকে তৈরি করা হয় এবং, আনা হলে, ব্যবহারকারী সিস্টেমে প্যাকেজটি ইনস্টল করুন।

## NUPKG ফাইল ফরম্যাট

NUPKG ফাইলগুলি হল [ZIP](/compression/zip/) আর্কাইভ যা এর ভিতরে প্যাকেজ করা লাইব্রেরি ধারণ করে৷ ডাউনলোড করা হলে, এটির নাম পরিবর্তন করে .zip করা যেতে পারে এবং WinZIP, 7-Zip, এবং Apple Archive Utility-এর মতো যেকোনো স্ট্যান্ডার্ড জিপ ইউটিলিটি দিয়ে বের করা যেতে পারে।

## রেফারেন্স

* [Nuget.org](https://nuget.org)

* [কুইকস্টার্ট: ভিজ্যুয়াল স্টুডিওতে একটি প্যাকেজ ইনস্টল করুন এবং ব্যবহার করুন (শুধুমাত্র উইন্ডোজ)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- স্টুডিও)

* [কীভাবে একটি নুগেট প্যাকেজ তৈরি এবং প্রকাশ করবেন](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)


