{
  "date" : "2019-10-11",
  "keywords" :["FODG फाइल", "FODG फाइल फॉर्मेट", "FODG फाइल क्या है", "फाइल", "FODG उदाहरण", "FODG फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument आरेखण फ़ाइल स्वरूप",
  "description":"FODG फ़ाइल स्वरूप और API के बारे में जानें जो FODG फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## FODG फाइल क्या है?

.fodg एक्सटेंशन वाली फाइल ड्राइंग एलिमेंट्स को स्टोर करने के लिए Apache OpenOffice Drawing फाइल फॉर्मेट है। यह स्ट्रक्चरल इंफॉर्मेशन स्टैंडर्ड्स (OASIS) के एडवांसमेंट द्वारा उल्लिखित फ़ाइल प्रारूप विनिर्देशों पर आधारित है। OpenOffice ग्राफ़िक्स के लिए एक अन्य समान फ़ाइल स्वरूप [ODG](/hi/image/odg/) है जो आरेखण तत्वों को सदिश छवि के रूप में संग्रहीत करता है। FODG फाइलें OpenOffice के साथ-साथ LibreOffice में भी खोली जा सकती हैं। OpenOffice द्वारा समर्थित अन्य फ़ाइल स्वरूपों में, उदाहरण के लिए, [ODT](/hi/word-processing/odt/), ODF, [ODP](/hi/presentation/odp/) और [ODS](/hi/spreadsheet/ods/) शामिल हैं।

## FODG फ़ाइल स्वरूप

FODG OpenDocument के XML फ़ाइल स्वरूप पर आधारित है जो OASIS OpenDocument Format ISO/IEC 26300 के अनुरूप है। इसमें इंटरनेट मीडिया प्रकार application/vnd.oasis.opendocument.graphics है और यह org.oasis-open.opendocument public.composite-content के अनुरूप भी है। . XML संरचना सभी दस्तावेज़ प्रकारों जैसे स्प्रेडशीट, ड्राइंग फ़ाइलें और पाठ दस्तावेज़ों के लिए सामान्य है। OpenOffice दस्तावेज़ सामग्री, शैलियों, मेटाडेटा और एप्लिकेशन सेटिंग्स को चार अलग-अलग XML फ़ाइलों में अलग करके चिंताओं को अलग करने का लाभ उठाते हैं।

`<office:document-content>` - सामग्री में प्रयुक्त दस्तावेज़ सामग्री और स्वचालित शैलियाँ।
`<office:document-styles>` - दस्तावेज़ सामग्री में उपयोग की जाने वाली शैलियाँ और स्वयं शैलियों में उपयोग की जाने वाली स्वचालित शैलियाँ।
`<office:document-meta>` - दस्तावेज़ मेटा जानकारी, जैसे कि लेखक या अंतिम सेव एक्शन का समय।
`<office:document-settings>` - एप्लिकेशन-विशिष्ट सेटिंग्स, जैसे विंडो आकार या प्रिंटर जानकारी।

## संदर्भ ##
* [v 1.3 मानकीकरण के लिए भविष्य की विशिष्टताएँ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [कार्यालय अनुप्रयोगों के लिए OASIS खुला दस्तावेज़ प्रारूप](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - विकिपीडिया](https://en.wikipedia.org/wiki/OpenDocument)

