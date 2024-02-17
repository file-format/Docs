
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4র্থ ফাইল - ফোর্থ ল্যাঙ্গুয়েজ ফাইল ফরম্যাট",
  "description":"উদাহরণ সহ .4র্থ ফাইল ফরম্যাট কি এবং এপিআই যা 4র্থ ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন।",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-bn",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## একটি 4র্থ ফাইল কি?

.4র্থ ফাইল এক্সটেনশন সহ একটি ফাইল হল একটি প্রোগ্রামিং ফাইল যা **ফোর্থ প্রোগ্রামিং ল্যাঙ্গুয়েজ** এর জন্য তৈরি করা হয়েছে। এটি ফরথ প্রোগ্রামিং ভাষায় লেখা প্রোগ্রামগুলির জন্য সোর্স কোড ধারণ করে এবং যখন প্রোগ্রামটি কার্যকর করা হয় তখন আউটপুট তৈরি করে। এটি শুধুমাত্র [C](/programming/c/) এবং [C++](/programming/cpp/) সোর্স ফাইলের অনুরূপ অন্য একটি প্রোগ্রামিং ভাষা ফাইল।

## 4র্থ ফাইল ফরম্যাট - আরও তথ্য


### ৪র্থ প্রোগ্রামিং ল্যাঙ্গুয়েজ কোডের উদাহরণ

এখানে Forth-এ লেখা একটি সাধারণ প্রোগ্রামের একটি উদাহরণ রয়েছে যা একটি প্রদত্ত সংখ্যার ফ্যাক্টরিয়াল গণনা করে:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * স্ট্যাকের উপরে দুটি মান গুণ করে। যদি এবং শুরু/পর্যন্ত গঠন প্রোগ্রামের প্রবাহ নিয়ন্ত্রণ করে।

এই প্রোগ্রামটি ব্যবহার করার জন্য, আপনি ফরথ ইন্টারপ্রেটারে সংজ্ঞাটি প্রবেশ করাবেন এবং তারপর আপনি যে নম্বরটির ফ্যাক্টরিয়াল খুঁজে পেতে চান তার সাথে ফ্যাক্টোরিয়াল শব্দটিকে কল করুন:

```
10 factorial .
```
এর ফলে আউটপুট 3628800 হবে, যা 10 এর ফ্যাক্টরিয়াল।

## তথ্যসূত্র

 * [ফোর্থ প্রোগ্রামিং ভাষা](https://en.wikipedia.org/wiki/Forth_(programming_language))

