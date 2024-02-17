{
  "date": "2023-06-21",
  "keywords": [
"সাব ফাইল",
"একটি সাব ফাইল কি",
"মাইক্রোডিভিডি সাবটাইটেল ফাইলের উদাহরণ",
"সাবটাইটেল এক্সটেনশন",
"সাব খুলুন",
"সাবটাইটেল ফাইলের ধরন",
"কিভাবে SUB ফাইল খুলবেন",
"ফাইল",
"SUB ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "সাব ফাইল ফরম্যাট - মাইক্রোডিভিডি সাবটাইটেল ফাইল",
  "description": "SUB ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি SUB ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub-bn",
      "parent": "video"
}
},
  "lastmod": "2023-06-21"
}

## একটি SUB ফাইল কি?

একটি SUB ফাইল হল একটি মাইক্রোডিভিডি সাবটাইটেল ফাইল ফর্ম্যাট যা ভিডিওতে সাবটাইটেল প্রদর্শন করতে ব্যবহৃত হয়, সাধারণত .sub ফাইল এক্সটেনশন থাকে। এই ফাইলগুলিতে প্রতিটি সাবটাইটেল এন্ট্রির জন্য সময় সংক্রান্ত তথ্য এবং পাঠ্য রয়েছে।

মাইক্রোডিভিডি সাবটাইটেল ফাইলগুলি সাধারণ পাঠ্য-ভিত্তিক বিন্যাস ব্যবহার করে যেখানে প্রতিটি সাবটাইটেল এন্ট্রিতে কয়েকটি লাইন থাকে। প্রথম লাইনে শুরু এবং শেষ টাইমস্ট্যাম্প সহ সাবটাইটেলের সময় সংক্রান্ত তথ্য রয়েছে। পরবর্তী লাইনে প্রকৃত সাবটাইটেল পাঠ্য রয়েছে।

Here is an example of MicroDVD subtitle file:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## সাবটাইটেল এক্সটেনশন

Subtitles can have various file extensions depending on format they are in. Some common subtitle file extensions include:

- **.srt:** SubRip subtitle format. It is one of most widely used subtitle formats and is supported by many media players and video editing software.
- **.sub:** Subtitle file format that can be used by different subtitle formats, such as MicroDVD, SubViewer and SubStation Alpha.
- **.ass or .ssa:** Advanced SubStation Alpha or SubStation Alpha subtitle format. It supports advanced features like text formatting, positioning and effects.
- **.vtt:** WebVTT (Web Video Text Tracks) format used for displaying subtitles on web videos. It is commonly used with HTML5 video players.
- **.idx/.sub:** Format used by DVD subtitles. The .idx file contains timing and formatting information, while .sub file contains the actual subtitle text.
- **.smi or .sami:** Synchronized Accessible Media Interchange format. It is commonly used for closed captions and subtitles in Windows Media Player.

## ওপেন সাব বলতে কী বোঝায়?

ওপেন সাব মানে সাধারণত OpenSubtitles যা একটি জনপ্রিয় অনলাইন প্ল্যাটফর্ম যা একাধিক ভাষায় সিনেমা এবং টিভি শোগুলির জন্য সাবটাইটেল প্রদান করে। এটি ব্যবহারকারীদের সম্প্রদায়ের দ্বারা অবদান রাখা সাবটাইটেল ফাইলের বিশাল সংগ্রহ অফার করে। আপনি আপনার পছন্দসই সিনেমা বা টিভি সিরিজের জন্য সাবটাইটেল অনুসন্ধান এবং ডাউনলোড করতে OpenSubtitles ওয়েবসাইট (www.opensubtitles.org) দেখতে পারেন।

## সাবটাইটেল ফাইলের ধরন

Subtitle files come in various formats, each with its own file type or extension. Here are some common subtitle file types:

- **SubRip Subtitle Format (.srt):** This is one of most widely used subtitle formats. SRT files are plain text files that contain subtitle entries with timestamps and corresponding text.
- **SubViewer Subtitle Format (.sub):** SubViewer files are similar to SRT files, contain subtitle entries with timestamps and text, may support additional features such as text formatting and colors.
- **SubStation Alpha (.ssa) and Advanced SubStation Alpha (.ass):** These formats support advanced features like text formatting, styling, positioning and animation effects. SSA and ASS files are commonly used for anime subtitles.
- **MicroDVD Subtitle Format (.sub):** MicroDVD format uses .sub files and includes timing information and text for each subtitle entry. It is often used with media players and video editing software.
- **DVD Subtitles (.sub and .idx):** DVD subtitles typically consist of two files: the .sub file, which contains subtitle text, and .idx file, which contains timing and formatting information.
- **WebVTT (.vtt):** WebVTT is a subtitle format used for web videos, commonly used with HTML5 video players and supports basic formatting options.
- **MPL2 Subtitle Format (.mpl):** MPL2 files are used with MPlayer, a media player for Unix-like systems, contain subtitle entries with timestamps and text.
- **iTunes Timed Text (.itt):** iTunes Timed Text files are used for subtitles in Apple's iTunes and other Apple platforms. They support features like text styling and positioning.
- **Teletext Subtitle Format (.srt or .txt):** Teletext subtitles are commonly used in broadcast television. They are usually saved as plain text files with .srt or .txt extensions.

## কিভাবে SUB ফাইল খুলবেন?

নিম্নলিখিত মিডিয়া প্লেয়ারগুলি সাবটাইটেল ট্র্যাক হিসাবে SUB ফাইল খুলতে পারে।

- VideoLAN VLC মিডিয়া প্লেয়ার
- এমপি প্লেয়ার

ভিএলসি প্লেয়ারে SUB ফাইল খুলতে এই পদক্ষেপগুলি অনুসরণ করুন

- ভিএলসি প্লেয়ার খুলুন এবং আপনার ভিডিও চালান
- VLC মিডিয়া প্লেয়ার মেনু বার থেকে, **সাবটাইটেল > সাবটাইটেল ফাইল যোগ করুন ....** নির্বাচন করুন।
- SUB ফাইলে নেভিগেট করুন এবং এটি খুলুন

আপনার যদি SUB ফাইল সম্পাদনা করার প্রয়োজন হয়, আপনি এটি যেকোনো টেক্সট এডিটর যেমন Microsoft Notepad (Windows) বা Apple TextEdit (Mac) দিয়ে খুলতে পারেন।

## তথ্যসূত্র
* [মাইক্রোডিভিডি](https://en.wikipedia.org/wiki/MicroDVD)


