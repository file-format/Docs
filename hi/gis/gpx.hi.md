{
  "date" : "2019-10-11",
  "keywords" :[ "जीपीएक्स फाइल", "एक जीपीएक्स फाइल क्या है", "फाइल", "जीपीएक्स उदाहरण", "जीपीएक्स फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX एक्सचेंज फ़ाइल स्वरूप",
  "description":"GPX फ़ाइल स्वरूप और API के बारे में जानें जो GPX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## GPX फ़ाइल क्या है?

जीपीएक्स एक्सटेंशन वाली फाइलें इंटरनेट पर एप्लिकेशन और वेब सेवाओं के बीच जीपीएस डेटा के आदान-प्रदान के लिए जीपीएस एक्सचेंज प्रारूप का प्रतिनिधित्व करती हैं। यह एक हल्के वजन का एक्सएमएल फ़ाइल प्रारूप है जिसमें जीपीएस डेटा यानी वेपॉइंट, मार्ग और ट्रैक शामिल हैं जिन्हें कई कार्यक्रमों द्वारा आयात और लाल किया जाना है। GPX फ़ाइल स्वरूप खुला है और विभिन्न अनुप्रयोगों और GPS उपकरणों द्वारा समर्थित है। ऐसी फाइलों से जीपीएस डेटा भू-स्थानिक उद्देश्यों के लिए मानचित्रण अनुप्रयोगों पर प्रदर्शित करने के लिए लोड किया जा सकता है।

## GPX फ़ाइल स्वरूप ##

एक GPX फ़ाइल में अक्षांश और देशांतर स्थान डेटा, ऊंचाई मान और अन्य संभवतः अन्य वर्णनात्मक जानकारी होती है। स्थान डेटा दशमलव डिग्री के रूप में व्यक्त किया जाता है और ऊंचाई मीटर में व्यक्त की जाती है। GPX फ़ाइल में समय ISO 8601 प्रारूप का उपयोग करके कोऑर्डिनेटेड यूनिवर्सल टाइम (UTC) में होता है। GPX फ़ाइल का उपयोग करने के लाभ इस प्रकार हैं:

* GPX आपको Windows, MacOS, Linux, Palm और PocketPC के लिए प्रोग्रामों की बढ़ती सूची के साथ डेटा का आदान-प्रदान करने की अनुमति देता है।
* GPX को एक साधारण वेबपेज या कन्वर्टर प्रोग्राम का उपयोग करके अन्य फ़ाइल स्वरूपों में बदला जा सकता है।
* GPX XML मानक पर आधारित है, इसलिए आपके द्वारा उपयोग किए जाने वाले कई नए प्रोग्राम (उदाहरण के लिए Microsoft Excel) GPX फ़ाइलें पढ़ सकते हैं।
* GPX वेब पर किसी के लिए भी नई सुविधाओं को विकसित करना आसान बनाता है जो आपके पसंदीदा कार्यक्रमों के साथ तुरंत काम करेगी।

[GPX स्कीमा](https://www.topografix.com/GPX/1/1/gpx.xsd) संदर्भ के लिए GPX फ़ाइल स्वरूप का प्रतिनिधित्व दिखाता है।

### आवश्यक डेटा ###

निम्नलिखित आवश्यक डेटा है जो GPS डेटा के प्रतिनिधित्व के लिए GPX फ़ाइल का हिस्सा है।

* **वेपॉइंट**: एक वेपॉइंट एक WGS84 (GPS) एक बिंदु का निर्देशांक है और OGR प्रकार wkbPoint की सुविधाओं की परत का प्रतिनिधित्व करता है
* **मार्ग**: OGR प्रकार wkbLineString की सुविधाओं की एक परत का प्रतिनिधित्व करते हैं। इसमें ट्रैक बिंदुओं की एक सूची शामिल है, जो एक मोड़ या चरण बिंदु दिखाने वाले मार्ग बिंदु हैं जो एक गंतव्य की ओर ले जाते हैं
* **ट्रैक**: ट्रैक OGR प्रकार wkbMultiLineString की विशेषताओं की परत का प्रतिनिधित्व करते हैं। यह कम से कम एक खंड से बना होता है जिसमें पथ का वर्णन करने वाले बिंदुओं की एक क्रमबद्ध सूची में वेपॉइंट होते हैं। इसमें ट्रैक बिंदुओं की एक सूची होती है जो एक सतत जीपीएस ट्रैक का प्रतिनिधित्व करती है।

### GPX उदाहरण फ़ाइल ###

निम्न GPX फ़ाइल GPX फ़ाइल में GPS डेटा के संगठन को दिखाती है और GPX फ़ाइल की सामग्री के बारे में एक अच्छा विचार दे सकती है।

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## संदर्भ ##

* [GPX फ़ाइल स्वरूप] (http://www.topografix.com/gpx.asp)
* [जीपीएक्स - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/GPS_Exchange_Format)
