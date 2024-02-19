{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CFML - কোল্ডফিউশন মার্কআপ ল্যাঙ্গুয়েজ ফাইল",
  "description": "একটি CFML ফাইল এবং API যা CFML ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfml-bn"
    }
  },
  "lastmod": "2021-08-19"
}

## একটি CFML ফাইল কি?

.cfml এক্সটেনশন সহ একটি ফাইল হল একটি ColdFusion Markup Language ফাইল যা ওয়েব পেজ তৈরি করতে ব্যবহৃত হয়। এটি প্রোগ্রামার দ্বারা কোল্ডফিউশন অ্যাপ্লিকেশন কীভাবে তৈরি করা হবে তা নির্ধারণ করতে ব্যবহৃত নিয়মগুলির একটি সেট বোঝায়। ColdFusion হল একটি প্রোগ্রামিং ভাষা যা দ্রুত এবং অন্যান্য প্রযুক্তি যেমন [ASP](/web/asp/), [PHP](/programming/php/) ইত্যাদির তুলনায় কম সময়ে বিচ্ছিন্ন ওয়েব অ্যাপ্লিকেশন তৈরি করতে ব্যবহৃত হয়৷ কিছু অ্যাপ্লিকেশন যা CML ফাইল খুলতে পারে তার মধ্যে রয়েছে Adobe ColdFusion 2018, Adobe ColdFusion Builder, এবং Adobe Dreamweaver.

## CFML ফাইল ফরম্যাট - আরও তথ্য

CFML ফাইল হল মার্কআপ ফাইল এবং ট্যাগ আকারে ওয়েব উপাদান ধারণ করে। এগুলি এমন টেক্সট ফাইল যা যেকোনো টেক্সট এডিটরে খোলা এবং এডিট করা যায়। CFML ফাইলে কয়েকটি ট্যাগ থাকে যা [HTML](/web/html/) এর মতো এবং সাধারণত একটি খোলা এবং বন্ধ করার ট্যাগ নিয়ে গঠিত। এই ট্যাগগুলিতে এক বা একাধিক বৈশিষ্ট্য থাকতে পারে।

### ট্যাগ সিনট্যাক্স

CFML ট্যাগের সাধারণ সিনট্যাক্স নিচে দেওয়া হল।

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

বেশিরভাগ ট্যাগ বৈশিষ্ট্যগুলি গ্রহণ করে এবং অনুসরণ হিসাবে সংজ্ঞায়িত করা হয়।

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

এই ট্যাগগুলির মধ্যে কিছু নিম্নলিখিত সিনট্যাক্স সহ একাধিক বৈশিষ্ট্য গ্রহণ করে।

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML কোড উদাহরণ

এখানে একটি উদাহরণ যা একটি প্রকৃত CFML ট্যাগ ব্যবহার করে - `cfoutput` ট্যাগ:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## তথ্যসূত্র

* [কোল্ডফিউশন](https://www.quackit.com/coldfusion/tutorial/)


