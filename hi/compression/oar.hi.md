{
  "date" : "2021-04-08",
  "keywords" :[ "ओअर फाइल", "ओअर फाइल फॉर्मेट", "ओअर फाइल क्या है", "फाइल", "ओअर उदाहरण", "ओअर फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator संग्रह फ़ाइल स्वरूप",
  "description":"OAR फ़ाइल स्वरूप और API के बारे में जानें जो OAR फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## ओएआर फाइल क्या है?

.oar एक्सटेंशन वाली फ़ाइल OpenSimulator एप्लिकेशन द्वारा उपयोग की जाने वाली एक आर्काइव फ़ाइल है जो नेटवर्क पर बहु-उपयोगकर्ताओं के लिए सुलभ वर्चुअल वातावरण बनाने के लिए एक ओपन-सोर्स 3D एप्लिकेशन सर्वर है। ओएआर फ़ाइल प्रारूप एक अलग सिस्टम पर इलाके, वस्तु बनावट और सूची को पूरी तरह से लोड करने के लिए आवश्यक आवश्यक संपत्ति डेटा प्रदान करता है। OpenSimulator में वैकल्पिक हाइपरग्रिड भी है जो उपयोगकर्ताओं को पूरे वेब पर अन्य OpenSimulator स्थापनाओं पर जाने की अनुमति देता है। OAR फ़ाइलों में इंटरनेट MIME प्रकार का अनुप्रयोग/oar होता है और इसमें एक या अधिक संग्रहीत फ़ाइलें होती हैं।


## ओएआर फ़ाइल प्रारूप

OAR बाइनरी फ़ाइलें हैं जो संपीड़ित संग्रह फ़ाइल स्वरूप में संग्रहीत हैं। OAR फ़ाइल स्वरूप का नवीनतम संस्करण [संस्करण 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) है जिसमें इसके पिछले [संस्करण 0.8](http://opensimulator.org/wiki/OAR_Format_0.8) से बड़े बदलाव हैं। । नवीनतम संस्करण एक ही OAR में कई क्षेत्रों को संग्रहीत करने का समर्थन करता है और 0.7.5 से पहले OpenSimulator के संस्करणों के साथ पीछे की ओर संगत नहीं है। एक OAR फ़ाइल मूल यूनिक्स टार प्रारूप (USTAR नहीं) में एक gzipped tar फ़ाइल (tar.gz) है।

## ओएआर क्षेत्र उदाहरण
AOR फ़ाइलों में कई क्षेत्र हो सकते हैं। संग्रह की संरचना इस प्रकार है (इस उदाहरण में 4 क्षेत्र हैं):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## ओएआर संग्रह.xml

भविष्य के प्रारूप परिवर्तनों के साथ संगतता को परिभाषित करने के लिए संग्रह नियंत्रण फ़ाइल में एक प्रमुख संस्करण संख्या है। ओएआर प्रारूप में संपत्तियों की उपस्थिति बूलियन तत्व द्वारा इंगित की जाती है<assets_included> . शामिल क्षेत्रों के बारे में जानकारी एक मेनिफेस्ट में निहित है जो नियंत्रण फ़ाइल में मौजूद है। Archive.xml का एक उदाहरण इस प्रकार है।

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## संदर्भ

* [ओएआर प्रारूप v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [ओपनसिम्युलेटर](http://opensimulator.org/wiki/Main_Page)

