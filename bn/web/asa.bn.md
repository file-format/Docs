{
  "date": "2021-12-09",
  "keywords": [
    "asa",
    ".asa",
    "file format",
    "file type",
    "what is a .asa file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASA - ASP কনফিগারেশন ফাইল",
  "description": "একটি ASA ফাইল এবং APIগুলি কী যেগুলি ASA ফাইলগুলি তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-bn"
    }
  },
  "lastmod": "2021-12-09"
}

## একটি ASA ফাইল কি?

একটি ASA ফাইল হল কনফিগারেশন ফাইল, [ASP](/web/asp/)/ASP.NET প্রকল্পগুলির জন্য তৈরি করা হয়েছে৷ এটিতে ভেরিয়েবল, ধারণ এবং ফাংশনগুলির ঘোষণা রয়েছে যা অ্যাপ্লিকেশনটিতে গ্লোবাল লেভেলে অ্যাক্সেসযোগ্য। প্রকল্পের সমস্ত পৃষ্ঠাগুলি এই ভেরিয়েবল এবং ফাংশনগুলি অ্যাক্সেস করতে পারে, এইভাবে এইগুলি পুনরায় লেখার প্রয়োজনীয়তা এড়ানো যায়। এরকম একটি উদাহরণ হল Global.asa পৃষ্ঠা যা অন্যান্য ASP ওয়েবসাইট পৃষ্ঠাগুলির দ্বারা অ্যাক্সেসযোগ্য হওয়ার জন্য রুট ডিরেক্টরিতে সংরক্ষণ করা হয়। Global.asa ফাইলগুলি ঐচ্ছিক, কিন্তু ব্যবহার করা হলে, প্রতিটি অ্যাপ্লিকেশনে শুধুমাত্র একটি Global.asa ফাইল থাকতে পারে।

## ASA ফাইল ফরম্যাট - আরও তথ্য

ASA ফাইল হল নিম্নোক্ত তথ্য সহ প্লেইন টেক্সট ফাইল।

 * অ্যাপ্লিকেশন ইভেন্ট
 * সেশন ইভেন্ট
 * \<object> ঘোষণা
 * টাইপলাইব্রেরি ঘোষণা
 * নির্দেশিকা অন্তর্ভুক্ত করুন

## ASA ফাইলের উদাহরণ

একটি Global.asa ফাইল এই মত কিছু দেখতে পারে.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## তথ্যসূত্র

* [ASP Global.asa ফাইল - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


