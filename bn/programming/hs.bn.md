{
  "date": "2021-04-21",
  "keywords": [
    "what is a HS file",
    "tutorials on HS",
    "HS means",
    "HS",
    "HS files",
    "extension",
    "format",
    "HS tutorial",
    ".hs",
    "HS example",
    "hs file extension",
    "how to open a hs file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "HS - হাসকেল স্ক্রিপ্ট ফাইল ফরম্যাট",
  "description": "একটি HS ফাইল ফরম্যাট এবং APIগুলি কী তা সম্পর্কে জানুন যা HS ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-hs-bn"
    }
  },
  "lastmod": "2021-06-15"
}

# HS - জাভা হেল্পসেট ফাইল ফরম্যাট

## একটি জাভা এইচএস ফাইল কি?

জাভা প্রোগ্রামিং ভাষায় .hs এক্সটেনশন সহ একটি ফাইল হল একটি হেল্প ডকুমেন্টেশন ফাইল যা JavaHelp সিস্টেম দ্বারা ব্যবহার করা হয় যখন এটি একটি অ্যাপ্লিকেশন দ্বারা সক্রিয় হয়। এটি ইনস্টল করা নির্দিষ্ট অ্যাপ্লিকেশনের জন্য হেল্পসেট সংজ্ঞায়িত করে এবং অ্যাপ্লিকেশনটির জন্য সিস্টেম সহায়তার অংশ হিসাবে একাধিক উপসেট নিয়ে গঠিত। জাভা প্রোগ্রামটি অবশ্যই হেল্পসেট ফাইল খুঁজে পেতে সক্ষম হবে যার নাম .hs এক্সটেনশন দিয়ে শেষ হয়।

## জাভা হেল্পসেট তথ্য

A.hs ফাইলে নিম্নলিখিত তথ্য থাকতে পারে।

|তথ্য|বর্ণনা|
---|---|
|মানচিত্র ফাইল
|তথ্য দেখুন|হেল্পসেটের মধ্যে নিযুক্ত ন্যাভিগেটরদের বর্ণনা করে এমন তথ্য। মানের নেভিগেটরগুলি হল: বিষয়বস্তুর সারণী, সূচী এবং পূর্ণ-পাঠ্য অনুসন্ধান। আরও ন্যাভিগেটরগুলির মধ্যে রয়েছে চকচকে এবং প্রিয় নেভিগেটরগুলিও। কাস্টম নেভিগেটর সম্পর্কিত ডেটা এখানে আরও সংযুক্ত করা হয়েছে।|
|হেল্পসেট শিরোনাম|দি \<title> হেল্পসেট (.hs) ফাইলের মধ্যে রূপরেখা দেওয়া আছে। এই শিরোনামটি সর্বাধিক উইন্ডোর সর্বোচ্চ এবং আপনার হেল্পসেট ফাইলে বর্ণিত যেকোন সেকেন্ডারি উইন্ডোতে বলে মনে হচ্ছে৷|
|হোম আইডি|(ডিফল্ট) আইডির শিরোনাম যা প্রদর্শিত হয় যখন কোনো আইডি নির্দেশ না করে সাহায্যকারীকে ডাকা হয়৷|
|প্রেজেন্টেশন|যে উইন্ডোতে সহায়তার বিষয়গুলি দেখানো হবে এটি JavaHelp 2 কম্পিউটার প্রোগ্রামের একটি আধুনিক অন্তর্ভুক্ত হতে পারে যা নীচে আরও বিস্তারিতভাবে চিত্রিত করা হয়েছে \<presentation> |
|সাব-হেল্পসেট|এই বিবেচ্য ক্ষেত্রটি ট্যাগ ব্যবহার করে স্ট্যাটিকভাবে অন্যান্য হেল্পসেটগুলিকে অন্তর্ভুক্ত করে। এই ট্যাগ দ্বারা দেখানো হেল্পসেটগুলি ট্যাগটি ধারণ করে এমন হেল্পসেটের সাথে স্বাভাবিকভাবে একত্রিত হয়। ব্লেন্ডিং হেল্পসেটগুলিতে ব্লেন্ডিং সম্পর্কে আরও বেশি আগ্রহের বিষয় পাওয়া যাবে
| বাস্তবায়ন এছাড়াও রেজিস্ট্রি একটি প্রদত্ত এমুলেট সাজানোর জন্য ক্লায়েন্টের কাছে পদার্থ দর্শককে সিদ্ধান্ত নেয়।|

