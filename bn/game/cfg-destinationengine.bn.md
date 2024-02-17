{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg ফাইল",
"cfg সোর্স ইঞ্জিন কনফিগারেশন ফাইল",
"একটি cfg ফাইল কি?",
"কিভাবে cfg ফাইল খুলবেন",
"ফাইল",
"cfg ফাইল এক্সটেনশন",
"এক্সটেনশন"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG ফাইল ফরম্যাট - সোর্স ইঞ্জিন কনফিগারেশন ফাইল",
  "description": "CFG সোর্স ইঞ্জিন কনফিগারেশন ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি CFG ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "CFG Source Engine",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine-bn",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## একটি CFG ফাইল কি?

**ভালভের সোর্স ইঞ্জিন** প্রসঙ্গে CFG ফাইল, যেমন হাফ-লাইফ 2-এর মতো গেমগুলিতে দেখা যায়, কনফিগারেশন ফাইল হিসাবে কাজ করে। এই ফাইলগুলি প্লেইন টেক্সট কমান্ডের তালিকার মাধ্যমে বিভিন্ন ইন-গেম সেটিংস পরিবর্তন করতে ব্যবহৃত হয়। এই কমান্ডগুলি সাধারণত প্রতি লাইনে একটি দিয়ে সাজানো হয় এবং গেমের দিকগুলি কাস্টমাইজ করার জন্য দায়ী।

প্লেয়ার এবং সার্ভার প্রশাসকদের কাছে `.cfg` ফাইলে উল্লেখিত পরিবর্তনগুলি প্রয়োগ করার জন্য কয়েকটি বিকল্প রয়েছে:

1.  **ম্যানুয়াল এক্সিকিউশন**: ব্যবহারকারীরা ম্যানুয়ালি CFG ফাইলের মধ্যে কমান্ড চালাতে পারে। এর মানে হল যে তারা গেমের ডেভেলপার কনসোলে একে একে প্রতিটি কমান্ড প্রবেশ করে। এই পদ্ধতিটি কোন সেটিংস এবং কখন পরিবর্তন করা হবে তার উপর সুনির্দিষ্ট নিয়ন্ত্রণের অনুমতি দেয়।
    
2.  **অটোমেটিক এক্সিকিউশন**: বিকল্পভাবে, প্লেয়াররা স্বয়ংক্রিয় এক্সিকিউশন বেছে নিতে পারে। এটি উপযুক্ত গেম ডিরেক্টরিতে `.cfg` ফাইল স্থাপন করে। কিছু কিছু `.cfg` ফাইল, যেমন `autoexec.cfg`, খেলা শুরু হলে স্বয়ংক্রিয়ভাবে কার্যকর হয়। এটি নিশ্চিত করে যে প্রতিটি গেম লঞ্চ করার সময় ম্যানুয়াল ইনপুট প্রয়োজন ছাড়াই নির্দিষ্ট সেটিংস প্রয়োগ করা হয়।

## ভালভ সোর্স ইঞ্জিন

The Valve Source Engine, often simply referred to as **Source Engine**, is highly versatile and widely used game engine developed by Valve Corporation. It has been foundation for many popular video games and has powered numerous successful titles. Here are some key points about Valve Source Engine:

1.  **History**: The Source Engine was first introduced with release of Valve's game "Counter-Strike 1.6" in 2004. Since then it has undergone several updates and revisions, with most recent version known as Source 2.0.
    
2.  **উল্লেখযোগ্য গেম**: সোর্স ইঞ্জিন বিভিন্ন সমালোচকদের দ্বারা প্রশংসিত গেমগুলিতে ব্যবহার করা হয়েছে, যার মধ্যে রয়েছে কিন্তু সীমাবদ্ধ নয়:
    
- হাফ-লাইফ 2 এবং এর পর্বগুলি
- পোর্টাল এবং পোর্টাল 2
- টিম দুর্গ 2
- বাম 4 মৃত এবং বাম 4 মৃত 2
- কাউন্টার-স্ট্রাইক: সোর্স এবং কাউন্টার-স্ট্রাইক: গ্লোবাল অফেন্সিভ
- ডোটা 2
3.  **বৈশিষ্ট্য**:
    
- **নমনীয়তা**: সোর্স ইঞ্জিন তার নমনীয়তার জন্য পরিচিত যা ডেভেলপারদের ফার্স্ট-পারসন শুটার থেকে শুরু করে পাজল গেম এবং আরও অনেক কিছু তৈরি করতে দেয়।
- **পদার্থবিদ্যা**: এতে রয়েছে শক্তিশালী পদার্থবিদ্যা ইঞ্জিন যা বাস্তবসম্মত বস্তুর মিথস্ক্রিয়া এবং পরিবেশগত প্রভাব সক্ষম করে।
- **মডিং সাপোর্ট**: ইঞ্জিনে শক্তিশালী মডিং সাপোর্ট রয়েছে যা ব্যবহারকারীর দ্বারা তৈরি অসংখ্য বিষয়বস্তু এবং গেম মোড তৈরি করেছে।
- **মাল্টিপ্লেয়ার ক্ষমতা**: সোর্স ইঞ্জিন একক-প্লেয়ার এবং মাল্টিপ্লেয়ার উভয় গেম বিকাশ করতে ব্যবহার করা হয়েছে এবং এটি অনলাইন গেমপ্লের জন্য ব্যাপক নেটওয়ার্কিং ক্ষমতা প্রদান করে।
    
4.  **Graphics**: Over years Source Engine has received graphical updates to keep up with evolving hardware capabilities. It supports advanced rendering techniques like HDR (High Dynamic Range) lighting and dynamic shadows.

## কিভাবে CFG ফাইল খুলবেন?

আপনার কাছে মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও কোড বা আপনার পছন্দের অন্য কোনও পাঠ্য সম্পাদকের মতো পাঠ্য সম্পাদক ব্যবহার করে `.cfg` ফাইলটি খুলতে এবং সংশোধন করার বিকল্প রয়েছে। এই পাঠ্য সম্পাদকগুলি `.cfg` ফাইলের মধ্যে প্লেইন টেক্সট কমান্ডগুলি দেখার এবং সম্পাদনা করার জন্য ব্যবহারকারী-বান্ধব ইন্টারফেস সরবরাহ করে যা আপনাকে প্রয়োজন অনুসারে সেটিংস কাস্টমাইজ করতে দেয়।

CFG ফাইল খোলা বা রেফারেন্স যে প্রোগ্রাম অন্তর্ভুক্ত

- মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও কোড
- নোটপ্যাড
- টেক্সটএডিট
- যেকোনো টেক্সট এডিটর

## অন্যান্য CFG ফাইল

এখানে অন্যান্য ফাইলের ধরন রয়েছে যা **.cfg** ফাইল এক্সটেনশন ব্যবহার করে।

**সেটিংস**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**খেলা**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**সিস্টেম ও বিবিধ**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## তথ্যসূত্র
* [উৎস (গেম ইঞ্জিন)](https://en.wikipedia.org/wiki/Source_(game_engine))


