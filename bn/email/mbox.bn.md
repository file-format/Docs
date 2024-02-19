{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MBOX - ইমেল মেইলবক্স ফাইল",
  "description": "MBOX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি MBOX ফাইল তৈরি এবং খুলতে পারে৷",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbox-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি MBOX ফাইল কি?

MBox ফাইল ফরম্যাট হল একটি সাধারণ শব্দ যা ইলেকট্রনিক মেল বার্তা সংগ্রহের জন্য একটি ধারককে উপস্থাপন করে। বার্তাগুলি তাদের সংযুক্তি সহ পাত্রের ভিতরে সংরক্ষণ করা হয়। একটি সম্পূর্ণ ফোল্ডারের বার্তাগুলি একটি একক ডাটাবেস ফাইলে সংরক্ষিত হয় এবং ফাইলের শেষে নতুন বার্তা যুক্ত করা হয়। অসংখ্য অ্যাপ্লিকেশন এবং API MBox ফাইল ফরম্যাটের জন্য সমর্থন প্রদান করে যেমন Apple Mail এবং Mozilla Thunderbird।

## MBOX ফাইল ফরম্যাট ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## MBox ফাইল ## থেকে একটি বার্তা পড়া

একজন পাঠক একটি এমবক্স ফাইলের মাধ্যমে স্ক্যান করে From_ লাইনগুলি খুঁজছেন৷ যেকোনো From_ লাইন একটি বার্তার শুরুকে চিহ্নিত করে। প্রতিটি From_ লাইন (ফাইলের শুরুর অতীত) ফাঁকা লাইনের সুবিধা নেওয়ার চেষ্টা পাঠকের উচিত নয়। একবার পাঠক একটি বার্তা খুঁজে পেলে, এটি From_ লাইনের বাইরে একটি (সম্ভবত দূষিত) খাম প্রেরক এবং বিতরণের তারিখ বের করে। এটি তারপর পরবর্তী From_ লাইন বা ফাইলের শেষ পর্যন্ত পড়া হয়, যেটি প্রথমে আসে। এটি চূড়ান্ত ফাঁকা লাইনটি বন্ধ করে দেয় এবং >From_ লাইন এবং >>From_ লাইন ইত্যাদির উদ্ধৃতি মুছে দেয়। ফলাফল হল একটি RFC 822 বার্তা।

## এনকোডিং বিবেচনা ##

একটি MBox ফাইলের বিষয়বস্তু অপরিবর্তনীয়ভাবে মিশে যেতে পারে যখন প্রাপ্ত একটি ইমেলে সংযুক্তি হিসাবে একটি Mbox ফাইল থাকে এবং অন্য Mbox ফাইলে সংরক্ষণ করা হয়। এটি এড়াতে, মেসেজিং সিস্টেমগুলিকে অবশ্যই অ-স্বচ্ছ স্থানান্তর এনকোডিং সহ একটি এমবক্স ডাটাবেস এনকোড করতে হবে (যেমন BASE64 বা উদ্ধৃত-মুদ্রণযোগ্য) যখনই এই জাতীয় বস্তু বার্তাপ্রেরণ প্রোটোকলের মাধ্যমে স্থানান্তরিত হয়। অ-সম্মতিমূলক ডেটা প্রাপ্ত হলে বাস্তবায়নকারীদের স্থানীয়ভাবে এমবক্স ডেটা এনকোড করার জন্যও প্রস্তুত থাকতে হবে।

## তথ্যসূত্র ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Mbox)


