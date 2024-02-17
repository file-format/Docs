{
  "date" : "2020-08-20",
  "keywords" : [ "eot file", "eot file format", "what is a eot file", "file", "eot example", "eot file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EOT - TrueType ফন্ট ফাইল ফরম্যাট",
  "description":"EOT ফাইল তৈরি এবং খোলার জন্য EOT ফাইল ফরম্যাট এবং API সম্পর্কে জানুন।",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## একটি EOT ফাইল কি?

.eot এক্সটেনশন সহ একটি ফাইল হল একটি OpenType ফন্ট যা একটি নথিতে এম্বেড করা হয়। এগুলি বেশিরভাগ ওয়েব ফাইলে ব্যবহৃত হয় যেমন একটি ওয়েব পৃষ্ঠা। এটি Microsoft দ্বারা তৈরি করা হয়েছে এবং PowerPoint উপস্থাপনা [.pps](/presentation/pps/) ফাইল সহ Microsoft পণ্য দ্বারা সমর্থিত। ফাইলটি প্রাথমিক ব্যবহারের জন্য নয় এবং এটি প্রধান নথি বা ওয়েব পৃষ্ঠার সাথে সহগামী নথির মতো৷ OTF ফন্টের মতো, EOT পোস্টস্ক্রিপ্ট এবং ট্রু টাইপ উভয় গ্লিফের রূপরেখা সমর্থন করে। EOT ফাইলগুলি LZ কম্প্রেশন ব্যবহার করে সংকুচিত হওয়ার কারণে আকারে ছোট। বিদ্যমান TTF/OTF ফন্ট থেকে একটি ফন্ট তৈরি করতে EOT একটি Microsoft টুল ব্যবহার করে।

## সংক্ষিপ্ত ইতিহাস

EOT ফন্টটি 2007 সালে CSS3-এর অংশ হিসাবে W3C-তে জমা দেওয়া হয়েছিল কিন্তু রিমোট সিস্টেমে স্থায়ীভাবে ইনস্টল করার প্রয়োজনীয়তার কারণে এটি প্রত্যাখ্যানের কারণ হয়ে ওঠে। এটি মার্চ 2008 সালে পুনরায় জমা দেওয়া হয়েছিল, কিন্তু W3C শেষ পর্যন্ত [Web Font Format](/font/woff/) (WOFF) বেছে নিয়েছিল যা তখন প্রমিত ছিল।

## EOT ফাইল ফরম্যাট

EOT ফাইল বিন্যাসের বিশদ বিবরণ [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat)-এ পাওয়া যাবে এবং এই ফন্ট বিন্যাস দ্বারা ব্যবহৃত কাঠামোটি বিশদভাবে বর্ণনা করা হয়েছে। EOT একটি একক EMBEDDEDFONT কাঠামো নিয়ে গঠিত যা hte ফন্টের নাম এবং সমর্থিত অক্ষর সম্পর্কে যথেষ্ট প্রাথমিক তথ্য প্রদান করে। এই তথ্যের প্যাকিং ব্যবহারকারী এজেন্টদের ফন্টটিকে আনপ্যাক করা, ডিকম্প্রেস করা বা ইনস্টল করা এড়াতে দেয় যদি এটি ইতিমধ্যেই মেশিনে উপস্থিত থাকে।

### এমবেডেডফন্ট স্ট্রাকচার
EMBEDDEDFONT স্ট্রাকচারে তিনটি রিভিশন হয়েছে, প্রতিটি রিভিশনের সাথে স্ট্রাকচারের শেষে অতিরিক্ত ডাটা যোগ করা হয়েছে। EMBEDDEDFONT কাঠামোর শেষ সংশোধনটি নীচে চিত্রিত করা হয়েছে।

|ডেটা টাইপ | এন্ট্রি নাম | বর্ণনা |
---|---|---|
|আনসাইন করা লং|EOTSize|বাইটে মোট গঠন দৈর্ঘ্য (স্ট্রিং এবং ফন্ট ডেটা সহ)|
|আনসাইনড লং|ফন্টডেটা সাইজ|বাইটে ওপেনটাইপ ফন্টের (ফন্টডেটা) দৈর্ঘ্য|
|আনসাইন করা লম্বা|সংস্করণ|এই বিন্যাসের সংস্করণ সংখ্যা - 0x00020002|
|আনসাইন করা লম্বা|পতাকা|প্রসেসিং পতাকা|
|byte[10]|FontPANOSE|এই ফন্টের জন্য প্যানোস মান - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|বাইট|চারসেট|উইন্ডোজে এটি TEXTMETRIC.tmCharSet থেকে নেওয়া হয়েছে এই মানটি ফন্টের অক্ষর সেট নির্দিষ্ট করে। DEFAULT_CHARSET (0x01) কোনো পছন্দ নির্দেশ করে না। - দেখুন https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|বাইট
|আনসাইন করা লম্বা
|আনসাইন করা সংক্ষিপ্ত
|আনসাইন করা সংক্ষিপ্ত|MagicNumber|EOT ফাইলের জন্য ম্যাজিক নম্বর - 0x504C৷ ডেটা দুর্নীতি পরীক্ষা করতে ব্যবহৃত হয়
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (বিট 0-31) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (বিট 32-63) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (বিট 64-95) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (বিট 96-127) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|আনসাইন করা লম্বা|CodePageRange1|CodePageRange1 (বিট 0-31) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|আনসাইন করা লম্বা|CodePageRange2|CodePageRange2 (বিট 32-63) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|আনসাইনড লং|চেকসুম অ্যাডজাস্টমেন্ট
|আনসাইন করা দীর্ঘ|সংরক্ষিত1|সংরক্ষিত - অবশ্যই 0| হতে হবে৷
|আনসাইন করা দীর্ঘ|সংরক্ষিত2|সংরক্ষিত - অবশ্যই 0| হতে হবে৷
|আনসাইন করা দীর্ঘ|সংরক্ষিত3|সংরক্ষিত - অবশ্যই 0| হতে হবে৷
|আনসাইন করা দীর্ঘ|সংরক্ষিত4|সংরক্ষিত - অবশ্যই 0| হতে হবে৷
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং1|দীর্ঘ সারিবদ্ধতা বজায় রাখার জন্য প্যাডিং। প্যাডিং মান সর্বদা 0x0000 এ সেট করা আবশ্যক।|
|আনসাইন করা সংক্ষিপ্ত|FamilyNameSize|FamilyName অ্যারে দ্বারা ব্যবহৃত বাইটের সংখ্যা|
|byte|FamilyName[FamilyNameSize]|UTF-16 অক্ষরের অ্যারে FamilyNameSize বাইটের দৈর্ঘ্য। এটি হল ইংরেজি ভাষার ফন্ট ফ্যামিলি স্ট্রিং ফন্টের নামের টেবিলে পাওয়া যায় (নাম আইডি = 1) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং2|প্যাডিং মান সর্বদা 0x0000 এ সেট করতে হবে
|আনসাইন করা সংক্ষিপ্ত|StyleNameSize|StyleName| দ্বারা ব্যবহৃত বাইটের সংখ্যা|
|byte|StyleName[StyleNameSize]|UTF-16 অক্ষরের অ্যারে StyleNameSize বাইটের দৈর্ঘ্য। এটি ইংরেজি ভাষার ফন্ট সাবফ্যামিলি স্ট্রিংটি ফন্টের নামের টেবিলে পাওয়া যায় (নাম আইডি = 2) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং3|প্যাডিং মান সর্বদা 0x0000 এ সেট করতে হবে
|আনসাইন করা সংক্ষিপ্ত|VersionNameSize|VersionName দ্বারা ব্যবহৃত বাইটের সংখ্যা|
|bytes|VersionName[VersionNameSize]|UTF-16 অক্ষরের অ্যারে VersionNameSize বাইটের দৈর্ঘ্য। এটি ইংরেজি ভাষার সংস্করণ স্ট্রিং যা ফন্টের নামের টেবিলে পাওয়া যায় (নাম আইডি = 5) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং4|প্যাডিং মান সর্বদা 0x0000 এ সেট করতে হবে
|আনসাইন করা সংক্ষিপ্ত|FullNameSize|FullName দ্বারা ব্যবহৃত বাইটের সংখ্যা|
|byte|FullName[FullNameSize]|UTF-16 অক্ষরের অ্যারে FullNameSize বাইটের দৈর্ঘ্য। এটি ফন্টের নামের টেবিলে পাওয়া ইংরেজি ভাষার পুরো নামের স্ট্রিং (নাম আইডি = 4) - দেখুন https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং5|প্যাডিং মান সর্বদা 0x0000 এ সেট করা আবশ্যক।|
|আনসাইন করা সংক্ষিপ্ত|RootStringSize|RootString অ্যারে দ্বারা ব্যবহৃত বাইটের সংখ্যা|
|byte|RootString[RootStringSize]|UTF-16 অক্ষরের অ্যারে RootStringSize বাইটের দৈর্ঘ্য।|
|আনসাইন করা লম্বা|RootStringCheckSum|RootString CheckSum মান। নীচে RootStringChecksum প্রক্রিয়া করার জন্য অ্যালগরিদম দেখুন
|আনসাইন করা লম্বা|EUDCCodePage|EUDC ফন্ট সমর্থনের জন্য কোডপৃষ্ঠা মান প্রয়োজন৷|
|আনসাইন করা সংক্ষিপ্ত|প্যাডিং6|প্যাডিং মান সর্বদা 0x0000 এ সেট করতে হবে
| স্বাক্ষরবিহীন সংক্ষিপ্ত| স্বাক্ষরের আকার| স্বাক্ষর অ্যারে দ্বারা ব্যবহৃত বাইটের সংখ্যা৷ বর্তমানে সংরক্ষিত এবং 0x0000 এ সেট করা উচিত।|
|বাইট|স্বাক্ষর[সিগনেচার সাইজ]|বর্তমানে সংরক্ষিত। স্বাক্ষরের আকার 0x0000 হলে এই অ্যারের কোন দৈর্ঘ্য নেই।|
|আনসাইনড লং|EUDCFlags|EUDC ফন্টের জন্য প্রসেসিং পতাকা। সাধারণ মান TTEMBED_XORENCRYPTDATA এবং TTEMBED_TTCOMPRESSED হতে পারে৷|
|আনসাইন করা লম্বা|EUDCFontSize|সিগনেচার অ্যারে দ্বারা ব্যবহৃত বাইটের সংখ্যা৷|
|byte|EUDCFontData[EUDCFontSize]|EUDC ফন্ট ডেটার জন্য ব্যবহৃত বাইটের সংখ্যা। যদি EUDCFontSize 0x00000000 হয় তাহলে এই অ্যারের কোনো দৈর্ঘ্য নেই।|
|byte|FontData[FontDataSize]|এই EOT ফাইলের ফন্ট ডেটা। প্রসেসিং ফ্ল্যাগ দ্বারা নির্দেশিত হিসাবে ডেটা সংকুচিত বা XOR এনক্রিপ্ট করা হতে পারে।|

## তথ্যসূত্র

 * [EOT ফাইল ফরম্যাট](https://www.w3.org/Submission/EOT/)
 * [এম্বেডেড ওপেনটাইপ](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [ফন্ট এমবেডিং](https://en.wikipedia.org/wiki/Font_embedding)

