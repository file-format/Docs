{
  "date": "2021-05-24",
  "keywords": [
    "xul",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "XML User Interface Language"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "XUL - XML ইউজার ইন্টারফেস ল্যাঙ্গুয়েজ ফাইল",
  "description": "XUL ফাইল ফর্ম্যাট এবং API সম্পর্কে জানুন যেগুলি XUL ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xul-bn"
    }
  },
  "lastmod": "2021-05-24"
}

## একটি XUL ফাইল কি?

একটি .xul এক্সটেনশন সহ একটি ফাইল ([XUL](https://wiki.mozilla.org/XUL:Home_Page) হল XML ইউজার ইন্টারফেস ল্যাঙ্গুয়েজ) একটি [XML](/web/xml/) ভিত্তিক মার্কআপ ল্যাঙ্গুয়েজ ফাইল ইউজার ইন্টারফেস তৈরি করার জন্য। এটি মজিলা দ্বারা ডেভেলপারদের জন্য গ্রাফিকাল ইউজার ইন্টারফেস উপাদান তৈরি করার জন্য তৈরি করা হয়েছিল যা ওয়েব পেজ তৈরির জন্য ব্যবহৃত অন্যান্য মার্কআপ ভাষার মতো। XUL মোজিলা তার ফায়ারফক্স ব্রাউজারে ব্যাপকভাবে ব্যবহার করছে যেখানে এটি মোজিলা কোডবেস ব্যবহার করেছে। XUL রেন্ডারিং ব্যবহার করে বাহিত হয়
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software))। ফায়ারফক্স ফর্ক যেমন প্যাল মুন, ব্যাসিলিস্ক, এবং ওয়াটারফক্স XUL অ্যাড-অনগুলির জন্য সমর্থন বজায় রাখে। XUL ফাইলগুলিকে MIME প্রকার দ্বারা চিহ্নিত করা হয়: application/vnd.mozilla.xul+xml।

## XUL ফাইল বিন্যাস

XUL ফাইলগুলি XML ফাইল ফর্ম্যাটের উপর ভিত্তি করে প্লেইন টেক্সটে লেখা হয় এবং Gecko ইঞ্জিন ব্যবহার করে রেন্ডার করা হয়। একটি XUL কাঠামোর তিনটি প্রধান অংশ হল:

 * সামগ্রী' - এর মধ্যে উইন্ডোর ঘোষণা এবং তাদের মধ্যে থাকা ব্যবহারকারী ইন্টারফেস উপাদান অন্তর্ভুক্ত রয়েছে।
 * `স্কিন` - এতে যেকোনো স্টাইল শীট, ছবি এবং অন্যান্য থিম সম্পর্কিত ফাইল রয়েছে। একটি উইন্ডোর চেহারা শৈলী শীট বর্ণনা করা হয়।
 * `লোকেল` - একটি উইন্ডোর মধ্যে প্রদর্শিত টেক্সট আলাদাভাবে সংরক্ষণ করা হয় এবং একাধিক সেট ভাষার ফাইল ব্যবহারকারীরা ব্যবহার করতে পারেন।

### XUL উদাহরণ

নিম্নলিখিত উদাহরণটি তিনটি বোতাম তৈরি করে যা একে অপরের উপরে উল্লম্ব দিক থেকে স্ট্যাক করা হয়।

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## তথ্যসূত্র

* [XUL - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/XUL)

* [XUL আর্কাইভড ডকুমেন্টেশন - মজিলা দ্বারা](https://wiki.mozilla.org/XUL:Home_Page)


