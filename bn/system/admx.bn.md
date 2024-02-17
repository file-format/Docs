{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADMX ফাইল - গ্রুপ পলিসি অ্যাডমিনিস্ট্রেটিভ টেমপ্লেট ফাইল ফরম্যাট",
  "description":"ADMX ফাইল ফরম্যাট এবং কিভাবে ADMX ফাইল খুলতে হয় সে সম্পর্কে জানুন।",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx-bn",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## একটি ADMX ফাইল কি?

An ADMX file is a policy configuration file used by Microsoft Windows Group Policy software that manages group of computers in a group. It is an XML-based administrative template file and was introduced with Windows Vista Service Pack 1. ADMX ফাইলগুলিতে ব্যবহারকারীর অ্যাকাউন্ট, অপারেটিং সিস্টেম কনফিগারেশন এবং অ্যাপ্লিকেশনগুলির জন্য কনফিগারেশন সেটিংস থাকে। ADMX ফাইলগুলি অনেক কম্পিউটার সিস্টেমের কেন্দ্রীভূত ব্যবস্থাপনার জন্য কনফিগারেশনগুলি সংরক্ষণ এবং স্থাপন করতে ব্যবহৃত হয়।

আপনি যেকোনো XML-সামঞ্জস্যপূর্ণ, যেকোনো পাঠ্য সম্পাদক বা Microsoft Group Policy অবজেক্ট এডিটর ব্যবহার করে ADMX ফাইল তৈরি বা সম্পাদনা করতে পারেন।

## ADMX ফাইল ফরম্যাট - আরও তথ্য

ADMX ফাইলগুলি সর্বজনীন [XML](/web/xml/) ফাইল বিন্যাসে সংরক্ষণ করা হয় যা মানুষের পাঠযোগ্য। এটি বহুভাষিক ফাইল বিন্যাস এবং বিভিন্ন ভাষার সিস্টেম অ্যাডমিনিস্ট্রেটরদের একই ADMX ফাইলের সাথে কাজ করার অনুমতি দেয়। ADMX ফাইলগুলি পুরানো [ADM](/system/adm/) ফাইল ফর্ম্যাটকে প্রতিস্থাপন করেছে যা একটি ইউনিকোড-ফরম্যাট করা টেক্সট ফাইল ফর্ম্যাট৷ ADMX ফাইলগুলি রেজিস্ট্রি কীগুলি নির্দিষ্ট করে যা পরিবর্তিত হয় যখন একটি নির্দিষ্ট গ্রুপ নীতি সেটিং পরিবর্তন করা হয়।

### আমি ADMX ফাইল দিয়ে কি করতে পারি?

ADMX ফাইলগুলি সংজ্ঞায়িত করে যে কোন ক্রিয়াগুলি একটি গ্রুপের অংশ ব্যবহারকারী কম্পিউটারগুলিতে অনুমোদিত। গ্রুপ নীতি সক্রিয় ডিরেক্টরি সফ্টওয়্যারের সাথে সংমিশ্রণে সেট করা নিয়মগুলি আরোপ করে। ADMX ফাইলগুলি Windows OS-এর কেন্দ্রীয় স্টোর থেকে পরিচালিত হয় যা ডোমেনের একটি কেন্দ্রীয় অবস্থান।

একটি কাজের পরিবেশে স্থাপন করা একটি ADMX ফাইল প্রশাসকদের নীতিগুলি বাস্তবায়ন করতে দেয় যেমন:

 * ইন্টারনেট ব্যবহার নিয়ন্ত্রণ করুন
 * নির্দিষ্ট ধরনের ফাইল ডাউনলোড করা হচ্ছে
 * সিস্টেমে অপসারণযোগ্য ডিভাইসের ব্যবহার

## তথ্যসূত্র

* [প্রশাসনিক টেমপ্লেট ফাইল - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ - প্রশাসনিক টেমপ্লেট ফাইল পরিচালনা করা](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


