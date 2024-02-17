{
  "date": "2023-05-16",
  "keywords": [
"sami ফাইল",
"একটি সামি ফাইল কি?",
"সামি ফাইলের উদাহরণ",
"ফাইল",
"সামি ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI ফাইল ফরম্যাট - সাবটাইটেল এবং মেটাডেটা ইন্টারচেঞ্জ ফাইল",
  "description": "SAMI ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি SAMI ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-bn",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## একটি SAMI ফাইল কি?

.sami এক্সটেনশন সহ একটি ফাইল সাধারণত একটি সাবটাইটেল এবং মেটাডেটা ইন্টারচেঞ্জ (SAMI) ফাইলকে বোঝায়। SAMI হল একটি ক্যাপশনিং ফর্ম্যাট যা ভিডিওতে সাবটাইটেল বা বন্ধ ক্যাপশন প্রদর্শনের জন্য ব্যবহৃত হয়। এটি মূলত মাইক্রোসফট তাদের উইন্ডোজ মিডিয়া প্লেয়ারের জন্য তৈরি করেছে।

SAMI ফাইলগুলিতে সাবটাইটেল বা ক্লোজড ক্যাপশনের জন্য সময় সংক্রান্ত তথ্য এবং পাঠ্য বিষয়বস্তু থাকে, যা তাদের একটি ভিডিও প্লেব্যাকের সাথে সিঙ্ক্রোনাইজ করার অনুমতি দেয়। বিন্যাসটি মৌলিক বিন্যাস বিকল্পগুলিকে সমর্থন করে যেমন ফন্ট শৈলী, রঙ এবং স্ক্রিনে সাবটাইটেলগুলির অবস্থান।

SAMI ফাইলগুলি সাধারণত সাধারণ পাঠ্য ফাইল এবং একটি পাঠ্য সম্পাদক ব্যবহার করে খোলা এবং সম্পাদনা করা যায়। একটি SAMI ফাইলের বিষয়বস্তুতে সাধারণত একটি শিরোনাম বিভাগ অন্তর্ভুক্ত থাকে যা ফাইল সম্পর্কে তথ্য প্রদান করে, যার পরে তাদের নিজ নিজ সময় এবং পাঠ্য সহ পৃথক সাবটাইটেল এন্ট্রি থাকে।

একটি SAMI ফাইল দেখতে কেমন হতে পারে তার একটি উদাহরণ এখানে দেওয়া হল:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI ফাইলগুলি সাধারণত ভিডিও প্লেয়ার বা মিডিয়া প্লেয়ারগুলির সাথে একত্রে ব্যবহৃত হয় যা সাবটাইটেল প্রদর্শন সমর্থন করে, যেমন Windows Media Player বা VLC Media Player৷ প্লেয়ারটি SAMI ফাইলটি পড়ে এবং ভিডিও সামগ্রীর সাথে সাবটাইটেলগুলিকে সিঙ্ক্রোনাইজ করে, ভিডিও দেখার সময় দর্শকদের ক্যাপশন পড়তে দেয়৷

## সমর্থিত HTML ট্যাগ

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` মূল উপাদান যা সমগ্র SAMI ফাইলকে এনক্যাপসুলেট করে।
- ``<HEAD> :`` SAMI ফাইলের জন্য হেডার তথ্য রয়েছে।
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` আবদ্ধ পাঠ্যের জন্য ফন্ট বৈশিষ্ট্য সংজ্ঞায়িত করে। রঙ, মুখ, আকার এবং শৈলীর মতো বৈশিষ্ট্যগুলি ফন্টের চেহারা পরিবর্তন করতে ব্যবহার করা যেতে পারে।</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` মোটা অক্ষরে আবদ্ধ পাঠ্য রেন্ডার করে।</b>
- `` <I>:`` আবদ্ধ পাঠ্যটিকে তির্যক ভাষায় রেন্ডার করে।</i>
- `` <U>:`` আন্ডারলাইন করা বদ্ধ পাঠ রেন্ডার করে।</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

এগুলি SAMI ফাইলগুলির দ্বারা সমর্থিত কিছু মৌলিক ট্যাগ৷ এটা মনে রাখা গুরুত্বপূর্ণ যে SAMI HTML ট্যাগ এবং বৈশিষ্ট্যের সম্পূর্ণ পরিসর সমর্থন করে না। সমর্থিত ট্যাগগুলি মূলত বিস্তৃত নথির কাঠামো বা ইন্টারঅ্যাক্টিভিটি প্রদানের পরিবর্তে সাবটাইটেলগুলির স্টাইলিং এবং অবস্থানের উপর দৃষ্টি নিবদ্ধ করে।

## তথ্যসূত্র
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


