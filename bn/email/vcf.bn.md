{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VCF - ভার্চুয়াল যোগাযোগ ফাইল",
  "description":"ভিসিএফ ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা ভিসিএফ ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## একটি VCF ফাইল কি?

VCF (ভার্চুয়াল কার্ড ফরম্যাট) বা vCard যোগাযোগের তথ্য সংরক্ষণের জন্য একটি ডিজিটাল ফাইল বিন্যাস। ফরম্যাটটি জনপ্রিয় তথ্য বিনিময় অ্যাপ্লিকেশনগুলির মধ্যে ডেটা আদান-প্রদানের জন্য ব্যাপকভাবে ব্যবহৃত হয়। বেশিরভাগ অপারেটিং সিস্টেম যেমন Windows এবং MacOS এই ফাইলগুলি তৈরি এবং খোলার জন্য ডিফল্ট অ্যাপ্লিকেশনের সাথে আসে। একটি একক VCF ফাইলে এক বা একাধিক পরিচিতির যোগাযোগের তথ্য থাকতে পারে। একটি VCF ফাইলে সাধারণত পরিচিতির নাম, ঠিকানা, ফোন নম্বর, ইমেল, জন্মদিন, ফটোগ্রাফ এবং অডিওর মতো অন্যান্য ক্ষেত্র ছাড়াও তথ্য থাকে। ইমেল ক্লায়েন্ট এবং পরিষেবাগুলির দ্বারা সমর্থিত হচ্ছে, vCard ফর্ম্যাট ব্যবহার করে পরিচিতি স্থানান্তরের সময় ডেটার কোনও ক্ষতি হয় না৷ VCF ফাইল ফরম্যাটের মিডিয়া টাইপ হল text/vcard।

## ভিসিএফ ফাইল ফরম্যাট

ভিসিএফ ফাইলগুলি প্রকৃতির দ্বারা পাঠ্য এবং মানুষের পাঠযোগ্য। এগুলি মাইক্রোসফ্ট উইন্ডোজের নোটপ্যাড এবং MacOS-এ টেক্সটএডিটের মতো পাঠ্য সম্পাদকগুলিতে খোলা যেতে পারে। যদি ফাইলটিতে একটি চিত্র থাকে, তবে, এটি পাঠ্য সম্পাদকে দেখাবে না।

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) VCF ফাইলগুলি খোলার জন্য সমর্থন প্রদান করে এবং সেই সাথে জনপ্রিয় [MSG](/email/msg/) ফর্ম্যাটের মতো অন্যান্য ফরম্যাটে রূপান্তর করে৷ VCF ফাইল ফরম্যাট সংস্করণ 2.1 থেকে 4.0 পর্যন্ত সময়ের সাথে ফাইল ফরম্যাটে বিস্তারিত তথ্য যোগ করে উন্নত করা হয়েছে। ফরম্যাটটি ফোন পরিচিতি রপ্তানি করতে এবং পরে অন্য ডিভাইসে আমদানি করতেও ব্যবহৃত হয়।

{{< figure src="../VCF.png" alt="ভিসিএফ ফাইল ফরম্যাট" >}}

### VCF 2.1 উদাহরণ

নিম্নলিখিত সংস্করণ 2.1 এর একটি উদাহরণ।

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 উদাহরণ

নিম্নলিখিত সংস্করণ 3.0 এর একটি উদাহরণ।

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 উদাহরণ

নিম্নলিখিত সংস্করণ 4.0 এর একটি উদাহরণ।

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## তথ্যসূত্র

* [ভিসিএফ - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/VCard)


