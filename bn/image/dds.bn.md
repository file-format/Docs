{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DDS ফাইল ফরম্যাট- ডাইরেক্ট ড্র সারফেস ইমেজ ফাইল",
  "description": "DDS ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DDS ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dds-bn"
    }
  },
  "lastmod": "2022-04-02"
}

## একটি DDS ফাইল কি?

একটি ডিডিএস ফাইল হল একটি রাস্টার ইমেজ ফাইল যা ডাইরেক্ট ড্র সারফেস (ডিডিএস) কন্টেইনার ফর্ম্যাট ব্যবহার করে। এটি সংকুচিত এবং সংকুচিত (DXTn) টেক্সচার সংরক্ষণ করে এবং বিভিন্ন ধরণের ডেটা সংরক্ষণের জন্য বিভিন্ন ধরণের প্রয়োগ করে। এটি বিভিন্ন ধরণের ডেটা যেমন একক স্তর টেক্সচার, মিপম্যাপ সহ টেক্সচার, কিউব ম্যাপ, ভলিউম ম্যাপ এবং টেক্সচার অ্যারে সমর্থন করে। এটি ডিডিএস ফাইলগুলিকে ডিজিটাল ফটো এবং উইন্ডোজ ডেস্কটপ ব্যাকগ্রাউন্ড ছাড়াও ভিডিও গেম টেক্সচার ইউনিট মডেলগুলি সংরক্ষণ করতে সক্ষম করে। ডিডিএস ফাইল ফরম্যাটটি মাইক্রোসফট দ্বারা ডাইরেক্টএক্স এসডিকে ব্যবহার করার জন্য তৈরি করা হয়েছিল।

## DDS ফাইল ফরম্যাট

DDS ফাইলগুলি বাইনারি ফাইল হিসাবে সংরক্ষণ করা হয় এবং DirectX SDK এর সাথে ব্যবহার করা যেতে পারে। এটি 3D গেমের মতো রিয়েল-টাইম রেন্ডারিং অ্যাপ্লিকেশনগুলি বিকাশ করতে DirectX এর শক্তি ব্যবহার করে।

### DDS ফাইল লেআউট

[DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) বিস্তারিতভাবে Microsoft দ্বারা নথিভুক্ত করা হয়েছে৷ একটি বাইনারি ডিডিএস ফাইলে নিম্নলিখিত তথ্য রয়েছে।

 * একটি DWORD (জাদু নম্বর) যেখানে চারটি অক্ষরের কোড মান 'DDS' (0x20534444) রয়েছে।
 * A description of the data in the file.

DDS_HEADER ডেটা বর্ণনা করে এবং DDS_PIXELFORMAT পিক্সেল বিন্যাস বর্ণনা করে। এগুলি উভয়ই অবহেলিত DDSURFACEDESC2, DDSCAPS2 এবং DDPIXELFORMAT DirectDraw 7 কাঠামো প্রতিস্থাপন করে।

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) এই ফাইল ফরম্যাটের প্রযুক্তিগত বিশদ বিবরণ আরও বিস্তৃত করে৷

## তথ্যসূত্র

* [DDS - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [ZSoft PCX ফাইল ফরম্যাট টেকনিক্যাল রেফারেন্স ম্যানুয়াল](http://qzx.com/pc-gpe/pcx.txt)


