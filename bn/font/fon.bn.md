{
  "date" : "2020-08-20",
  "keywords" : [ "fon file", "fon file format", "what is a fon file", "file", "fon example", "fon file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "FON - ফন্ট লাইব্রেরি ফাইল",
  "description":"FON ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি FON ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## একটি FON ফাইল কি?

.fon এক্সটেনশন সহ একটি ফাইল হল একটি মাইক্রোসফ্ট উইন্ডোজ 3.x ফন্ট লাইব্রেরি যা আসলে একটি এক্সিকিউটেবল ফাইল কিন্তু .fon নামকরণ করা হয়েছে। এটি নিজেই [.fnt](/font/fnt/) ফাইলগুলির একটি সংগ্রহ এবং সিস্টেম ফন্ট অ্যাক্সেস করার সময় অ্যাপ্লিকেশনগুলি এটিকে উল্লেখ করে৷ এজন্য এটি একটি রিসোর্স ফাইল হিসাবে কাজ করে। এটি মাইক্রোসফ্ট উইন্ডোজ ফন্ট ভিউ অ্যাপ্লিকেশন ব্যবহার করে উইন্ডোজ ওএসে খোলা যেতে পারে।

## FON ফাইল ফরম্যাট

একটি FON ফাইলে ফন্ট রিসোর্স থাকে এবং রিসোর্স (.res) ফাইল ফরম্যাট থাকে। .res ফাইল ফরম্যাট ফাইল হেডারের পাশাপাশি ডেটা বিভাগের স্পেসিফিকেশন নির্দিষ্ট করে। একটি .fnt হল একটি রিসোর্স ডেটা ফাইল যা একটি রিসোর্স ফাইলের সাথে অন্তর্ভুক্ত করা হয়। FON ফাইলের বাইনারি ফাইল ফরম্যাট থাকে এবং অ্যাপ্লিকেশন/অক্টেট-স্ট্রীম MIME প্রকার থাকে।

ফন্ট সম্পদ, অন্যান্য ধরনের সম্পদ থেকে ভিন্ন, একটি অ্যাপ্লিকেশনের সম্পদ যোগ করা হয় না. পরিবর্তে এগুলিকে EXE ফাইলে যুক্ত করা হয় এবং .fon ফাইলে নামকরণ করা হয়, ফলে অ্যাপ্লিকেশনের পরিবর্তে লাইব্রেরি ফাইল হয়। একাধিক স্বতন্ত্র ফন্ট একটি ফন্ট গ্রুপের উপাদান গঠন করে যেখানে প্রতিটি গ্রুপ একটি রিসোর্স গ্রুপ কাঠামো অনুসরণ করে। ফন্ট রিসোর্স এই রিসোর্স গ্রুপ স্ট্রাকচার ব্যবহার করে। গ্রুপ শিরোনামে গ্রুপ থেকে একটি নির্দিষ্ট ফন্ট অ্যাক্সেস করার জন্য প্রয়োজনীয় সমস্ত তথ্য রয়েছে। একটি ফন্ট উপাদান সম্পদ নিম্নলিখিত বিন্যাস আছে.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
একটি একক .rc রিসোর্স ফাইলে মিশ্র সম্পদ ঘোষণা থাকতে পারে। ফন্ট গোষ্ঠীগুলি রিসোর্স ফাইলের যে কোনও জায়গায় থাকতে পারে এবং সংলগ্ন হওয়ার দরকার নেই। FONTDIR এর ম্যানুয়াল এন্ট্রি যোগ করার জন্য .RES ফাইল তৈরি করা প্রোগ্রামগুলির জন্য এটি আবশ্যক। গ্রুপ হেডারের গঠন নিচে দেওয়া হল।

```
[সাধারণ রিসোর্স হেডার (টাইপ = 7)]

ওয়ার্ড নম্বর অফফন্ট; // .RES ফাইলে মোট সংখ্যা
```     
The remaining data is repeated for every font in the .RES file.

```
শব্দ ফন্ট অর্ডিনাল;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
শব্দ dfType;
ওয়ার্ড dfPoints;
শব্দ dfVertRes;
শব্দ dfHorizRes;
শব্দ dfascent;
ওয়ার্ড dfInternalLeading;
ওয়ার্ড ডিএফএক্সটার্নাললিডিং;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet;
শব্দ dfPixWidth;
শব্দ dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
শব্দ dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
শব্দ dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD df সংরক্ষিত;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

