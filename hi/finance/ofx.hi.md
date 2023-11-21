{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ओएफएक्स - ओपन फाइनेंशियल एक्सचेंज फ़ाइल फॉर्मेट",
  "description":"ओएफएक्स फ़ाइल प्रारूप और एपीआई के बारे में जानें जो ओएफएक्स फाइलें बना और खोल सकते हैं।",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## OFX फ़ाइल क्या है?

ओएफएक्स (ओपन फाइनेंशियल एक्सचेंज) फ़ाइल एक वित्तीय फ़ाइल प्रारूप है जिसका उपयोग सॉफ्टवेयर प्रोग्राम और वित्तीय संस्थानों के बीच वित्तीय जानकारी के आदान-प्रदान के लिए किया जाता है। इन-हाउस वित्तीय लेखांकन बहीखाता पद्धति के लिए सॉफ़्टवेयर समाधानों के विकास के साथ, सॉफ़्टवेयर प्रोग्राम विकसित किए गए हैं जो आपके बैंक से जुड़ सकते हैं और बैंकों के साथ वित्तीय डेटा आयात या निर्यात कर सकते हैं। इसमें लेनदेन, खाता जानकारी और बिल भुगतान जैसे वित्तीय डेटा शामिल हैं। QuickBooks, Microsoft Money, Intuit और Quicken जैसे सॉफ़्टवेयर प्रोग्राम आयातित डेटा को OFX फ़ाइल के रूप में सहेजते हैं।

OFX फ़ाइल स्वरूप के लिए इंटरनेट मीडिया प्रकार एप्लिकेशन/x-ofx है।

## OFX फ़ाइल स्वरूप

OFX फ़ाइलें XML (एक्स्टेंसिबल मार्कअप लैंग्वेज) फ़ाइल स्वरूप में सहेजी जाती हैं और डेटा को संरचित करने के लिए टैग का उपयोग करती हैं। [XML](/hi/web/xml/) फ़ाइलें मानव पठनीय प्रारूप में संग्रहीत की जाती हैं और इन्हें नोटपैड, नोटपैड++, या ऐप्पल टेक्स्टएडिट जैसे किसी भी टेक्स्ट एडिटर में खोला और संपादित किया जा सकता है। OFX फ़ाइलों के अंदर संग्रहीत डेटा **SGML (मानक सामान्यीकृत मार्कअप भाषा)** मानक पर आधारित है। OFX फ़ाइलों के अंदर संग्रहीत डेटा में आम तौर पर शामिल हैं:

*बैंकों से संबंधित जानकारी
* क्रेडिट और डेबिट कार्ड की जानकारी
* खाते और निवेश की जानकारी
* कोई अन्य वित्तीय लेनदेन

### ओएफएक्स फ़ाइल प्रारूप उदाहरण

उदाहरण OFX फ़ाइल की आंतरिक डेटा संरचना और नमूना डेटा निम्नलिखित है।

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

इस उदाहरण OFX फ़ाइल में निम्नलिखित जानकारी है:

* बैंक खाते की जानकारी जैसे बैंक का नाम, खाता संख्या और शेष राशि
* प्रत्येक लेनदेन की तारीख, प्रकार और राशि सहित लेनदेन की सूची

खाते के लेनदेन और खर्चों पर नज़र रखने के लिए यह सारी जानकारी व्यक्तिगत वित्त सॉफ़्टवेयर प्रोग्राम में आयात की जा सकती है।

## सन्दर्भ ##

* [विकिपीडिया द्वारा ओपन फाइनेंशियल एक्सचेंज](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [इलेक्ट्रॉनिक डेटा एक्सचेंज के लिए आईएसओ मानक](https://en.wikipedia.org/wiki/ISO_20022)

