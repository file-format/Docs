{
  "date": "2020-11-11",
  "keywords": [
    "NSF",
    "extension",
    "file",
    "file format",
    "Database File Type",
    "Database File Format",
    "Database Files"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "NSF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি NSF ফাইল তৈরি এবং খুলতে পারে।",
  "title": "NSF ফাইল ফরম্যাট - Lotus Notes Database Format",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nsf-bn"
    }
  },
  "lastmod": "2020-08-12"
}

## একটি NSF ফাইল কি?

.nsf (নোটস স্টোরেজ ফ্যাসিলিটি) এক্সটেনশন সহ একটি ফাইল হল একটি ডাটাবেস ফাইল ফর্ম্যাট যা [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino) দ্বারা ব্যবহৃত হয়, যা আগে লোটাস নোট নামে পরিচিত ছিল। এটি বিভিন্ন ধরণের বস্তু যেমন ইমেল, অ্যাপয়েন্টমেন্ট, নথি, ফর্ম এবং ভিউ সংরক্ষণ করার জন্য স্কিমাকে সংজ্ঞায়িত করে। এই সমস্ত তথ্য একটি PST/OST ফাইলের মতো ব্যবসায়িক সহযোগিতার জন্য একটি একক NSF ফাইলে রয়েছে৷ NSF ফাইল খুলতে পারে এমন কিছু অ্যাপ্লিকেশনের মধ্যে রয়েছে IBM Lotus Notes এবং IBM Domino।

## NSF ফাইল ফরম্যাট স্পেসিফিকেশন

NSF ফাইলগুলি বাইনারি প্রকৃতির এবং তাদের স্পেসিফিকেশন জোয়াকিম মেটজ দ্বারা [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc-এ উপলব্ধ। এই বিবরণ অনুযায়ী, একটি NSF ফাইলের মধ্যে রয়েছে:

 * ফাইল হেডার
 * ডাটাবেস হেডার

উপরন্তু, এটি গঠিত:

 * সুপারব্লক
 * বালতি বর্ণনাকারী ব্লক
 * বিটম্যাপ
 * রেকর্ড রিলোকেশন ভেক্টর বালতি
 * সারাংশ buckets
 * অ-সারাংশ বালতি


### NSF ফাইল হেডার

NSF ফাইল হেডার একটি 6 বাইট আকারের। ইহা গঠিত:

|অফসেট|আকার|মান|বর্ণনা|
---|---|---|---|
0|2|0x1a 0x00|স্বাক্ষর|
2|4| |ডাটাবেস হেডার সাইজ|

### ডাটাবেস হেডার

NSD ডাটাবেস হেডারে নিম্নলিখিত নিশ্চিত মান রয়েছে।

 * ডাটাবেস তথ্য
   * ডাটাবেস শনাক্তকারী (DBID)
 * প্রতিলিপি তথ্য
 * ডাটাবেস তথ্য বাফার পতাকা
   * শিরোনাম
   * ক্যাটাগরি
   * ক্লাস
   * ডিজাইন ক্লাস (টেমপ্লেট নাম)
 * বিশেষ নোট শনাক্তকারী
 * প্যাডিং
 * ডাটাবেস তথ্য 2
 * ডাটাবেস তথ্য 3
 * ডাটাবেস তথ্য 4
 * ডাটাবেস তথ্য 5
 * প্যাডিং
 * ডাটাবেস ইনস্ট্যান্স আইডেন্টিফায়ার (DBIID)
 * প্রতিলিপি ইতিহাস

## তথ্যসূত্র

 * [NSF ফরম্যাট - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

