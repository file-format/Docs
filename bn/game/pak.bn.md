{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":".pak ফাইল এবং API সম্পর্কে জানুন যেগুলি PAK ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "title" : "PAK ফাইল ফরম্যাট- ভিডিও গেম প্যাকেজ ফাইল",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-bn",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## একটি PAK ফাইল কি?

একটি PAK ফাইল হল একটি প্যাকেজ ফাইল যা বিভিন্ন ভিডিও গেম দ্বারা গেমের ডেটা আর্কাইভ করার জন্য তৈরি করা হয়। মূলত, এটি একটি গেম ফাইল ফরম্যাট। এতে অন্যান্য গেম ডেটা সহ গ্রাফিক্স, টেক্সচার, শব্দ, বস্তুর মতো একাধিক গেম উপাদান অন্তর্ভুক্ত থাকতে পারে। সংরক্ষণাগারটি বেশিরভাগই .zip ফাইল হিসাবে সংরক্ষণ করা হয় এবং WinZip এবং WinRAR এর মতো জনপ্রিয় ডিকম্প্রেশন সফ্টওয়্যার দিয়ে বের করা যায়। PAK ফাইলগুলি ব্যবহার করে ভিডিও গেমগুলির উদাহরণগুলির মধ্যে রয়েছে Quake, Hexen, Crysis এবং হাফ-লাইফ।

## PAK ফাইল ফরম্যাট - আরও তথ্য

বেশিরভাগ ক্ষেত্রে, PAK ফাইলগুলি [ZIP file format](/compression/zip/) এ সংরক্ষিত হয়৷ কিন্তু বিভিন্ন অ্যাপ্লিকেশন এই ফাইলগুলি সংরক্ষণ করার জন্য বিভিন্ন ফাইল বিন্যাস ব্যবহার করতে পারে।


## কিভাবে PAK ফাইল খুলবেন?

আপনি [PakExplorer](https://www.quaketerminus.com/tools.shtml) এবং [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) এর মতো অ্যাপ্লিকেশন দিয়ে PAK ফাইল খুলতে পারেন।

**------------------------------------------------ -------------------------------------------------- ----------------------------------------

## PAK ফাইল ফরম্যাট - সিমুট্রান্স অবজেক্ট ফাইল

.pak এক্সটেনশন সহ একটি ফাইল হল একটি [Simutrans](https://www.simutrans.com/en/) পরিবহন সিমুলেশন গেম ফাইল ফর্ম্যাট৷ এতে ব্যবহারকারীর তৈরি গ্রাফিক্স এবং ডেটা বিষয়বস্তুর মতো সিমুলেশনে ব্যবহৃত বস্তু রয়েছে। এতে গেমের যানবাহন, ভবন, ভূখণ্ড ইত্যাদির মতো বিভিন্ন বস্তু থাকতে পারে। মেকঅবজেক্ট ব্যবহার করে PAK ফাইল তৈরি করা হয়, এই সিমুলেশন অবজেক্ট তৈরির জন্য .dat ফাইল এবং .png ছবি কম্পাইল করে। সিমুট্রান্স খেলোয়াড়দের স্থলপথে যাত্রী, মেইল এবং পণ্যের পরিবহন ব্যবস্থা নির্মাণ ও পরিচালনার মাধ্যমে একটি সফল পরিবহন ব্যবস্থা চালাতে দেয়

## কিভাবে PAK ফাইল তৈরি করবেন?

সিমুট্রান্স উইন্ডোজ এবং লিনাক্স ওএসে PAK ফাইল তৈরির জন্য নমুনা উদাহরণ তালিকাভুক্ত করেছে।

### উইন্ডোজ ওএস

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### লিনাক্স বিই/ওএস

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## তথ্যসূত্র

 * [সিমুট্রান্স](https://en.wikipedia.org/wiki/Simutrans)

