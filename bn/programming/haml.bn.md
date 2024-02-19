{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HAML ফাইল ফরম্যাট - হ্যামল সোর্স কোড ফাইল",
  "description": "HAML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা HAML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-haml-bn"
    }
  },
  "lastmod": "2022-04-07"
}

## একটি HAML ফাইল কি?

একটি HAML ফাইল হল একটি HTML বিমূর্ততা মার্কআপ ভাষা ফাইল যাতে সোর্স কোড [Haml](https://haml.info/) ভাষায় লেখা থাকে। এটি ERB (রুবি টেমপ্লেট স্ক্রিপ্ট) এর প্রতিস্থাপন হিসাবে ব্যবহার করা যেতে পারে। HAML ফাইলে টেমপ্লেট সোর্স কোড থাকে যা একটি ওয়েব ডকুমেন্টের HTML তৈরি করার জন্য। ফাইলের এক্সটেনশন পরিবর্তন করে ERB ফাইলগুলিকে শুধুমাত্র অ্যাপ/ভিউ ফোল্ডারে হ্যামলে প্রতিস্থাপন করে প্রতিস্থাপন করা যেতে পারে। HAML ফাইলগুলি যেকোন টেক্সট এডিটর যেমন Microsoft Notepad, Notepad++, Apple TextEdit, দিয়ে খোলা যায়

## HAML ফাইল ফরম্যাট

HAML ফাইলগুলি হল সোর্স ফাইল যা ডিস্কে প্লেইন টেক্সট ফাইল হিসাবে সংরক্ষিত হয়। এতে HAML সিনট্যাক্সে লেখা কোড রয়েছে। HAML **<>** ট্যাগগুলিকে **%** চিহ্ন দিয়ে প্রতিস্থাপন করে যাতে কোড সহজ ও সহজ হয়। ERB ফাইলগুলি HAML দ্বারা ড্রপ-ইন প্রতিস্থাপনযোগ্য যেমন নিম্নলিখিত সহজ উদাহরণে দেখানো হয়েছে।

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML উদাহরণ

নিম্নে HAML-এর Hello World উদাহরণ হল।

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
যা নিম্নলিখিত HTML আউটপুটে রেন্ডার করে।

```
<p class="sample" id="welcome">Hello, World!</p>
```

## তথ্যসূত্র

* [HAML - Github](https://github.com/haml/haml)


