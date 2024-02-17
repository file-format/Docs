
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "এডিএস ফাইল - অ্যাডা স্পেসিফিকেশন ফাইল ফরম্যাট",
  "description":"উদাহরণ সহ ADS ফাইল ফরম্যাট কি সে সম্পর্কে জানুন এবং APIs যা ADS ফাইল তৈরি করতে এবং খুলতে পারে।",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-bn",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## একটি ADS ফাইল কি?

একটি ADS ফাইল একটি Ada প্রোগ্রামিং প্রকল্পের জন্য একটি স্পেসিফিকেশন ফাইল। এটি জাভার জন্য একটি ক্লাসের অনুরূপ, অথবা C++ এর ক্ষেত্রে শিরোনাম এবং বাস্তবায়ন জোড়া। Ada প্যাকেজের পাবলিক এবং প্রাইভেট স্পেসিফিকেশন .ads ফাইলে সংরক্ষণ করা হয়। বিপরীতে, .adb ফাইলে বাস্তবায়ন বা অ্যাডা বডি রয়েছে। [C++](/programming/cpp/)-এর মতো, Ada নির্দিষ্টকরণ এবং OOP থেকে স্বাধীন বাস্তবায়নের মধ্যে বিচ্ছেদ প্রস্তাব করে৷

ADS ফাইলগুলি যেকোন পাঠ্য সম্পাদক যেমন Microsoft Notepad, Notepad++, এবং Atom-এ খোলা যেতে পারে।

## এডিএস ফাইল ফরম্যাট

এডিএস ফাইলগুলি সরল প্লেইন টেক্সট ফাইল ফরম্যাটে এবং যেকোনো টেক্সট এডিটর দিয়ে খোলা/সম্পাদিত হতে পারে। অ্যাডা প্যাকেজগুলিকে ক্রমানুসারে সংগঠিত করা যেতে পারে। একটি শিশু ইউনিট নিম্নলিখিত উপায়ে ঘোষণা করা যেতে পারে:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## তথ্যসূত্র

 * [Ada প্যাকেজ](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

