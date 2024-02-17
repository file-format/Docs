{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CDF - চ্যানেল সংজ্ঞা বিন্যাস",
  "description" : "একটি CDF ফাইল এবং API যা CDF ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## একটি CDF ফাইল কি?

.cdf এক্সটেনশন সহ একটি ফাইল হল একটি XLM ভিত্তিক তথ্য বিতরণ ফাইল বিন্যাস যা চ্যানেল হিসাবে ঘন ঘন আপডেট প্রকাশ করতে ব্যবহৃত হত। তথ্য যেকোন ওয়েব সার্ভার থেকে প্রকাশিত হয় এবং স্বয়ংক্রিয়ভাবে ওয়েব ব্রাউজারগুলির মতো সামঞ্জস্যপূর্ণ গ্রহণকারী প্রোগ্রামগুলির সাথে কম্পিউটারে বিতরণ করা হয়। ব্যবহারকারীরা সক্রিয় চ্যানেলে সাবস্ক্রাইব করে এবং তাদের ডেস্কটপে বিতরিত আপডেটগুলি নির্ধারিত করে।
সিডিএফ ফাইলগুলি আগে মাইক্রোসফ্টের অ্যাক্টিভ চ্যানেল, অ্যাক্টিভ ডেস্কটপ এবং স্মার্ট অফলাইন ফেভারিট প্রযুক্তিগুলির সাথে একত্রে ব্যবহার করা হয়েছিল।

## CDF ফাইল ফরম্যাট

CDF ফাইলগুলি XML ফাইল হিসাবে সংরক্ষিত হয় যা তথ্য বিনিময়ের জন্য একটি জেনেরিক ওয়েব ফাইল ফর্ম্যাট। CDF ফাইল বিন্যাস এখন একটি পুরানো বিন্যাস এবং ব্যাপকভাবে গৃহীত হয় নি। এর তুলনায়, নেটস্কেপের আরএসএস বেশি বিখ্যাত এবং ব্যাপকভাবে ব্যবহৃত হয়েছিল।

### CDF ফাইল ফরম্যাটের উদাহরণ

নিম্নলিখিতটি CDF ফাইল বিন্যাসের একটি সাধারণ উদাহরণ।

```
<?xml version=1.0 encoding=UTF-8?>
<CHANNEL HREF=http://domain/folder/pageOne.extension
BASE=http://domain/folder/
লাস্টমোড=1998-11-05T22:12
PRECACHE=হ্যাঁ
লেভেল=0>
<TITLE>চ্যানেলের শিরোনাম</TITLE>
<ABSTRACT>চ্যানেলের বিষয়বস্তুর সংক্ষিপ্তসার।</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY=14/>
</SCHEDULE>
<LOGO HREF=wideChannelLogo.gif STYLE=IMAGE-WIDE/>
<LOGO HREF=imageChannelLogo.gif STYLE=IMAGE/>
<LOGO HREF=iconChannelLogo.gif STYLE=ICON/>
<ITEM HREF=pageTwo.extension
    লাস্টমোড=1998-11-05T22:12
    PRECACHE=হ্যাঁ
স্তর=1>
<TITLE>পৃষ্ঠা দুই এর শিরোনাম</TITLE>
<ABSTRACT>পৃষ্ঠা দুই এর বিষয়বস্তুর সংক্ষিপ্তসার।</ABSTRACT>
<LOGO HREF=pageTwoLogo.gif STYLE=IMAGE/>
<LOGO HREF=pageTwoLogo.gif STYLE=ICON/>
</ITEM>
</CHANNEL>
```

## তথ্যসূত্র

* [চ্যানেল সংজ্ঞা বিন্যাস - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Channel_Definition_Format)


