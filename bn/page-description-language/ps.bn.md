{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "পিএস ফাইল ফরম্যাট",
  "description": "পিএস ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা পিএস ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ps-bn"
    }
  },
  "lastmod": "2019-09-10"
}

## একটি .PS ফাইল কি? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## সংক্ষিপ্ত ইতিহাস ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. অ্যাপলের স্টিভ জবস তাদের পরিদর্শন করেন এবং লেজার প্রিন্টার চালানোর জন্য পোস্টস্ক্রিপ্ট মানিয়ে নেওয়ার পরামর্শ দেন।

মার্চ 1985 সালে, একটি এমবেডেড পোস্টস্ক্রিপ্ট ইন্টারপ্রেটার সহ প্রথম প্রিন্টারটি ছিল অ্যাপলের লেজার রাইটার, যা ডেস্কটপ প্রকাশনায় (ডিটিপি) বিপ্লব ঘটায়। প্রযুক্তিগত সুস্থতা এবং ব্যাপক প্রাপ্যতা পোস্টস্ক্রিপ্ট, ডেস্কটপ এবং ইলেকট্রনিক প্রকাশনার জন্য একটি পছন্দের ভাষা তৈরি করেছে। 1990 সালে, পোস্টস্ক্রিপ্ট ভাষার জন্য একজন দোভাষী লেজার প্রিন্টারের একটি অপরিহার্য অংশ ছিল।

## প্রধান বৈশিষ্ট্য ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**আকৃতি:** প্রকৃতির স্বেচ্ছাচারী, সরলরেখা, বক্ররেখা, বর্গক্ষেত্র এবং ঘনবক্ররেখার সমন্বয়ে গঠিত হতে পারে যা স্ব-প্রান্তরিত এবং সংযোগ বিচ্ছিন্ন (বিভাগ এবং গর্তে) উভয়ই হতে পারে।

**পেইন্টিং অপারেটর:** যেকোনো বেধ, রঙের আকৃতির রূপরেখাকে অনুমতি দেয়, অন্য কোনো গ্রাফিকের ক্রপিং করার জন্য আকৃতিটিকে ক্লিপিং হিসেবে আঁকার অনুমতি দেয়।

**রঙ:** গ্রেস্কেল, RGB, CMYK, এবং CIE এর মত বৈচিত্র্য রয়েছে। বিশেষ ধরনের রং বিভিন্ন বৈশিষ্ট্য হিসাবে মডেল করা হয়: স্পট রং, রঙ ম্যাপিং, এমনকি ছায়া এবং পুনরাবৃত্তি প্যাটার্ন.

**টেক্সট:** সম্পূর্ণরূপে গ্রাফিক্সের সাথে একত্রিত। অধিকন্তু, অ্যাডোব ইমেজিং মডেল পাঠ্য অক্ষরগুলিকে গ্রাফিকাল আকার হিসাবে প্রদর্শন করার অনুমতি দেয় যা যে কোনও সাধারণ গ্রাফিক্স অপারেটর দ্বারা পরিচালিত হতে পারে।

**নমুনা ছবি**: মূল উৎস থেকে নেওয়া (স্ক্যান করা ফটোগ্রাফ) অথবা কৃত্রিমভাবে তৈরি করা হতে পারে। পোস্টস্ক্রিপ্ট ভাষা যেকোন রেজোলিউশনে এবং একটি আউটপুট ডিভাইসে বিভিন্ন রঙের মডেল অনুসারে চিত্রগুলি পুনরুত্পাদনের জন্য বিভিন্ন উপায় সরবরাহ করে।

