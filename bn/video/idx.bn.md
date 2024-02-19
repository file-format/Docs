{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "IDX - উচ্চ দক্ষতা ভিডিও কোডেক",
  "description": "IDX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি IDX ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-idx-bn"
    }
  },
  "lastmod": "2022-07-12"
}

## একটি IDX ফাইল কি?

একটি IDX ফাইল হল একটি সাবটাইটেল ইনডেক্স ফাইল যা একটি .sub (VobSub সাবটাইটেল) ফাইলের ভিতরে সাবটাইটেলের জন্য মেটাডেটা তথ্যের তালিকা নির্দেশ করে। এটি VobSub সফ্টওয়্যার অ্যাপ্লিকেশন দ্বারা তৈরি এবং ব্যবহার করা হয়েছে যা ব্যবহারকারীদের ডিভিডি থেকে সাবটাইটেল বের করতে এবং একটি SUB ফাইলে ডাম্প করতে দেয়। IDX ফাইলগুলিতে টাইমস্ট্যাম্প এবং বাইট অফসেট রয়েছে যা প্রতিটি একক সাবটাইটেল নির্দেশ করতে ব্যবহৃত হয়। VobSub সর্বদা সংশ্লিষ্ট SUB ফাইলের সাথে একটি IDX ফাইল তৈরি করে।

## IDX ফাইল ফরম্যাট - আরও তথ্য

IDX ফাইলগুলি তৈরি করা হয় এবং প্লেইন টেক্সট ফাইল হিসেবে সেভ করা হয় যা যেকোনো টেক্সট এডিটরে খোলা যায়। একটি IDX ফাইলে এমন তথ্য থাকে যা মিডিয়া প্লেয়াররা পর্দায় প্রদর্শিত সাবটাইটেল টেক্সটের রঙ, স্ক্রিনে সাবটাইটেল টেক্সটের অবস্থানের মতো পরামিতিগুলি পড়ার জন্য পড়ে।

### IDX সাবটাইটেল সেটিংস

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## IDX ফাইল ফরম্যাটের উদাহরণ

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## কিভাবে IDX ফাইল ব্যবহার করবেন?

আপনি যদি একটি মুভির জন্য সাব এবং IDX ফাইলগুলি পেয়ে থাকেন, তাহলে আপনি এই সাবটাইটেলগুলিকে সেই মুভির সাথে প্লে ব্যাক করতে পারেন যার জন্য এগুলি তৈরি করা হয়েছে৷ ভিএলসি, জিওএম প্লেয়ার, পটপ্লেয়ার, বা পাওয়ারডিভিডির মতো অনেক অ্যাপ্লিকেশনের এই SUB এবং IDX ফাইলগুলি লোড করার ক্ষমতা রয়েছে এবং এগুলিকে মুভির সাথে প্লে করা যায়। সফ্টওয়্যার অ্যাপ্লিকেশনগুলি SUB এবং IDX সাবটাইটেল ফাইলগুলিকে [.mkv](/video/mkv/) ফাইলগুলিতে এম্বেড করতে পারে৷

## IDX কে SRT তে রূপান্তর করুন

[SRT](/video/srt/) (সাবরিপ ফাইল ফরম্যাট) হল সাবরিপ ফাইল ফরম্যাটে সংরক্ষিত একটি সাধারণ সাবটাইটেল ফাইল। VobSub ফাইল ফরম্যাটের তুলনায় এটি বেশি ব্যবহৃত হয়। এইভাবে, আপনি যদি SUB/IDX ফাইলগুলিকে SRT ফাইল ফরম্যাটে রূপান্তর করতে চান, সেখানে 3য় পক্ষের টুল উপলব্ধ রয়েছে যা এটি অর্জন করতে ব্যবহার করা যেতে পারে। SUB/IDX থেকে SRT রূপান্তরকারী, SubtitleTools.com-এ উপলব্ধ এমন একটি টুল যা SUB এবং IDX ফাইলগুলিকে ইনপুট হিসাবে নেয় এবং এই VobSub সাবটাইটেলগুলিকে SRT ফাইলগুলিতে রূপান্তর করে৷

## তথ্যসূত্র

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

