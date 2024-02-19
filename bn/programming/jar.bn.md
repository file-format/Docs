{
  "date": "2019-10-11",
  "keywords": [
    "JAR",
    ".jar",
    "what is a jar file",
    "how to open a jar file",
    "extension",
    "file",
    "jar file",
    "jar file format",
    ".jar extension"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "JAR - জাভা আর্কাইভ ফাইল ফরম্যাট",
  "description": "JAR ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা JAR ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jar-bn"
    }
  },
  "lastmod": "2020-09-10"
}

## একটি JAR ফাইল কি?

.jar এক্সটেনশন সহ একটি ফাইল হল একটি জাভা আর্কাইভ ফাইল যাতে একটি একক ফাইল হিসাবে বিভিন্ন অ্যাপ্লিকেশন সম্পর্কিত ফাইল থাকে। একাধিক HTTP সংযোগ তৈরি করা এড়িয়ে HTTP লেনদেনের মাধ্যমে ব্রাউজারে ডাউনলোড করা জাভা অ্যাপলেট লোড করার গতি কমাতে এই ফাইল বিন্যাসটি তৈরি করা হয়েছে। একটি একক JAR ফাইলে জাভা ক্লাস ফাইল ([.class](/programming/class/)), [images](/image/), এবং [sounds](/audio/) থাকতে পারে৷ একটি JAR ফাইলের মধ্যে থাকা স্বতন্ত্র আইটেমগুলি তাদের উত্স প্রমাণীকরণের জন্য অ্যাপ্লিকেশন বিকাশকারী দ্বারা ডিজিটালভাবে স্বাক্ষরিত হতে পারে। JAR ফাইলগুলি নিয়মিতভাবে কার্যকরী API তৈরি করতে ব্যবহৃত হয় যা সেই API এর সাথে সম্পর্কিত নির্দিষ্ট কার্যকারিতা ধারণ করে।

## JAR ফাইল ফরম্যাট

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### ম্যানিফেস্ট ফাইল

যখন একটি JAR ফাইল তৈরি করা হয়, তখন একটি ম্যানিফেস্ট ফাইল স্বয়ংক্রিয়ভাবে এর ভিতরে তৈরি হয় যাতে JAR ফাইলের বিষয়বস্তু সম্পর্কে মেটাডেটা তথ্য থাকে। এই ফাইলটি JAR ফাইলের ভিতরে প্যাকেজ করা বিষয়বস্তু দেখায়। একটি সাধারণ ম্যানিফেস্ট ফাইল অনুসরণ করে দেখায় যা JAR ফাইলে অন্তর্ভুক্ত ফোল্ডার এবং ক্লাসগুলি দেখায়।

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### ম্যানিফেস্ট স্পেসিফিকেশন

ম্যানিফেস্ট স্পেসিফিকেশন ওরাকল দ্বারা অনুসরণ করা হয়েছে।

`manifest-file`: প্রধান-বিভাগের নতুন লাইন \ব্যক্তি-বিভাগ

`প্রধান-বিভাগ`: সংস্করণ-তথ্য নতুন লাইন \প্রধান-বিশিষ্ট

`সংস্করণ-তথ্য`: ম্যানিফেস্ট-সংস্করণ : সংস্করণ-সংখ্যা

`সংস্করণ-সংখ্যা` : অঙ্ক+{.digit+}*

`main-attribute`: (যে কোনো বৈধ প্রধান বৈশিষ্ট্য) নতুন লাইন

`ব্যক্তি-বিভাগ`: নাম : মান নিউলাইন \পেরেন্ট্রি-অ্যাট্রিবিউট

`perentry-attribute`: (যেকোনো বৈধ perentry অ্যাট্রিবিউট) নতুন লাইন

`নতুনরেখা` : CR LF | LF | CR (LF দ্বারা অনুসরণ করা হয় না)

`সংখ্যা`: {0-9}

### এক্সিকিউটেবল JAR

JAR ফাইলগুলিতে এমন একটি অ্যাপ্লিকেশনও থাকতে পারে যা জাভা ভার্চুয়াল মেশিন (JVM) দ্বারা চালানো যেতে পারে মাইক্রোসফ্ট উইন্ডোজ অপারেটিং সিস্টেমের অন্য যেকোনো অ্যাপ্লিকেশনের মতো। এই ক্ষেত্রে, JVM-কে অ্যাপ্লিকেশনের এন্ট্রি পয়েন্ট সম্পর্কে জানতে হবে যেটি একটি পাবলিক স্ট্যাটিক ভ্যাইড মেইন পদ্ধতি সহ যেকোনো ক্লাস। ম্যানিফেস্ট ফাইল নিম্নলিখিত বিন্যাসে `প্রধান-শ্রেণি` শিরোনাম সহ এমন একটি শ্রেণী চিহ্নিত করে:

```
Main-Class: com.example.MyClassName
```



## তথ্যসূত্র

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR ফাইল ফরম্যাট](https://en.wikipedia.org/wiki/JAR_(file_format))

