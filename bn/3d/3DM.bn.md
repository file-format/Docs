{
  "date": "2021-08-13",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "3DM",
  "description": "3DM ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা 3DM ফাইল খুলতে এবং তৈরি করতে পারে।",
  "linktitle": "3DM",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3DM-bn"
    }
  },
  "lastmod": "2021-08-13"
}

## একটি 3DM ফাইল কি?

.3dm এক্সটেনশন সহ একটি ফাইল একটি ওপেন-সোর্স ফাইল বিন্যাস যা 3D গ্রাফিক্স সফ্টওয়্যারের জন্য ব্যবহৃত হয়। এটিতে 3D মডেলের সাথে তাদের নির্ভরশীল উপাদান যেমন পৃষ্ঠ, বিন্দু এবং বক্ররেখার তথ্য রয়েছে। অ্যাপ্লিকেশানগুলির মধ্যে 3-ডি জ্যামিতি সঠিকভাবে স্থানান্তর করার জন্য 3DM ফাইল ফর্ম্যাটটি [openNURBS](https://github.com/mcneel/opennurbs) উদ্যোগের দ্বারা তৈরি করা হয়েছিল৷ 3DM ফাইল খোলা এবং রূপান্তর করা যেতে পারে অ্যাপ্লিকেশন যেমন Rhinoceros, SAP VEViewer, Moment of Inspiration, এবং Right Hemisphere Deep View।

## 3DM ফাইল ফরম্যাট

[openNURBS](https://github.com/mcneel/opennurbs), একটি ওপেন-সোর্স টুলকিট, 3DM ফাইল ফরম্যাট স্পেসিফিকেশন, ডকুমেন্টেশন, C++ সোর্স কোড লাইব্রেরি এবং .NET 2.0 অ্যাসেম্বলি ফাইল ফরম্যাট পড়তে ও লিখতে ধারণ করে।

### 3DM উদাহরণ ফাইল

কিছু উদাহরণ 3DM ফাইল openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) বিভাগ থেকে ডাউনলোড করা যেতে পারে। এগুলি openNURBS টুলকিট ব্যবহার করে লোড এবং প্রদর্শন করা যেতে পারে।

## কিভাবে 3DM ফাইল পড়তে বা লিখতে হয়?

[openNURBS](https://github.com/mcneel/opennurbs) লাইব্রেরি রাইনোর প্রয়োজন ছাড়াই যে কাউকে 3DM ফাইল ফরম্যাট পড়তে এবং লিখতে দেয়৷ এটি একটি লাইব্রেরির জন্য C++ সোর্স কোড প্রদান করে যা openNURBS ফাইল ফরম্যাট ব্যবহার করে 3D মডেল পড়তে এবং লিখবে। এই টুলকিটটি NURBS মূল্যায়ন সরঞ্জাম এবং প্রাথমিক জ্যামিতিক এবং 3D ভিউ ম্যানিপুলেশন সরঞ্জামের পাশাপাশি বেশ কয়েকটি উদাহরণ প্রোগ্রামের জন্য সোর্স কোডও প্রদান করে। [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) সমর্থন ফোরাম হল একটি সমৃদ্ধ বিষয়বস্তু এবং 3DM সম্প্রদায়ের সমস্যাগুলি ভাগ করে নেওয়ার এবং সমাধান পেতে আলোচনার জায়গা৷

## তথ্যসূত্র ##

* [গণ্ডার](https://www.rhino3d.com/download/openNURBS)

* [গণ্ডার - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Rhinoceros_3D)

* [GitHub-এ openNURBS](https://github.com/mcneel/opennurbs)


