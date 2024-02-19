{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MSG - Microsoft Outlook ইমেল বিন্যাস",
  "description": "MSG ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা MSG ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-msg-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি MSG ফাইল কি?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG ফাইল স্ট্রাকচার

CFB_3 ফরম্যাট হল MSG ফাইলের ভিত্তি। দৃষ্টান্তটি স্টোরেজ এবং স্ট্রিম ধারণার উপর ভিত্তি করে তৈরি করা হয়েছে, যা ডিরেক্টরি এবং ফাইলের বেশ কাছাকাছি। তাই পূর্বের মধ্যে একটি প্রধান পার্থক্য হল সমগ্র শ্রেণিবিন্যাস, একটি স্বতন্ত্র ফাইলে প্যাকেজ করা, যাকে যৌগিক ফাইল বলা হয়। অবজেক্ট বার্তা ফাইল গঠন করে এবং একটি একক সম্পত্তি বা এর সংগ্রহ নিয়ে গঠিত। এই ক্ষমতা একটি একক ফাইলে জটিল, স্ট্রাকচার্ড ডেটা সঞ্চয় করতে অ্যাপ্লিকেশনগুলিকে সহায়তা করে। এই বিন্যাসটি একাধিক স্টোরেজও নির্দিষ্ট করে, প্রতিটি স্টোরেজ মেসেজ অবজেক্টকে একটি প্রধান উপাদান হিসেবে উপস্থাপন করে। এই স্টোরেজগুলিতে সেই উপাদানটির একটি সম্পত্তির প্রতিনিধিত্ব করে এমন অনেকগুলি স্ট্রিম রয়েছে। স্টোরেজ নেস্টিং এছাড়াও সম্ভব.

## ম্যাপি বৈশিষ্ট্য

.msg ফাইলের শীর্ষ স্তরে, স্টোরেজগুলিতে স্ট্রীম থাকে যা তাদের মধ্যে বৈশিষ্ট্য সংরক্ষণ করে। বৈশিষ্ট্যগুলি নিম্নরূপ শ্রেণীবদ্ধ করা যেতে পারে:

* নির্দিষ্ট দৈর্ঘ্য বৈশিষ্ট্য

* পরিবর্তনশীল দৈর্ঘ্য বৈশিষ্ট্য

* একাধিক-মূল্যবান বৈশিষ্ট্য


বিভাগ নির্বিশেষে, একটি সম্পত্তি হয় একটি ট্যাগ বা নামকরণ করা হয়. যাইহোক, তাদের ম্যাপিং স্টোরেজ দ্বারা নির্দিষ্ট করা নামযুক্ত বৈশিষ্ট্যগুলির জন্য উপযুক্ত ম্যাপিং তথ্য প্রয়োজন।

## স্টোরেজ

স্টোরেজগুলি মেসেজ অবজেক্টের মূল উপাদান গঠন করে। MSG ফাইল ফর্ম্যাট নিম্নলিখিত স্টোরেজগুলিকে বলে:

## টপ লেভেল স্ট্রাকচার

মেসেজ অবজেক্ট MSG ফাইল ফরম্যাটের সম্পূর্ণ টপ লেভেলের প্রতিনিধিত্ব করে। প্রকার, বৈশিষ্ট্য, প্রাপকের সংখ্যা এবং সংযুক্তি বস্তুর উপর নির্ভর করে, একটি বার্তা বস্তুর সংশ্লিষ্ট .MSG ফাইলে বিভিন্ন স্ট্রিম স্টোরেজ থাকতে পারে।

### অন্যান্য কাঠামোর সাথে সম্পর্ক

Msg ফাইল ফরম্যাটের অন্যান্য কাঠামোর সাথে নিম্নলিখিত সম্পর্ক রয়েছে:

* .msg এর ভিত্তি হল যৌগিক ফাইল বাইনারি ফাইল ফরম্যাট।

* মেসেজ এবং অ্যাটাচমেন্ট অবজেক্ট প্রোটোকল দ্বারা ব্যবহৃত বৈশিষ্ট্যগুলি এই বিন্যাস দ্বারা ব্যবহৃত হয়।


## এমএসজি ফরম্যাট এড়ানোর জন্য দৃশ্যকল্প

মেসেজ অবজেক্ট ক্লায়েন্ট বা মেসেজ স্টোরের মধ্যে শেয়ার করা যেতে পারে যারা .msg ফাইল সিস্টেম ব্যবহার করে। এমন কিছু পরিস্থিতিতে আছে যেখানে .msg ফাইল ফরম্যাটে একটি বার্তা বস্তু সংরক্ষণ করা উপযুক্ত হবে না। উদাহরণ স্বরূপ:

* একটি বৃহৎ স্বতন্ত্র সংরক্ষণাগার বজায় রাখার ক্ষেত্রে, একটি পূর্ণ-বৈশিষ্ট্যযুক্ত বিন্যাস ব্যবহার করা ভাল যেখানে দৃশ্যগুলি আরও সুনির্দিষ্টভাবে রেন্ডার করা যেতে পারে।

* যদি রিসিভার অজানা হয়, তাহলে এটা সম্ভব যে ফরম্যাটটি রিসিভার শেষ দ্বারা সমর্থিত নয় এবং ব্যক্তিগত বা অপ্রাসঙ্গিক বিতরণ করা হতে পারে।


## MSG ফাইলের উদাহরণ

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## তথ্যসূত্র

* [[MS-OXMSG]: Outlook MSG ফাইল ফরম্যাট](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


