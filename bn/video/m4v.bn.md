{
  "date": "2019-10-11",
  "keywords": [
    "M4V",
    "file",
    "extension",
    "format",
    "MPEG-4",
    "Digital Rights Management",
    "DRM",
    "Apple",
    "video"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "M4V ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি M4V ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4v-bn"
    }
  },
  "lastmod": "2019-09-14"
}

## একটি M4V ফাইল কি?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V ভিডিওর জন্য H.264 এবং **[AAC](/audio/aac/)** এবং অডিও এনকোডিং এবং ডিকোডিংয়ের জন্য ডলবি ডিজিটাল ব্যবহার করে।

## M4V ফাইল স্ট্রাকচার ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V সাব-টাইপ দ্বারা সংজ্ঞায়িত যা অবশ্যই M4V_ হতে হবে। আরও খণ্ডের ধরন হল পূর্বনির্ধারিত স্বাক্ষর: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , লোড, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt, ssrc,  পিআইসিটি। অজানা টাইপ শনাক্ত না হওয়া পর্যন্ত অংশগুলি পুনরাবৃত্তি করে, আমরা M4V ফাইল রচনা করি।

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. অফসেট 32 এ (হেক্স: 20) দ্বিতীয় খণ্ডটি অবস্থিত, যার আকার 30,322 (হেক্স: 00 00 76 72, বিগ-এন্ডিয়ান, লোয়ার-বাইট প্রথম) এবং টাইপ করুন **moov** (হেক্স: 6D 6F 6F) 76)। পরবর্তী খণ্ডটি অফসেট 32+30,322#30,354 (হেক্স: 00 00 76 92) এ অবস্থিত এবং এর আকার 8 (হেক্স: 00 00 00 08) এবং টাইপ করুন **মুক্ত** (হেক্স: 66 72 65 65)।
### M4V তে ব্যবহৃত কোডেক ###

#### ভিডিও কোডেক H.264 ####

H.264 হল একটি ভিডিও কম্প্রেশন স্ট্যান্ডার্ড ডিজিটাল ভিডিওকে এমন একটি ফরম্যাটে রূপান্তর করে যাতে ট্রান্সমিশন বা স্টোরেজ প্রয়োজন হলে কম জায়গা লাগে। M4V ভিডিও কম্প্রেশনের জন্য H.264 ব্যবহার করে। এর অ্যাপ্লিকেশন ডিভিডি, টিভি, ভিডিও কনফারেন্সিং এবং ইন্টারনেটে ভিডিও স্ট্রিমিং থেকে বিস্তৃত। H.264 দুটি প্রধান অংশ নিয়ে গঠিত: এনকোডার - যা ভিডিওকে সংকুচিত করে, ডিকোডার - যা কম্প্রেস করা ভিডিওটিকে আনকম্প্রেস করে। নীচের চিত্রে, এনকোডিং এবং ডিকোডিং প্রক্রিয়াগুলি হাইলাইট করা হয়েছে, এবং অন্যান্য প্রক্রিয়াগুলি H.264 স্ট্যান্ডার্ডে আচ্ছাদিত করা হয়েছে।

##### H.264 এ ভিডিও কোডিং এবং ডিকোডিং প্রক্রিয়া #####

সংকুচিত H.264 বিটস্ট্রিমের জন্য, ভিডিও এনকোডার পূর্বাভাস, রূপান্তর এবং এনকোডিং প্রক্রিয়া পরিচালনা করে। একই সময়ে, ডিকোডারটি ভিডিও ফাইলটি তৈরি করতে ডিকোডিং, বিপরীত রূপান্তর এবং পুনর্গঠনের বিপরীত প্রক্রিয়াটি বহন করে। H.264 MPEG এর অর্ধেক আকার নেয়।

#### অডিও কোডেক ####

অ্যাডভান্সড অডিও কোডিং (AAC) ক্ষতিকারক ডিজিটাল অডিও কম্প্রেশনের জন্য একটি অডিও কোডেক এবং এটি একটি M4V পাত্রে ব্যবহৃত হয়। AAC হল [MP3](/audio/mp3/) ফরম্যাটের উত্তরসূরি এবং একই বিটরেট সহ MP3 এর থেকে ভাল মানের অর্জন করে৷ AAC বিন্যাস কম্প্রেশন প্রক্রিয়ার সময় কিছু তথ্য ফেলে দেয়, যা কম গুরুত্ব দেয়। AAC হল একটি পরিবর্তনশীল বিটরেট (VBR) ব্লক-ভিত্তিক কোডেক যেখানে প্রতিটি ব্লক 1024 টাইম-ডোমেন নমুনায় ডিকোড করে।

### তথ্যসূত্র ###

* [উইকিপিডিয়া - M4V](https://en.wikipedia.org/wiki/M4V)

* [উইকিপিডিয়া - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


