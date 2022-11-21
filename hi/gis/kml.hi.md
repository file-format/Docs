{
  "date" : "2019-10-11",
  "keywords" :[ "किमी फ़ाइल", "किमी फ़ाइल क्या है", "फ़ाइल", "केएमएल उदाहरण", "केएमएल फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"केएमएल - कीहोल मार्कअप लैंग्वेज",
  "description":"KML फ़ाइल स्वरूप और API के बारे में जानें जो KML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## KML फ़ाइल क्या है?

KML, कीहोल मार्कअप लैंग्वेज) में XML संकेतन में भू-स्थानिक जानकारी होती है। KML के रूप में सहेजी गई फ़ाइलें भौगोलिक सूचना प्रणाली (GIS) अनुप्रयोगों में खोली जा सकती हैं बशर्ते वे इसका समर्थन करें। अंतर्राष्ट्रीय मानक के रूप में अपनाए जाने के बाद कई अनुप्रयोगों ने KML फ़ाइल स्वरूप के लिए समर्थन प्रदान करना शुरू कर दिया है। KML नेस्टेड तत्वों और विशेषताओं के साथ टैग-आधारित संरचना का उपयोग करता है। सभी टैग केस-संवेदी होते हैं और [KML](https://developers.google.com/kml/documentation/kmlreference) संदर्भ के अनुसार इन टैग्स के क्रम का पालन करना महत्वपूर्ण है।

## संक्षिप्त इतिहास ##

KML को मूल रूप से Google धरती के उपयोग के लिए विकसित किया गया था जिसे मूल रूप से कीहोल अर्थ व्यूअर के रूप में जाना जाता था। केएलएम को 2008 में ओपन जियोस्पेशियल कंसोर्टियम द्वारा 2008 में अंतरराष्ट्रीय मानक के रूप में अपनाया गया था। चूंकि प्रारूप को Google धरती के साथ उपयोग के लिए विकसित किया गया था, इसलिए इसे केएमएल फाइलों को देखने और संपादित करने वाला पहला व्यक्ति होने का गौरव प्राप्त है। समय बीतने के साथ, अब अधिक से अधिक परियोजनाएं हैं जो विभिन्न भाषाओं में कई एपीआई सहित केएमएल फ़ाइल स्वरूपों के लिए समर्थन प्रदान करती हैं।

## KML फ़ाइल स्वरूप निर्दिष्टीकरण ##

KML संदर्भ पूर्ण फ़ाइल प्रारूप विनिर्देशों के लिए संदर्भ देने के लिए एक संपूर्ण मार्गदर्शिका है। एक मानक KML फ़ाइल में निम्न शामिल होते हैं:

* स्थान-चिह्न
* वर्णनात्मक HTML स्थल-चिह्नों में
* ग्राउंड ओवरले
* पथ
*बहुभुज

इनके अतिरिक्त, KML फ़ाइल के उन्नत संस्करण में निम्न हो सकते हैं:

* ज्यामिति के लिए शैलियाँ
* हाइलाइट किए गए चिह्नों के लिए शैलियाँ
* स्क्रीन ओवरले
* नेटवर्क लिंक

प्रत्येक KML तत्व में लंबे समय तक जानकारी होती है जो फ़ाइल में मौजूद जानकारी को भू-पता लगाती है। हालांकि, शीर्षक, ऊंचाई और झुकाव जैसे अतिरिक्त पैरामीटर भी हो सकते हैं।

### प्लेसमार्क ###

इसका उपयोग पृथ्वी की सतह पर एक स्थिति का प्रतिनिधित्व करने के लिए किया जाता है और इसकी पहचान द्वारा की जाती है<Point> तत्व। निम्नलिखित एक उदाहरण है कि KML फ़ाइल में किसी स्थान-चिह्न का प्रतिनिधित्व कैसे किया जाता है।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### स्थान-चिह्नों में वर्णनात्मक HTML ###

अतिरिक्त जानकारी को प्लेसमार्क के साथ जोड़ा जा सकता है जो प्लेसमार्क के प्रतिनिधित्व को और बढ़ाता है। ऐसी जानकारी में लिंक, फ़ॉन्ट आकार, शैली और रंग शामिल हैं। इसके अलावा, इसमें प्लेसमार्क का हिस्सा बनने के लिए टेक्स्ट अलाइनमेंट और टेबल भी शामिल हैं।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### ग्राउंड ओवरले ###

ये पृथ्वी की सतह पर एक छवि की परत का प्रतिनिधित्व करते हैं।<icon> elment में ओवरले छवि फ़ाइल का लिंक होता है।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### पथ ###

पथों का प्रतिनिधित्व द्वारा किया जाता है<LineString> तत्व जो अक्षांश-लंबे जोड़े का संग्रह है। इनका उपयोग करके Google धरती में कई अलग-अलग प्रकार के पथ बनाए जा सकते हैं।

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML फ़ाइल में स्थानिक संदर्भ ##

भू-स्थानों के बारे में किसी भी भू-स्थानिक फ़ाइल में निहित जानकारी के स्थानिक संदर्भ जानकारी के बिना अलग-अलग अर्थ हो सकते हैं। डिफ़ॉल्ट रूप से, KML फ़ाइल के स्थानिक संदर्भ को वर्ल्ड जियोडेटिक सिस्टम ऑफ़ 1984, WGS84 द्वारा परिभाषित किया गया है।

## संदर्भ ##

* [केएमएल संदर्भ](https://developers.google.com/kml/documentation/kmlreference)
* [KML के लिए Google डेवलपर ट्यूटोरियल](https://developers.google.com/kml/documentation/kml_tut)
* [केएमएल फ़ाइल प्रारूप](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

