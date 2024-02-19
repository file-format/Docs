{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "FZPZ ফাইল ফরম্যাট - ফ্রিটজিং পার্ট ফাইল",
  "description": "একটি FZPZ ফাইল এবং API যা FZPZ ফাইলগুলি তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzpz-bn"
    }
  },
  "lastmod": "2022-06-20"
}

## একটি FZPZ ফাইল কি?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ ফাইল ফরম্যাট - আরও তথ্য

FZPZ ফাইলগুলি সংকুচিত [ZIP](/compression/zip/) সংরক্ষণাগার হিসাবে ডিস্কে সংরক্ষিত হয়৷ আপনি .fzpz থেকে .zip এক্সটেনশনের নাম পরিবর্তন করতে পারেন এবং সংরক্ষণাগার থেকে ফাইলগুলি বের করতে WinZIP-এর মতো যেকোনো স্ট্যান্ডার্ড ডিকম্প্রেশন ইউটিলিটি ব্যবহার করতে পারেন।

### FZPZ ফাইলের কাঠামোর তথ্য

উল্লিখিত হিসাবে, একটি FZPZ ফাইল হল একটি সংরক্ষণাগার ফাইল যাতে মুদ্রিত সার্কিট বোর্ডে ব্যবহৃত অংশের প্রতিনিধিত্বের জন্য একাধিক ফাইল থাকে। FZPZ নিম্নলিখিত ফাইল ধারণ করে:

 * `চারটি SVG ফাইল` - যা অংশের ব্রেডবোর্ড, পরিকল্পিত, PCB এবং আইকন চিত্রগুলিকে উপস্থাপন করে
 * `FZP ফাইল` - একটি XML ফাইল যাতে অংশের বৈশিষ্ট্য, সংযোগকারী এবং বাস সম্পর্কে তথ্য থাকে

ফাইল সাধারণত অনুসরণ হিসাবে নামকরণ করা হয়.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## তথ্যসূত্র ##

* [fzpz এক্সটেনশন সহ নতুন অংশ](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


