{
  "date" : "2021-02-01",
  "keywords" :[ "यूएसडी", "यूएसडी फाइल", "यूएसडी फाइल फॉर्मेट", "फाइल फॉर्मेट", "फाइल", "एक्सटेंशन", "3 डी"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"यूएसडी - यूनिवर्सल सीन विवरण प्रारूप",
  "description":"USD फ़ाइल स्वरूप और API के बारे में जानें जो USD फ़ाइलें खोल और बना सकते हैं।",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## यूएसडी फाइल क्या है?

.usd एक्सटेंशन वाली फ़ाइल एक यूनिवर्सल सीन विवरण फ़ाइल स्वरूप है जो डिजिटल सामग्री निर्माण अनुप्रयोगों के बीच डेटा इंटरचेंजिंग और संवर्द्धन के उद्देश्य से डेटा को एन्कोड करता है। पिक्सर द्वारा विकसित, [यूएसडी](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) मौलिक संपत्तियों (जैसे मॉडल) या एनीमेशन को इंटरचेंज करने की क्षमता प्रदान करता है।

## यूएसडी फ़ाइल प्रारूप

यूएसडी फाइलों में बाइनरी प्रारूप (क्रेट फाइल के रूप में भी जाना जाता है) या एएससीआईआई-समर्थित फाइलें हो सकती हैं। ये दोनों फ़ाइल प्रारूप विनिमेय हैं जहां संदर्भों को स्रोतों को बदले बिना .usd संपत्तियों से जोड़ा जा सकता है। यूएसडी फ़ाइल प्रारूप में स्क्रिप्टिंग के लिए पायथन बाइंडिंग के साथ सी ++ पुस्तकालयों का एक सेट होता है। यह किसी भी संख्या में 3D दृश्य तत्वों जैसे वर्चुअल सेट, दृश्यों और शॉट्स के संयोजन और संगठन को उन्हें एप्लिकेशन से एप्लिकेशन तक प्रसारित करने में सक्षम बनाता है।

### यूएसडी डेटा प्रकार

USD फ़ाइल स्वरूप द्वारा समर्थित मूलभूत डेटा प्रकार निम्न तालिका में सूचीबद्ध हैं।

|वैल्यू टाइप टोकन |सी++ टाइप |विवरण|
---|---|---|
|बूल|बूल||
|uchar|uint8_t|8 बिट अहस्ताक्षरित पूर्णांक|
|int|int32_t|32 बिट हस्ताक्षरित पूर्णांक|
|uint|uint32_t|32 बिट अहस्ताक्षरित पूर्णांक|
|int64|int64_t|64 बिट हस्ताक्षरित पूर्णांक|
|uint64|uint64_t|64 बिट अहस्ताक्षरित पूर्णांक|
|हाफ|जीएफहाफ|16 बिट फ्लोटिंग पॉइंट|
|फ्लोट|फ्लोट|32 बिट फ्लोटिंग पॉइंट|
|डबल|डबल|64 बिट फ्लोटिंग पॉइंट|
|timecode|SdfTimeCode|दोहरा समाधान योग्य समय का प्रतिनिधित्व करता है|
|स्ट्रिंग|एसटीडी::स्ट्रिंग|एसटीएल स्ट्रिंग|
|टोकन|TfToken|तेज तुलना और हैशिंग के साथ इंटर्न की गई स्ट्रिंग|
|asset|SdfAssetPath|एक अन्य संपत्ति के लिए एक समाधान योग्य पथ का प्रतिनिधित्व करता है|
|matrix2d|GfMatrix2d|2x2 डबल्स का मैट्रिक्स|
|matrix3d|GfMatrix3d|3x3 डबल्स का मैट्रिक्स|
|matrix4d|GfMatrix4d|4x4 डबल्स का मैट्रिक्स|
|quatd|GfQuatd|डबल-सटीक quaternion|
|quatf|GfQuatf|एकल-सटीक quaternion|
|quath|GfQuath|अर्ध-सटीक quaternion|
|डबल2|जीएफवीईसी2डी|2 डबल्स का सदिश|
|float2|GfVec2f|2 फ़्लोट्स का सदिश|
|हाफ2|जीएफवीईसी2एच|2 हाफ का सदिश|
|int2|GfVec2i|2 ints का सदिश|
|डबल3|जीएफवीईसी3डी|3 डबल्स का सदिश|
|float3|GfVec3f|3 फ़्लोट्स का सदिश|
|हाफ3|जीएफवीईसी3एच|3 हाफ का सदिश|
|int3|GfVec3i|3 ints का सदिश|
|double4|GfVec4d|4 डबल्स का सदिश|
|float4|GfVec4f|4 फ्लोट का वेक्टर|
|हाफ4|जीएफवीईसी4एच|4 हाफ का सदिश|
|int4|GfVec4i|4 ints का सदिश|

## अमरीकी डालर उदाहरण

सादे ASCII फ़ाइल स्वरूप में USD फ़ाइल का एक उदाहरण इस प्रकार है।

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## संदर्भ ##

* [यूएसडी का परिचय](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [यूएसडी एपीआई संदर्भ](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