একটি সাধারণ-উদ্দেশ্য প্রোগ্রামিং ভাষা তার কাঠামোর মধ্যে Ps এম্বেড করে গ্রাফিক্স ক্ষমতা পোস্টস্ক্রিপ্ট ভাষার সুবিধা নিতে পারে। আদিম ডেটাটাইপ, যেমন সংখ্যা, অক্ষর, অ্যারে এবং স্ট্রিং; নিয়ন্ত্রণ আদিম, যেমন, loops, পদ্ধতি এবং শর্তাবলী; এবং কিছু অপ্রচলিত বৈশিষ্ট্য, যেমন অভিধানগুলি ভাষায় নির্দিষ্ট করা হয়েছে। এই বৈশিষ্ট্যগুলি প্রোগ্রামারদের উচ্চ স্তরের ক্রিয়াকলাপগুলি চালানোর জন্য কমান্ড লিখতে সহায়তা করে। এই উচ্চ স্তরের ক্রিয়াকলাপগুলি জটিল প্রয়োগের চাহিদা পূরণ করে। এই ধরনের অনুশীলন মৌলিক ক্রিয়াকলাপগুলির একটি নির্দিষ্ট সেট ব্যবহার করার পরিবর্তে আরও কমপ্যাক্ট এবং দক্ষ।

পোস্টস্ক্রিপ্টে লেখা প্রোগ্রামগুলি ASCII উৎস পাঠের আকারে উত্পাদিত, যোগাযোগ এবং ব্যাখ্যা করা যেতে পারে। পুরো ভাষাটিকে মুদ্রণযোগ্য অক্ষর এবং সাদা স্থানের আকারে সংজ্ঞায়িত করা যেতে পারে। এই উপস্থাপনা প্রোগ্রামারদের ভাষা তৈরি করতে, ম্যানিপুলেট করতে এবং সহজেই বুঝতে সহায়তা করে। তাছাড়া, বিভিন্ন কম্পিউটার এবং অপারেটিং সিস্টেমের মধ্যে ফাইল স্টোরেজ এবং ট্রান্সমিশন মেশিনের স্বাধীনতার মাধ্যমে সুবিধাজনক রাখা হয়েছে।

ভাষাটির বাইনারি এনকোডেড ফর্মগুলি সম্ভব, যখন প্রোগ্রামটি পোস্টস্ক্রিপ্ট দোভাষীর কাছে একটি সম্পূর্ণ স্বচ্ছ যোগাযোগের পথ নিশ্চিত করা হয়। PS প্রোগ্রামগুলির ASCII প্রতিনিধিত্বের জন্য কঠোর সমন্বয়ের পরামর্শ Adobe থেকে ডকুমেন্ট এক্সচেঞ্জ বা আর্কাইভাল স্টোরেজের জন্য দেওয়া হয়।

## সংস্করণ ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. প্রতিটি সংস্করণ গুরুত্বপূর্ণ কাঠামোগত মন্তব্য সংজ্ঞায়িত করে। এনক্যাপসুলেটেড পোস্টস্ক্রিপ্ট ফাইল (ইপিএস) হল পোস্টস্ক্রিপ্ট ফাইলের একটি বিশেষ উপ-প্রকার যা একটি আয়তক্ষেত্রাকার গ্রাফিক নির্দিষ্ট করতে ভাষা ব্যবহার করে। পোস্টস্ক্রিপ্ট ল্যাঙ্গুয়েজ রেফারেন্স ম্যানুয়াল একটি ইপিএসকে এভাবে বর্ণনা করে, একটি এনক্যাপসুলেটেড পোস্টস্ক্রিপ্ট (ইপিএস) ফাইল হল একটি পোস্টস্ক্রিপ্ট প্রোগ্রাম যা একটি ফর্মে সর্বাধিক একক পৃষ্ঠার বর্ণনা করে যা অন্যান্য অ্যাপ্লিকেশন দ্বারা আমদানি করা নথির মধ্যে এম্বেড করতে পারে। একটি পোস্টস্ক্রিপ্ট নথি ফাইল এটিতে একটি ইপিএস ফাইল এনক্যাপসুলেট করতে পারে। পোস্টস্ক্রিপ্টের একটি অতিরিক্ত ব্যবহার প্রদর্শন পোস্টস্ক্রিপ্ট (DPS) হিসাবে উল্লেখ করা হয়েছে। ডিপিএস একটি গ্রাফিক্স ইঞ্জিনের মাধ্যমে অন-স্ক্রিন গ্রাফিক্স তৈরি করে যা পোস্টস্ক্রিপ্ট ইমেজিং মডেল এবং ভাষা ব্যবহার করে।

## তথ্যসূত্র ##

* [পোস্টস্ক্রিপ্ট ফরম্যাট পরিবার](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


