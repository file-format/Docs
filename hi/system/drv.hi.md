{
  "date" : "2021-07-08",
  "keywords" :["डीआरवी", "एक्सटेंशन", "फाइल", "प्रारूप", "सिस्टम", "ड्राइवर", "विंडोज डिवाइस ड्राइवर", "प्रोग्राम", "कंप्यूटर", "एप्लिकेशन"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - विंडोज डिवाइस ड्राइवर",
  "description":"DRV फ़ाइल स्वरूप और API के बारे में जानें जो DRV फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## डीआरवी फ़ाइल क्या है? ##

.drv एक्सटेंशन वाली फ़ाइलें Windows डिवाइस ड्राइवर से संबंधित होती हैं। विंडोज ऑपरेटिंग सिस्टम आंतरिक और बाहरी हार्ड डिवाइस को जोड़ने के लिए इन फाइलों का उपयोग करता है। DRV फाइलें एक डिवाइस और ऑपरेटिंग सिस्टम को एक साथ कैसे लिंक करती हैं, इसके लिए निर्देश और पैरामीटर शामिल हैं। ये फ़ाइलें Windows के साथ उचित कार्य करने के लिए डिवाइस ड्राइवर स्थापित करने में सहायता करती हैं। इसके अलावा, पीसी के मदरबोर्ड से बस या केबल के माध्यम से जुड़े उपकरणों को DRV फ़ाइलों की आवश्यकता होती है।


## DRV फ़ाइल स्वरूप ##

DRV फ़ाइलें आमतौर पर गतिशील पुस्तकालयों ([DDL](/hi/system/dll/) फ़ाइलें) या [EXE](/hi/executable/exe/) फ़ाइलों के रूप में पैक की जाती हैं। इन फ़ाइलों को सभी सिस्टम प्लेटफ़ॉर्म पर समर्थित किया जा सकता है, जैसे स्मार्टफ़ोन, और इस बात का कोई आश्वासन नहीं है कि प्रत्येक प्लेटफ़ॉर्म इन फ़ाइलों का ठीक से समर्थन करेगा। हालाँकि, .drv फ़ाइल एक्सटेंशन का उपयोग करने वाले कुछ सबसे सामान्य उपकरण हैं:

* ध्वनि कार्ड
* ग्राफिक कार्ड
* प्रिंटर
* भंडारण उपकरणों
* संचार अनुकूलक
* कंप्यूटर हार्डवेयर सहायक उपकरण

ईमेल द्वारा भेजी गई DRV फ़ाइलों को न खोलने की अनुशंसा की जाती है क्योंकि इस फ़ाइल स्वरूप में वायरस और अन्य दुर्भावनापूर्ण प्रोग्राम होते हैं। किसी भी अज्ञात DRV फ़ाइल को खोलने से पहले एक व्यापक स्कैन करना सुनिश्चित करें।


## डीआरवी उदाहरण ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

