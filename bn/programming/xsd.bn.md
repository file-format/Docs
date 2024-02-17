{
  "date" : "2022-02-06",
  "keywords" : [ "xsd", ".xsd","what is a xsd file","how to open xsd file", "extension", "file", "xsd file","xsd file format",  ".xsd extension" ,"xsd file example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" : " XSD ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা একটি XSD ফাইল তৈরি এবং খুলতে পারে।",
  "title" : "XSD ফাইল ফরম্যাট - XML স্কিমা সংজ্ঞা ফাইল",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## একটি XSD স্কিমা ফাইল কি?

একটি XSD ফাইল হল একটি সংজ্ঞা ফাইল যা একটি XML নথির অংশ হতে পারে এমন উপাদান এবং গুণাবলী নির্দিষ্ট করে। এটি নিশ্চিত করে যে ডেটা সঠিকভাবে ব্যাখ্যা করা হয়েছে, এবং ত্রুটি ধরা পড়েছে, যার ফলে উপযুক্ত XML বৈধতা পাওয়া যায়। XSD ফাইলগুলি নিশ্চিত করে যে প্রবেশ করা ডেটা ফাইলে সংজ্ঞায়িত একই কাঠামো অনুসরণ করে। XSD ফাইলগুলি [XML](/web/xml/) ফাইল ফরম্যাটে সংরক্ষিত থাকে এবং Microsoft Notepad, Notepad++, বা [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)-এর মতো যেকোনো টেক্সট এডিটরে খোলা বা সম্পাদনা করা যায়।

## XSD ফাইল ফরম্যাট

XSD ফাইলগুলি সাধারণ পাঠ্য ফাইল বিন্যাসে ডিস্কে সংরক্ষণ করা হয় যা মানুষের পাঠযোগ্য। একটি XSD সেই উপাদানগুলিকে সংজ্ঞায়িত করে যা নথিতে ব্যবহার করা যেতে পারে, প্রকৃত ডেটার সাথে সম্পর্কিত যা এটি এনকোড করা হবে।

## XSD ফাইলের উদাহরণ

ক্রয় অর্ডার স্কিমা সহ একটি সাধারণ XSD ফাইল নিম্নলিখিত [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022) এ দেখানো ট্যাগ ব্যবহার করে উপাদানগুলিকে সংজ্ঞায়িত করে৷

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

এখানে, নিম্নলিখিত ট্যাগ ব্যবহার করা হয়.

 * `xs: element` - একটি উপাদান সংজ্ঞায়িত করে।
 * `xs:sequence` - বোঝায় যে শিশু উপাদানগুলি শুধুমাত্র উল্লিখিত ক্রমে প্রদর্শিত হবে।
 * `xs:complexType` - বোঝায় এতে অন্যান্য উপাদান রয়েছে।
 * `xs:simpleType` - বোঝায় যে এতে অন্য উপাদান নেই।
 * `টাইপ` - স্ট্রিং, দশমিক, পূর্ণসংখ্যা, বুলিয়ান, তারিখ, সময়,

## তথ্যসূত্র ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

