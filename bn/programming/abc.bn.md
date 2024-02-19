
{
  "date": "2021-12-14",
  "keywords": [
    ".abc file",
    "extension",
    "format",
    "ActionScript Byte Code File",
    "how to open .abc file",
    "abc file format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ABC - অ্যাকশনস্ক্রিপ্ট বাইট কোড ফাইল",
  "description": "উদাহরণ সহ এবিসি ফাইল ফরম্যাট কী এবং এবিসি ফাইলগুলি তৈরি এবং খুলতে পারে এমন APIগুলি সম্পর্কে জানুন৷",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-abc-bn"
    }
  },
  "lastmod": "2021-12-14"
}

## একটি ABC ফাইল কি?

.abc এক্সটেনশন সহ একটি ফাইল হল একটি অ্যাকশনস্ক্রিপ্ট বাইট কোড ফাইল যা অ্যাকশনস্ক্রিপ্ট স্ক্রিপ্ট ফাইল কম্পাইল করার ফলে ফ্ল্যাশ কম্পাইলার দ্বারা তৈরি করা হয়েছে। ABC ফাইলে থাকা বাইট কোডটি অ্যাকশনস্ক্রিপ্ট ভার্চুয়াল মেশিন (AVM এবং AVM2) দ্বারা কার্যকর করা হয়। বাইট কোড ধ্রুবক ডেটা, AVM2 নির্দেশনা সেট থেকে নির্দেশাবলী এবং বিভিন্ন ধরণের মেটাডেটা নিয়ে গঠিত। যখন একটি ABC ফাইল AVM বা AVM2 এ লোড করা হয়, তখন এটি যাচাইকরণের মধ্য দিয়ে যায়। যদি এটি AVM2 সংক্ষিপ্ত বিবরণের সাথে সঙ্গতিপূর্ণ না হয় তবে এটি প্রত্যাখ্যান করা হয়। ABC ফাইলগুলি Adobe Flash Player-এ খোলা যেতে পারে যা অনেক আগেই বন্ধ হয়ে গেছে।

## ABC ফাইল ফরম্যাট - আরও তথ্য

এবিসি ফাইলগুলি বাইনারি ফাইল বিন্যাসে ডিস্কে সংরক্ষণ করা হয় যা AVM বা AVM2 ভার্চুয়াল মেশিন দ্বারা পাঠযোগ্য। এর অভ্যন্তরীণ ফাইল কাঠামোটি তার সমস্ত ধ্রুবক ডেটা, টাইপ বর্ণনাকারী, কোড এবং মেটাডেটা সহ এক্সিকিউটেবল কোড ব্লকের প্রতিনিধিত্ব করে।

## ABC ফাইল স্ট্রাকচার

ABC ফাইলের গঠন নিচে দেখানো হয়েছে।

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC ফাইলের ক্ষেত্র

|ক্ষেত্রের নাম|বর্ণনা|
---|---|
|minor_version, major_version|major_version এবং minor_version এর মান হল abcFile ফরম্যাটের প্রধান এবং ছোট সংস্করণ সংখ্যা।|
|constant_pool|ধ্রুবক_পুল হল একটি পরিবর্তনশীল দৈর্ঘ্যের কাঠামো যা পূর্ণসংখ্যা, দ্বিগুণ, স্ট্রিং, নেমস্পেস, নেমস্পেস সেট এবং মাল্টিনামের সমন্বয়ে গঠিত।|
|method_count, method|method_count-এর মান হল মেথড অ্যারের এন্ট্রির সংখ্যা। পদ্ধতি অ্যারের প্রতিটি এন্ট্রি একটি পরিবর্তনশীল দৈর্ঘ্য method_info কাঠামো।|
|metadata_count, metadata|metadata_count-এর মান হল মেটাডেটা অ্যারের এন্ট্রির সংখ্যা। প্রতিটি মেটাডেটা এন্ট্রি হল একটি মেটাডেটা_ইনফস্ট্রাকচার যা স্ট্রিং মানগুলির একটি সেটে একটি নাম ম্যাপ করে। |
|class_count, instance, class|class_count-এর মান হল ইন্সট্যান্স এবং ক্লাস অ্যারেতে এন্ট্রির সংখ্যা। |
|script_count, script|script_count-এর মান হল স্ক্রিপ্ট অ্যারের এন্ট্রির সংখ্যা। প্রতিটি স্ক্রিপ্ট এন্ট্রি হল একটি script_info কাঠামো যা এই ফাইলের একটি একক স্ক্রিপ্টের বৈশিষ্ট্য নির্ধারণ করে। |
|method_body_count, method_body| method_body_count-এর মান হল মেথড_বডি অ্যারের এন্ট্রির সংখ্যা। প্রতিটি মেথড_বডি এন্ট্রিতে একটি পরিবর্তনশীল দৈর্ঘ্যের মেথড_বডি_ইনফো গঠন থাকে যা একটি পৃথক পদ্ধতি বা ফাংশনের নির্দেশাবলী ধারণ করে।|

## তথ্যসূত্র

 * [শক্তিশালী ABC (অ্যাকশনস্ক্রিপ্ট বাইটকোড) [ডিস-]অ্যাসেম্বলার - গিথুব](https://github.com/CyberShadow/RABCDAsm)

