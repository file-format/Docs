{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX फ़ाइल - HTML एक्सटेंशन फ़ाइल स्वरूप",
  "description" :"आपका फ़ाइल स्वरूप गाइड यह जानने के लिए कि HTX फ़ाइल और API क्या है जो HTX फ़ाइल बना और खोल सकता है।",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTX फाइल क्या है?

एक HTX फ़ाइल वास्तव में एक HTML फ़ाइल होती है जिसमें डेटाबेस क्वेरी परिणामों को वेबपेज के रूप में प्रदर्शित करने के लिए डेटा चर होते हैं। अधिकतर Microsoft फ्रंटपेज वेब डेवलपमेंट सॉफ़्टवेयर के साथ बनाई गई, HTX फ़ाइलें संबंधित इंटरनेट डेटाबेस कनेक्टर (.IDC) फ़ाइल के समान फ़ोल्डर में सहेजी जाने के लिए सहेजी जाती हैं।

HTX फाइलें Microsoft FrontPage और किसी भी टेक्स्ट एडिटर जैसे Notepad, TextEdit, या Atom जैसे एप्लिकेशन के साथ खोली जा सकती हैं।

## HTX फ़ाइल स्वरूप

डेटाबेस से डेटा पुनर्प्राप्त करने और प्रदर्शन के लिए चर में सहेजने के लिए कोड के साथ HTX फ़ाइलों को सादे पाठ फ़ाइल के रूप में सहेजा जाता है।


### HTX फ़ाइल उदाहरण

HTX फ़ाइल का एक उदाहरण इस प्रकार है जो क्वेरी प्रतिबंध प्रदर्शित करने के लिए पेज हेडर और उपयोगकर्ता को प्रदर्शित करने के लिए पेज पर प्रदर्शित दस्तावेज़ों को परिभाषित करता है।

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

इस नमूना कोड का आउटपुट इस प्रकार है।

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

जैसा कि देखा जा सकता है, HTX फ़ाइल एक टेम्प्लेट है जो स्वरूप देता है कि परिणाम कैसे लौटाए जाते हैं और अंतिम उपयोगकर्ताओं को प्रदर्शित किए जाते हैं। यह कुछ IIS एक्सटेंशन और इंडेक्सिंग सर्विस के साथ HTML फॉर्मेट में लिखा गया है। इन एक्सटेंशन में प्रसंस्करण परिणामों के लिए चर नाम और अन्य कोड शामिल हैं।

## संदर्भ

* [परिणामों को .Htx फ़ाइल में स्वरूपित करना](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

