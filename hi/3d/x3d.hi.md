{
  "date" : "2019-10-11",
  "keywords" :[ "x3d फ़ाइल", "x3d फ़ाइल स्वरूप", "x3d फ़ाइल क्या है", "फ़ाइल", "x3d उदाहरण", "x3d फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D छवि फ़ाइल",
  "description":"X3D फ़ाइल स्वरूप और API के बारे में जानें जो X3D फ़ाइलें खोल और बना सकते हैं।",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## X3D फ़ाइल क्या है?
X3D 3D जानकारी की प्रस्तुति के लिए एक [XML](/hi/web/xml/) आधारित 3D ग्राफ़िक्स फ़ाइल स्वरूप है। यह एक मॉड्यूलर मानक है और इसे कई आईएसओ विनिर्देशों के माध्यम से परिभाषित किया गया है। प्रारूप वेक्टर और रेखापुंज ग्राफिक्स, पारदर्शिता, प्रकाश प्रभाव और एनीमेशन सेटिंग्स का समर्थन करता है जिसमें घुमाव, फीका और स्विंग शामिल हैं। यह 2001 में [VRML](/hi/3d/vrml/) फ़ाइल स्वरूप का उत्तराधिकारी बन गया। X3D में रंग जानकारी को एन्कोड करने का लाभ है ([STL](/hi/cad/stl/) के विपरीत) जिसका उपयोग मॉडल को रंग पर प्रिंट करने के दौरान किया जाता है। थ्री डी प्रिण्टर। प्रारूप में VRML के एक्सटेंशन हैं, जो XML सिंटैक्स के साथ-साथ VRML97 या बाइनरी फॉर्मेटिंग के ओपन इन्वेंटर-जैसे सिंटैक्स का उपयोग करके दृश्य को एन्कोड करने की क्षमता प्रदान करते हैं।

X3D (ISO/IEC 19775) के लिए सार विनिर्देश को पहली बार 2004 में ISO द्वारा अनुमोदित किया गया था। X3D (ISO/IEC 19776) के लिए XML और ClassicVRML एन्कोडिंग को पहली बार 2005 में अनुमोदित किया गया था।

## X3D फ़ाइल स्वरूप

X3D दृश्य फ़ाइलों में एक सामान्य फ़ाइल संरचना होती है:

* फ़ाइल हैडर (या तो XML, ClassicVRML, या संपीडित बाइनरी)
* संस्करण और प्रोफ़ाइल विशेषताओं सहित X3D रूट नोड की शुरुआत
* कंपोनेंट और मेटा स्टेटमेंट के साथ एक हेड सेक्शन (दोनों वैकल्पिक)
* X3D दृश्य ग्राफ और उसके बच्चे नोड्स
* X3D रूट नोड का अंत

## X3D फ़ाइल स्वरूप उदाहरण

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## संदर्भ ##

* [X3D - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/X3D)
* [वेब3डी कंसोर्टियम की आधिकारिक वेबसाइट](http://www.web3d.org/)
* [X3D आधिकारिक वेबसाइट] (http://www.web3d.org/x3d/what-x3d)

