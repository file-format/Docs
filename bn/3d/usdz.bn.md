{
  "date": "2021-02-01",
  "keywords": [
    "usdz",
    "usdz file",
    "usdz file format",
    "file format",
    "3d",
    "usdz file download"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "USDZ - ইউনিভার্সাল দৃশ্য বর্ণনা জিপ বিন্যাস",
  "description": "USDZ ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা USDZ ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usdz-bn"
    }
  },
  "lastmod": "2021-02-01"
}

## একটি USDZ ফাইল কি?

.usdz-এর সাথে একটি ফাইল হল [USD](/3d/usd/) (ইউনিভার্সাল সিন বর্ণনা) ফাইল ফরম্যাটের জন্য একটি কম্প্রেসড এবং আনএনক্রিপেটেড জিপ আর্কাইভ যা আর্কাইভের মধ্যে এমবেড করা অন্যান্য ফরম্যাটের (যেমন টেক্সচার এবং অ্যানিমেশন) ফাইলগুলির জন্য প্রক্সি ধারণ করে এবং সেগুলি চালায় কোনো প্যাকিং ছাড়াই সরাসরি USD রান-টাইমের সাথে। USDZ ফাইলগুলি হল প্যাকেজ যার ডিজাইন একটি প্যাকেজের নতুন Ar-স্তরের বিমূর্ততার উপর ভিত্তি করে। Usdz IANA-তে নিবন্ধিত ছিল এবং মডেলের মিডিয়া টাইপ নাম এবং vnd.usd+zip-এর একটি সাব-টাইপ নাম রয়েছে এবং এর বিশদ বিবরণ [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip)-এ পাওয়া যাবে।

## USDZ ফাইল ফরম্যাট

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### জিপ সীমাবদ্ধতা

USDZ ফাইল বিন্যাস কোনো `কম্প্রেশন` এবং `এনক্রিপশন` ছাড়াই জিপ ফাইল বিন্যাস ব্যবহার করে। এটি দুটি প্রয়োজনীয়তা পূরণ করার জন্য ডিজাইন দ্বারা লক্ষ্য করা হয়েছিল:

 * ইতিমধ্যেই মেমরিতে লোড করা প্যাকেজের জন্য বা ডিস্কে একটি একক ফাইল হিসাবে, চিত্রের মধ্যে থাকা ডেটা অ্যাক্সেস করার জন্য API USD-এ উপলব্ধ
 * ডিস্কে ফাইল এক্সট্র্যাক্ট করার বা আরও হিপ স্টোরেজ বরাদ্দ করার দরকার নেই

USDZ এর সাথে, এই উভয় প্রয়োজনীয়তা পূরণ করা হয় কারণ বেশিরভাগ চিত্র বিন্যাস নিজেই অভ্যন্তরীণ কম্প্রেশন স্কিমগুলিকে অনুমতি দেয়, যার ফলে ফাইলের আকার কমপ্যাক্ট হয়।

### লেআউট প্রয়োজনীয়তা

USDZ প্যাকেজগুলির জন্য প্যাকেজের মধ্যে ফাইলগুলির বিন্যাস প্রয়োজন যে প্রতিটি ফাইলের জন্য ডেটা প্যাকেজের শুরু থেকে 64 বাইটের একাধিক থেকে শুরু হওয়া উচিত। যাইহোক, প্যাকেজটিকে একটি সাধারণ রেফারেন্স সহ প্যাকেজ টার্গেট করার ক্ষেত্রে একটি নেটিভ [USD](/3d/usd/) ফাইল দিয়ে শুরু করা উচিত। এই ধরনের ক্ষেত্রে, এই প্রথম USD ফাইলটিকে ডিফল্ট স্তর হিসাবে উল্লেখ করা হয়। স্ট্রিমেবল কন্টেন্ট প্রদান করতে ইচ্ছুক ক্লায়েন্টরা অন্যান্য লেআউট সীমাবদ্ধতাগুলিও বিবেচনা করতে পারেন।

## USDZ ফাইল ডাউনলোড
যেহেতু ইউএসডিজেড ফাইলগুলি অন্যান্য উচ্চ মানের ছবি এবং ইউএসডি ফাইলগুলির সাথে প্যাক করা হয়, তারা আরও বেশি ডিস্ক সঞ্চয়স্থান দখল করতে পারে। এখানে আপনি ডাউনলোডের জন্য একটি সহজ এবং ছোট USDZ উদাহরণ ফাইল পেতে পারেন:

- [Sample.usdz](../sample.usdz)

## তথ্যসূত্র

* [USDZ ফাইল ফরম্যাট স্পেসিফিকেশন](https://openusd.org/release/spec_usdz.html)


