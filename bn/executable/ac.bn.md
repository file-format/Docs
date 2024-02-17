{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "এসি ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা ACCDB ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "এসি ফাইল ফরম্যাট - অটোকনফ স্ক্রিপ্ট ফাইল",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-bn",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## একটি AC ফাইল কি?

AC ফাইল হল Autoconf স্ক্রিপ্ট ফাইল। **Autoconf** হল M4 ম্যাক্রোগুলির একটি এক্সটেনসিবল প্যাকেজ যা সফ্টওয়্যার সোর্স কোড প্যাকেজগুলি স্বয়ংক্রিয়ভাবে কনফিগার করতে শেল স্ক্রিপ্ট তৈরি করে। এই স্ক্রিপ্টগুলি ম্যানুয়াল ব্যবহারকারীর হস্তক্ষেপ ছাড়াই প্যাকেজগুলিকে অনেক ধরণের UNIX-এর মতো সিস্টেমে মানিয়ে নিতে পারে। অটোকনফ একটি টেমপ্লেট ফাইল থেকে প্যাকেজের জন্য একটি কনফিগারেশন স্ক্রিপ্ট তৈরি করে যা M4 ম্যাক্রো কলের আকারে প্যাকেজটি ব্যবহার করতে পারে এমন অপারেটিং সিস্টেম বৈশিষ্ট্যগুলি তালিকাভুক্ত করে।

Producing configuration scripts using Autoconf requires GNU M4. অটোকনফ কনফিগার করার আগে আপনার GNU M4 (অন্তত সংস্করণ 1.4.6, যদিও 1.4.13 বা তার পরে বাঞ্ছনীয়) ইনস্টল করা উচিত, যাতে Autoconf-এর কনফিগার স্ক্রিপ্ট এটি খুঁজে পেতে পারে। Autoconf দ্বারা উত্পাদিত কনফিগারেশন স্ক্রিপ্টগুলি স্বয়ংসম্পূর্ণ, তাই তাদের ব্যবহারকারীদের Autoconf (বা GNU M4) থাকার প্রয়োজন নেই।

## কিভাবে এসি ফাইল খুলবেন?

AC মানে স্বয়ংক্রিয় কনফিগারেশন। এটি GNU Autoconf দ্বারা তৈরি একটি স্ক্রিপ্ট যা প্যাকেজে প্রয়োজনীয় বৈশিষ্ট্যগুলির জন্য পরীক্ষা করে বিভিন্ন Posix-এর মতো সিস্টেমে সফ্টওয়্যার সোর্স কোডকে অভিযোজিত করতে সক্ষম করে। স্ক্রিপ্ট একটি AC ফাইল বলা হয়.

## প্রধান Autotools উপাদান

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools হল সম্পর্কিত প্যাকেজের একটি সংগ্রহ যা একসাথে ব্যবহার করা হলে পোর্টেবল সফ্টওয়্যার তৈরিতে জড়িত অনেক অসুবিধা দূর হয়। এই টুলগুলি, কিছু তুলনামূলকভাবে সহজ আপস্ট্রিম-সরবরাহকৃত ইনপুট ফাইল সহ, একটি প্যাকেজের জন্য বিল্ড সিস্টেম তৈরি করতে ব্যবহৃত হয়।

**প্রধান অটোটুল উপাদানগুলি কীভাবে একত্রে ফিট করে তার একটি প্রাথমিক ওভারভিউ।**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

একটি সাধারণ সেটআপে:

- `autoconf` প্রোগ্রামটি `configure.in` বা `configure.ac` থেকে একটি কনফিগার স্ক্রিপ্ট তৈরি করে।
- 'অটোমেক' প্রোগ্রামটি Makefile.am থেকে একটি Makefile.in তৈরি করে।
- Makefile.in ফাইল থেকে এক বা একাধিক মেকফাইল ফাইল তৈরি করতে `কনফিগার` স্ক্রিপ্ট চালানো হয়।
- 'মেক' প্রোগ্রামটি প্রোগ্রাম কম্পাইল করতে মেকফাইল ব্যবহার করে।

## তথ্যসূত্র
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [অটোটুলগুলির মূল বিষয়গুলি](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



