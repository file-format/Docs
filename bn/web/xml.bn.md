{
  "date" : "2019-10-11",
  "keywords" : ["xml", "File", "Extension", "File Format", "File Extension", "extensible markup language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XML ফাইল ফরম্যাট",
  "description":"XML ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি XML ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## একটি XML ফাইল কি?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML ফাইল ফরম্যাট

XML ফাইল ফরম্যাট XML ডকুমেন্ট অবজেক্ট মডেল (DOM) এর উপর ভিত্তি করে যা HTML এবং XML নথিগুলির জন্য একটি প্রোগ্রামিং API। এক্সএমএল ডকুমেন্ট এক্সএমএল ডকুমেন্ট এলিমেন্ট অ্যাক্সেস এবং ম্যানিপুলেট করার জন্য একটি স্ট্যান্ডার্ড পদ্ধতি সংজ্ঞায়িত করে। এটি একটি XML নথির একটি ট্রি-স্ট্রাকচার ভিউ তৈরি করে যা DOM গাছের মাধ্যমে সমস্ত উপাদান অ্যাক্সেস করতে ব্যবহার করা যেতে পারে। এক্সএমএল ট্রিতে বিদ্যমান উপাদানগুলিকে সংশোধন/মুছে ফেলার পাশাপাশি নতুন উপাদান তৈরি করা যেতে পারে। একটি XML নথির প্রতিটি উপাদানকে নোড বলা হয়। XML DOM নিচের ছবিতে দেখানো হয়েছে।

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### XML এর সর্বজনীন পদ্ধতি

XML-এর শক্তি ডেটা পরিবহন এবং প্ল্যাটফর্ম পরিবর্তনগুলিকে সরলীকৃত করে নেটওয়ার্কের মাধ্যমে ডেটা যোগাযোগের জন্য এটিকে একটি সর্বজনীন ভাষা করে তোলে। এটি প্লেইন টেক্সট ফরম্যাটে ডেটা সংরক্ষণ করে বেমানান সিস্টেমগুলির মধ্যে ডেটা বিনিময় করা নিশ্চিত করে। HTML হল ওয়েবে ডেটা উপস্থাপনের জন্য, যেখানে XML হল ডেটা বিনিময়ের জন্য। XML-এর ভিতরে ব্যবহৃত মার্কআপ ট্যাগ জোড়াগুলি অ্যাপ্লিকেশন পড়ার মাধ্যমে ব্যবহার করা কাঠামোর মূল উপাদানগুলিকে সংজ্ঞায়িত করে।

## এক্সএমএল উদাহরণ

নীচে একটি সিডি ক্যাটালগের একটি সরলীকৃত উদাহরণ যেখানে প্রতিটি রেকর্ডে শিল্পী, দেশ, কোম্পানি, মূল্য এবং উত্পাদনের বছর হিসাবে সিডি সম্পর্কে তথ্য রয়েছে।

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## তথ্যসূত্র

* [XML - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/XML)


