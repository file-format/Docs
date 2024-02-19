{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "WSDL ফাইল ফরম্যাট - ওয়েব পরিষেবার বর্ণনা ভাষা ফাইল",
  "description": "একটি WSDL ফাইল এবং API যা WSDL ফাইল তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন।",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsdl-bn"
    }
  },
  "lastmod": "2022-02-03"
}

## একটি WSDL ফাইল কি?

একটি WSDL ফাইল হল একটি ওয়েব পরিষেবার বর্ণনা ভাষার ফাইল যা ওয়েব পরিষেবাগুলি বর্ণনা করার জন্য XML ভাষায় লেখা হয়। এটি সর্বজনীনভাবে স্বীকৃত বিন্যাসে বহির্বিশ্বের সাথে সংযোগের জন্য শেষ পয়েন্ট বা ইন্টারফেস সম্পর্কে তথ্য রয়েছে। [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (W3C.org দ্বারা রক্ষণাবেক্ষণ করা হয়েছে) পোর্ট এবং এন্ডপয়েন্টগুলিতে দূরবর্তী অ্যাপ্লিকেশন অ্যাক্সেস পাওয়ার জন্য ডেটা বিনিময়ের জন্য ডেটা ফিড প্রকাশ করার শর্তাবলী সংজ্ঞায়িত করে৷

## WSDL ফাইল ফরম্যাট - আরও তথ্য

WSDL ফাইলগুলি XML ফাইল হিসাবে সংরক্ষিত হয় যা মানুষের পাঠযোগ্য এবং বিষয়বস্তু দেখার জন্য যে কোনও পাঠ্য সম্পাদকে খোলা যেতে পারে।

## WSDL পরিষেবা বিবরণ

WSDL 2.0 ফাইল ফরম্যাটের স্পেসিফিকেশন WSDL পরিষেবাকে দুটি ধাপের সমন্বয়ে বর্ণনা করে:

- বিমূর্ত পর্যায়
- কংক্রিট মঞ্চ

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### WSDL পরিষেবাগুলির সাথে ইন্টারফেস করার জন্য কোন প্রযুক্তি ব্যবহার করা যেতে পারে?

ASP.NET, C/C++, এবং জাভা অ্যাপ্লিকেশন সহ WSDL পরিষেবাগুলির সাথে ইন্টারফেস করার জন্য বেশ কয়েকটি ভিন্ন প্রযুক্তি ব্যবহার করা যেতে পারে।

## WSDL উদাহরণ

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

এই উদাহরণে, portType glossaryTerms setTerm নামে একটি একমুখী অপারেশন সংজ্ঞায়িত করে।

## তথ্যসূত্র

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL ফাইল ফর্ম্যাট স্পেসিফিকেশন](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


