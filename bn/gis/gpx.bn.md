{
  "date": "2019-10-11",
  "keywords": [
    "gpx file",
    "what is an gpx file",
    "file",
    "gpx example",
    "gpx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GPX - GPX এক্সচেঞ্জ ফাইল ফরম্যাট",
  "description": "GPX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি GPX ফাইল তৈরি এবং খুলতে পারে৷",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpx-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি GPX ফাইল কি?

জিপিএক্স এক্সটেনশন সহ ফাইলগুলি ইন্টারনেটে অ্যাপ্লিকেশন এবং ওয়েব পরিষেবাগুলির মধ্যে জিপিএস ডেটা আদান-প্রদানের জন্য জিপিএস এক্সচেঞ্জ ফর্ম্যাটের প্রতিনিধিত্ব করে। এটি একটি হালকা ওজনের XML ফাইল ফরম্যাট যাতে জিপিএস ডেটা থাকে যেমন ওয়েপয়েন্ট, রুট এবং ট্র্যাকগুলি আমদানি করা হয় এবং একাধিক প্রোগ্রাম দ্বারা লাল করা হয়। GPX ফাইল ফরম্যাট খোলা এবং বিভিন্ন অ্যাপ্লিকেশন এবং GPS ডিভাইস দ্বারা সমর্থিত। এই ধরনের ফাইল থেকে GPS ডেটা ভূ-স্থানিক উদ্দেশ্যে ম্যাপিং অ্যাপ্লিকেশনগুলিতে প্রদর্শনের জন্য লোড করা যেতে পারে।

## GPX ফাইল ফরম্যাট ##

একটি GPX ফাইলে অক্ষাংশ এবং দ্রাঘিমাংশের অবস্থানের ডেটা, উচ্চতার মান এবং অন্যান্য সম্ভাব্য অন্যান্য বর্ণনামূলক তথ্য থাকে। অবস্থান ডেটা দশমিক ডিগ্রী হিসাবে প্রকাশ করা হয় এবং উচ্চতা মিটারে প্রকাশ করা হয়। একটি GPX ফাইলের সময় ISO 8601 ফর্ম্যাট ব্যবহার করে সমন্বিত ইউনিভার্সাল টাইমে (UTC) থাকে। একটি GPX ফাইল ব্যবহার করার সুবিধাগুলি নিম্নরূপ:

* GPX আপনাকে Windows, MacOS, Linux, Palm, এবং PocketPC-এর জন্য ক্রমবর্ধমান প্রোগ্রামগুলির তালিকার সাথে ডেটা আদান-প্রদান করতে দেয়৷

* GPX একটি সাধারণ ওয়েবপেজ বা কনভার্টার প্রোগ্রাম ব্যবহার করে অন্য ফাইল ফরম্যাটে রূপান্তরিত হতে পারে।

* GPX XML স্ট্যান্ডার্ডের উপর ভিত্তি করে তৈরি, তাই আপনি যে নতুন প্রোগ্রামগুলি ব্যবহার করেন তার অনেকগুলি (উদাহরণস্বরূপ, মাইক্রোসফ্ট এক্সেল) GPX ফাইল পড়তে পারে৷

* GPX ওয়েবে যেকোনও ব্যক্তির জন্য নতুন বৈশিষ্ট্যগুলি বিকাশ করা সহজ করে তোলে যা অবিলম্বে আপনার প্রিয় প্রোগ্রামগুলির সাথে কাজ করবে।


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) রেফারেন্সের জন্য GPX ফাইল ফরম্যাটের উপস্থাপনা দেখায়।

### প্রয়োজনীয় তথ্য ###

GPS ডেটা উপস্থাপনের জন্য একটি জিপিএক্স ফাইলের অংশ হিসেবে প্রয়োজনীয় তথ্য নিচে দেওয়া হল।

* **ওয়েপয়েন্টস**: একটি ওয়েপয়েন্ট হল একটি বিন্দুর একটি WGS84 (GPS) স্থানাঙ্ক এবং ওজিআর টাইপের wkbPoint-এর বৈশিষ্ট্যগুলির স্তর উপস্থাপন করে

* **রুট**: ওজিআর টাইপের wkbLineString-এর বৈশিষ্ট্যগুলির একটি স্তর উপস্থাপন করুন। এটিতে ট্র্যাক পয়েন্টগুলির একটি তালিকা রয়েছে, যা একটি বাঁক বা স্টেজ পয়েন্টগুলি দেখায় যা একটি গন্তব্যের দিকে নিয়ে যায়

* **ট্র্যাক**: ট্র্যাকগুলি ওজিআর টাইপের wkbMultiLineString-এর বৈশিষ্ট্যগুলির স্তর উপস্থাপন করে। এটি একটি পথ বর্ণনাকারী পয়েন্টগুলির একটি ক্রমানুসারে তালিকায় ওয়েপয়েন্ট সমন্বিত অন্তত একটি সেগমেন্ট দিয়ে তৈরি। এটি ট্র্যাক পয়েন্টগুলির একটি তালিকা নিয়ে গঠিত যা একটি অবিচ্ছিন্ন GPS ট্র্যাকের প্রতিনিধিত্ব করে।


### GPX উদাহরণ ফাইল ###

নিম্নলিখিত GPX ফাইলটি একটি GPX ফাইলে GPS ডেটার সংগঠন দেখায় এবং একটি GPX ফাইলের বিষয়বস্তু সম্পর্কে ভাল ধারণা দিতে পারে।

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## তথ্যসূত্র ##

* [GPX ফাইল ফরম্যাট](https://www.topografix.com/gpx.asp)

* [GPX - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


