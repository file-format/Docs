{
  "date": "2021-05-24",
  "keywords": [
    "zul",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "open"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ZUL - ZK ইউজার ইন্টারফেস ফাইল",
  "description": "ZUL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি ZUL ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zul-bn"
    }
  },
  "lastmod": "2021-05-24"
}

## একটি ZUL ফাইল কি?

.zul এক্সটেনশন সহ একটি ফাইল হল একটি ওয়েব ফাইল যা ইউজার ইন্টারফেস মার্কআপ ল্যাঙ্গুয়েজ (ZUML) দিয়ে তৈরি এবং এতে ব্যবহারকারীর ইন্টারফেস উপাদানগুলির সংজ্ঞা রয়েছে। Ajax এবং Java ক্লাস সার্ভার সাইড ফাইল তৈরির জন্য [XML](/web/xml/)-ভিত্তিক ZUML ব্যবহার করে সমর্থন করে। ZUL ফাইল ফরম্যাট ZK দ্বারা তৈরি করা হয়েছে, একটি UI ফ্রেমওয়ার্ক যা আপনাকে JavaScript বা AJAX এর জ্ঞান ছাড়াই ওয়েব এবং মোবাইল অ্যাপ্লিকেশন তৈরি করতে সক্ষম করে।

## ZUL ফাইল ফরম্যাট

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL উদাহরণ

ZUML কোডের নিম্নলিখিত উদাহরণে, প্রথম লাইনটি পৃষ্ঠার শিরোনামটি নির্দিষ্ট করে, দ্বিতীয় লাইনটি শিরোনাম এবং সীমানা সহ একটি রুট উপাদান তৈরি করে এবং তৃতীয় লাইনটি লেবেল এবং একটি ইভেন্ট লিসেনার সহ একটি বোতাম তৈরি করে।

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL স্কিমা https://www.zkoss.org/2005/zul/zul.xsd থেকে ডাউনলোড করা যেতে পারে।
## তথ্যসূত্র

* [ZUL - ZK দ্বারা](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [ZUL স্কিমা](https://www.zkoss.org/2005/zul/zul.xsd)


