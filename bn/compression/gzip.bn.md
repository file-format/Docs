{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GZIP ফাইল ফরম্যাট - GNU জিপ করা আর্কাইভ ফাইল",
  "description":"একটি GZIP ফাইল এবং API যা GZIP ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## একটি GZIP ফাইল কি?

একটি GZIP ফাইল হল একটি সংকুচিত আর্কাইভ যা স্ট্যান্ডার্ড [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) কম্প্রেশন অ্যালগরিদম দিয়ে তৈরি করা হয়। সংকুচিত সংরক্ষণাগারে সংকুচিত ফাইল, ডিরেক্টরি এবং ফাইল স্টাব সহ একাধিক ফাইল থাকতে পারে। বেশিরভাগ ইউনিক্স সিস্টেমে ফাইলের কম্প্রেশন/ডিকম্প্রেশনের জন্য ওপেন সোর্স gzip (GNU Zip) কম্প্রেসার ইউটিলিটি অন্তর্ভুক্ত থাকে। GZIP ফাইলগুলি [WinZip](https://www.winzip.com/en/) এর মতো অ্যাপ্লিকেশন দিয়ে খোলা যেতে পারে৷

## GZIP ফাইল ফরম্যাট - আরও তথ্য

GZIP ফাইলগুলিকে সংরক্ষণাগারে সংকুচিত করতে [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) অ্যালগরিদম ব্যবহার করে৷ দুটি RFC, [RFC1952](https://tools.ietf.org/html/rfc1952) এবং [RFC 1951](https://tools.ietf.org/html/rfc1951), যথাক্রমে gzip র্যাপার ফরম্যাটের স্পেসিফিকেশন এবং ডিফ্লেট কম্প্রেসড ডেটা ফরম্যাটকে সংজ্ঞায়িত করে।

GZIP ফাইলগুলি প্রায়ই [GZ](/compression/gz/) ফাইল ফর্ম্যাট হিসাবে সংরক্ষিত হয়৷

## তথ্যসূত্র

* [gzip](http://www.gzip.org/)

* [gzip - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP ফাইল ফর্ম্যাট স্পেসিফিকেশন](https://datatracker.ietf.org/doc/html/rfc1952), IETF দ্বারা

* [RFC 1951](https://tools.ietf.org/html/rfc1951)