## জাভা এইচএস ফাইল ফরম্যাট

জাভা এইচএস ফাইলগুলি XML ফাইল ফর্ম্যাটে এবং ওয়ার্ল্ড ওয়াইড ওয়েব কনসোর্টিয়াম (W3C) এক্সটেন্ডেড মার্কআপ ল্যাঙ্গুয়েজ প্রস্তাবিত সুপারিশ [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208) এর উপর ভিত্তি করে। এর মানে হল যে একটি জাভা এইচএস ফাইল মানুষের পঠনযোগ্য এক্সএমএল ফাইল ফরম্যাটে যা যেকোনো এক্সএমএল রিডার অ্যাপ্লিকেশনে খোলা যেতে পারে।

### জাভা এইচএস ফাইল ফরম্যাটের উদাহরণ

The following is an example of a helpset file as from [Oracle Helpset documentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## তথ্যসূত্র
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - হাসকেল স্ক্রিপ্ট ফাইল ফরম্যাট

## একটি HS ফাইল কি?

.hs এক্সটেনশন সহ একটি ফাইল হল একটি হাসকেল স্ক্রিপ্ট ফাইল যা [Haskell](https://wiki.haskell.org/Haskell) এ লেখা, একটি উন্নত বিশুদ্ধ-কার্যকর ওপেন সোর্স প্রোগ্রামিং ভাষা। HS ফাইলে লেখা কোডটি সম্পূর্ণরূপে ফাংশনের উপর ভিত্তি করে, [C](/programming/c/), [C++](/programming/cpp/) এবং একইভাবে, যা শক্তিশালী এবং সংক্ষিপ্ত সফ্টওয়্যারের দ্রুত বিকাশের মূলনীতি অনুসরণ করে। হ্যাস্কেল নমনীয় এবং উচ্চ-মানের অ্যাপ্লিকেশন তৈরি করতে সমৃদ্ধ API, প্রোফাইলার এবং ডিবাগারের সাথে অন্তর্নির্মিত একযোগে এবং সমান্তরালতা প্রদান করে।

## এইচএস ফাইল ফরম্যাট

যেকোনো প্রোগ্রামিং ভাষার মতো, HS ফাইলগুলি সাধারণ পাঠ্য বিন্যাসে লেখা হয় যা মানুষের পাঠযোগ্য। যেকোন উপলভ্য টেক্সট টুলের সাহায্যে এগুলি তৈরি, সম্পাদনা এবং দেখা যায়। .hs সোর্স কোড ফাইলটি একটি Haskell কম্পাইলার দিয়ে কম্পাইল করা হয়, এক্সিকিউটেবল বাইনারি ফাইল তৈরি করে।

### HS ফাইল ফরম্যাটের উদাহরণ

কোড একটি .hs ফাইলে লেখা এবং একটি হাসকেল কম্পাইলার যেমন [GHC](https://haskell.org/ghc) ব্যবহার করে কম্পাইল করা যেতে পারে। নিচের নমুনায় দেখানো কোডের নিচের লাইনটি `HelloWorld.hs` হিসেবে সংরক্ষিত হয়েছে।

```
main = putStrLn "Hello, World!"
```

এটি কমান্ড ব্যবহার করে সংকলিত হয়:

```
$ ghc -o hello hello.hs
```
এবং ফলস্বরূপ এক্সিকিউবল ফাইলটি এভাবে চালানো যেতে পারে:

```
$ ./hello
```
এটি প্রিন্ট করে হ্যালো, ওয়ার্ল্ড! আউটপুটে বিবৃতি।

## তথ্যসূত্র

 * [হাস্কেল](https://wiki.haskell.org/Haskell)
 * [হাস্কেল ৫টি সহজ ধাপে](https://wiki.haskell.org/Haskell_in_5_steps)

