{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - ব্যবসা এবং আর্থিক রিপোর্টিং ফাইল ফর্ম্যাট",
  "description":"XBRL ফাইল ফরম্যাট এবং এপিআই সম্পর্কে জানুন যা XBRL ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-bn",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## একটি XBRL ফাইল কি?

.xbrl (এক্সটেনসিবল বিজনেস রিপোর্টিং ল্যাঙ্গুয়েজ) এক্সটেনশন সহ একটি ফাইল হল ব্যবসার তথ্য বিনিময়ের জন্য একটি অবাধে উপলব্ধ এবং বিশ্বব্যাপী কাঠামো। এটি এখন ব্যাপকভাবে একটি মান বিন্যাস হিসাবে ব্যবহৃত হয় যা পুরানো কাগজ-ভিত্তিক প্রতিবেদনগুলিকে আরও দরকারী এবং সঠিক ডিজিটাল রেকর্ডগুলির সাথে প্রতিস্থাপন করেছে। এক্সবিআরএল ফাইলগুলি ব্যবহার করে আদান-প্রদান করা ডেটা লেজার, আর্থিক বিবরণ এবং ব্যালেন্স শীট অন্তর্ভুক্ত করে। এটি ডেটা ট্যাগগুলিকে সমর্থন করে যা প্রস্তুতি থেকে সমস্ত ধরণের ব্যবসায়িক তথ্যের বিশ্লেষণের পর্যায় পর্যন্ত ডেটা প্রক্রিয়াকরণের অনুমতি দেয়। XBRL ফাইলগুলি রিভেট সফ্টওয়্যার ড্রাগন ভিউ XBRL ভিউয়ার এবং [Aspose.Finance](https://products.aspose.com/finance/)-এর মতো API-এর মতো সফ্টওয়্যার ব্যবহার করে খোলা যেতে পারে৷

## XBRL ফাইল ফরম্যাট

XBRL হল ডিজিটাল বিজনেস রিপোর্টিংয়ের জন্য একটি উন্মুক্ত আন্তর্জাতিক মান যা বিশ্বব্যাপী ব্যাপকভাবে ব্যবহৃত হয়। এটি একটি [XML](/web/xml/) ভিত্তিক ভাষা যা এক্সবিআরএল উপাদানগুলি ব্যবহার করে, যা ট্যাগ নামে পরিচিত, ব্যবসার ডেটার প্রতিটি আইটেম বর্ণনা করতে রিপোর্ট বাছাই এবং বিশ্লেষণের জন্য ডেটা তৈরি করে৷ XBRL ফাইল ফরম্যাট স্পেসিফিকেশন XBRL ইন্টারন্যাশনাল, ইনকর্পোরেটেড দ্বারা বিকশিত এবং প্রকাশ করা হয়েছে, বর্তমানে ব্যবহারকারীদের জন্য [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) উপলব্ধ।

### XBRL ডকুমেন্ট স্ট্রাকচার

এই ফাইল ফরম্যাটে কাজ করার জন্য অ্যাপ্লিকেশন লিখতে প্রোগ্রামাররা [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) সম্পর্কে সম্পূর্ণ তথ্য উল্লেখ করতে পারেন। একটি XBRL একটি XBRL দৃষ্টান্ত এবং শ্রেণীকরণের একটি সংগ্রহ নিয়ে গঠিত।

**`XBRL দৃষ্টান্ত`** - XBRL দৃষ্টান্তটি দিয়ে শুরু হয়<xbrl> মূল উপাদান। একটি বড় XML নথিতে একাধিক XBRL দৃষ্টান্ত এমবেড করা থাকতে পারে।

**`XBRL শ্রেণীবিন্যাস`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) একটি XML স্কিমা স্ট্রাকচার হিসেবে সংজ্ঞায়িত করা হয়েছে এবং সরাসরি রেফারেন্স করা বাহ্যিক লিঙ্ক উপাদানের সেট। লিঙ্কবেস রেফারেন্স দেখানো একটি মাপযোগ্য শ্রেণীবিন্যাস স্কিমা অনুসরণ করা হয়েছে।

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## তথ্যসূত্র ##

* [XBRL - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/XBRL)

* [এক্সটেনসিবল বিজনেস রিপোর্টিং ল্যাঙ্গুয়েজ (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


