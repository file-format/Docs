{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - ফাইন্যান্সিয়াল এক্সচেঞ্জ ফাইল ফরম্যাট খুলুন",
  "description":"OFX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি OFX ফাইল তৈরি করতে এবং খুলতে পারে।",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-bn",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## একটি OFX ফাইল কি?

একটি OFX (ওপেন ফাইন্যান্সিয়াল এক্সচেঞ্জ) ফাইল হল একটি আর্থিক ফাইল বিন্যাস যা সফ্টওয়্যার প্রোগ্রাম এবং আর্থিক প্রতিষ্ঠানের মধ্যে আর্থিক তথ্য বিনিময়ের জন্য ব্যবহৃত হয়। অভ্যন্তরীণ আর্থিক অ্যাকাউন্টিং বই রাখার জন্য সফ্টওয়্যার সমাধানগুলির বিবর্তনের সাথে, সফ্টওয়্যার প্রোগ্রামগুলি তৈরি করা হয়েছে যা আপনার ব্যাঙ্কের সাথে সংযোগ করতে পারে এবং ব্যাঙ্কগুলির সাথে আর্থিক ডেটা আমদানি বা রপ্তানি করতে পারে৷ এর মধ্যে আর্থিক ডেটা যেমন লেনদেন, অ্যাকাউন্টের তথ্য এবং বিল পেমেন্ট অন্তর্ভুক্ত রয়েছে। QuickBooks, Microsoft Money, Intuit এবং Quicken-এর মতো সফ্টওয়্যার প্রোগ্রাম OFX ফাইল হিসাবে আমদানি করা ডেটা সংরক্ষণ করে।

OFX ফাইল ফরম্যাটের জন্য ইন্টারনেট মিডিয়া টাইপ হল অ্যাপ্লিকেশন/x-ofx।

## OFX ফাইল ফরম্যাট

OFX ফাইলগুলি XML (এক্সটেনসিবল মার্কআপ ল্যাঙ্গুয়েজ) ফাইল ফর্ম্যাটে সংরক্ষিত হয় এবং ডেটা গঠন করতে ট্যাগ ব্যবহার করে। [XML](/web/xml/) ফাইলগুলি মানুষের পঠনযোগ্য বিন্যাসে সংরক্ষণ করা হয় এবং নোটপ্যাড, নোটপ্যাড++ বা অ্যাপল টেক্সটএডিটের মতো যেকোনো পাঠ্য সম্পাদকে খোলা ও সম্পাদনা করা যায়। OFX ফাইলগুলির মধ্যে সংরক্ষিত ডেটা **SGML (স্ট্যান্ডার্ড জেনারেলাইজড মার্কআপ ল্যাঙ্গুয়েজ)** স্ট্যান্ডার্ডের উপর ভিত্তি করে। OFX ফাইলের মধ্যে সংরক্ষিত ডেটা সাধারণত অন্তর্ভুক্ত করে:

* ব্যাংক সম্পর্কিত তথ্য

* ক্রেডিট এবং ডেবিট কার্ড তথ্য

* অ্যাকাউন্ট এবং বিনিয়োগ তথ্য

* অন্য কোন আর্থিক লেনদেন


### OFX ফাইল ফরম্যাটের উদাহরণ

নীচে একটি উদাহরণ OFX ফাইলের অভ্যন্তরীণ ডেটা কাঠামো এবং নমুনা ডেটা রয়েছে।

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

এই উদাহরণ OFX ফাইলে নিম্নলিখিত তথ্য রয়েছে:

 * ব্যাঙ্ক অ্যাকাউন্টের তথ্য যেমন ব্যাঙ্কের নাম, অ্যাকাউন্ট নম্বর এবং ব্যালেন্স
 * প্রতিটি লেনদেনের তারিখ, প্রকার এবং পরিমাণ সহ লেনদেনের তালিকা

অ্যাকাউন্টের লেনদেন এবং ব্যয়ের ট্র্যাক রাখতে এই সমস্ত তথ্য একটি ব্যক্তিগত অর্থায়ন সফ্টওয়্যার প্রোগ্রামে আমদানি করা যেতে পারে।

## তথ্যসূত্র ##

* [ওপেন ফাইন্যান্সিয়াল এক্সচেঞ্জ - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [ইলেক্ট্রনিক ডেটা এক্সচেঞ্জের জন্য আইএসও স্ট্যান্ডার্ড](https://en.wikipedia.org/wiki/ISO_20022)


