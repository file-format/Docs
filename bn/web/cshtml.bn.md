{
  "date": "2019-10-11",
  "keywords": [
    "cshtml",
    "cshtml file",
    "cshtml file format",
    "cshtml file type",
    "file",
    "type",
    "what is a cshtml file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CSHTML - ASP.NET রেজার ওয়েবপেজ",
  "description": "সিএসএইচটিএমএল ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা CSHTML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtml-bn"
    }
  },
  "lastmod": "2021-04-29"
}

## একটি CSHTML ফাইল কি?

.cshtml এক্সটেনশন সহ একটি ফাইল হল একটি [C#](/programming/cs/) HTML ফাইল যা ব্যবহারকারীর ব্রাউজারে ওয়েবপৃষ্ঠা ফাইলগুলি রেন্ডার করতে রেজার মার্কআপ ইঞ্জিন দ্বারা সার্ভারের পাশে ব্যবহার করা হয়। এই সার্ভার সাইড কোডিং স্ট্যান্ডার্ড ASP.NET পৃষ্ঠার অনুরূপ যা ওয়েবপেজটি ব্রাউজারে লেখা হওয়ার সাথে সাথে ফ্লাইতে গতিশীল ওয়েব সামগ্রী তৈরি করতে সক্ষম করে। সার্ভার উত্পন্ন পৃষ্ঠাটি ব্রাউজারে পাঠানোর আগে পৃষ্ঠার ভিতরে সার্ভার-সাইড কোডটি কার্যকর করে। জটিল কাজ যেমন ডাটাবেস অ্যাক্সেস করা এবং জটিল ভিউ রেন্ডার করা। CSHTML ফাইলগুলি মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও ব্যবহার করে তৈরি এবং প্রোগ্রাম করা যেতে পারে।

## CSHTML ফাইল ফরম্যাট

CSHTML ফাইল হল টেক্সট ফাইল যা রেজার মার্কআপ ইঞ্জিন দ্বারা বর্ণিত সিনট্যাক্স অনুসরণ করে। রেজার C# এবং VB.NET উভয়কেই সমর্থন করে এবং এটি ক্লাসিক ASP এবং ASP.NET-এর তুলনায় শেখা এবং ব্যবহার করা সহজ। রেজারের [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) কোডিং-এর জন্য w3schools-এ একটি সহজ অথচ কার্যকরী নির্দেশিকা রয়েছে৷

### CSHTML উদাহরণ

রেজারের জন্য একটি CSHTML ফাইলে ব্যবহৃত C# কোডের উদাহরণ নিচে দেওয়া হল।

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

রেজারের জন্য সমতুল্য VB.NET কোডটি নিম্নরূপ।

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## তথ্যসূত্র

* [রেজার সিনট্যাক্স রেফারেন্স - মাইক্রোসফ্ট](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


