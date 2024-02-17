{
  "date" : "2021-06-24",
  "keywords" : [ "RSS", "partial", "extension", "file", "format", "web", "Really Simple Syndication","Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" : "আরএসএস - সত্যিই সহজ সিন্ডিকেশন",
  "description":"আরএসএস ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা আরএসএস ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## একটি RSS ফাইল কি? ##

.rss এক্সটেনশন সহ একটি ফাইল রিয়েলি সিম্পল সিন্ডিকেশন নামে পরিচিত। আরএসএস হল কম্পিউটার দ্বারা সহজে বা সহজে পঠিত ফাইলের ধরন, XML ফাইল। এই এক্সএমএল ফাইলগুলি স্বয়ংক্রিয়ভাবে ডেটা বা ওয়েবসাইট বা ওয়েবপৃষ্ঠার আপডেটের যেকোনো পরিবর্তনের সাথে আপডেট হয়। মেটাডেটা (লেখকের নাম, প্রকাশকের নাম, প্রকাশের তারিখ, ইত্যাদি) সহ আপডেট করা তথ্য এবং ওয়েবসাইটের অন্যান্য ওয়েব বিষয়বস্তু ব্যবহারকারীর আরএসএস ফাইল দ্বারা নিষ্কাশন করা হয় এবং সহজে-পঠনযোগ্য বিন্যাসে উপস্থাপন করা হয়। এই RSS ফাইলগুলির সর্বোত্তম বৈশিষ্ট্য হল যে এটি রিয়েল-টাইমে কাজ করে এবং আপডেট, খবর, প্রকাশ, যা সর্বশেষ, ফাইলের শীর্ষে প্রদর্শিত হয়। একটি RSS ফাইল ব্যবহার করে, আপনি সহজেই ওয়েব থেকে সম্পর্কিত বিষয়বস্তু টেনে এবং একটি RSS ফাইল ব্যবহার করে এটি পড়ার মাধ্যমে আপনার আগ্রহের যেকোনো বিষয়ের সর্বশেষ আপডেট সহ একটি ফাইল তৈরি করতে পারেন।

## সংক্ষিপ্ত ইতিহাস ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. দুটি ফাইলের কার্যপ্রণালী বেশ একই রকম এবং এটা অনুমান করা নিরাপদ যে RSS-এর ধারণাটি RDF-এর কাজের উপর ভিত্তি করে গঠিত হয়েছিল, একটি ফাইল রিডার যা মেটাডেটা সংগ্রহ করতে ব্যবহৃত হয়েছিল।

## প্রযুক্তিগত স্পেসিফিকেশন ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. বিভিন্ন RSS ফাইলের বিভিন্ন সংস্করণ রয়েছে, যেমন 0.91, 0.92, 2.0, অন্যদের মধ্যে। প্রতিটি সংস্করণের ফাইল সেই নির্দিষ্ট সংস্করণের বৈশিষ্ট্য এবং মানগুলির সাথে সামঞ্জস্যপূর্ণ। 

## আরএসএস উদাহরণ ##

নিচে আরএসএস-এর একটি সরলীকৃত উদাহরণ।

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## রেফারেন্স ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
