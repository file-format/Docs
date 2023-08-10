{
  "date" : "2019-10-11",
  "keywords" :["डीएई फाइल", "डीएई फाइल फॉर्मेट", "डीएई फाइल क्या है", "फाइल", "डीएई उदाहरण", "डीएई फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"डीएई फ़ाइल प्रारूप और एपीआई के बारे में जानें जो डीएई फाइलें खोल और बना सकते हैं।",
  "title" :"पऊवि - डिजिटल एसेट एक्सचेंज फ़ाइल स्वरूप",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## डीएई फाइल क्या है?

DAE फ़ाइल एक डिजिटल एसेट एक्सचेंज फ़ाइल स्वरूप है जिसका उपयोग इंटरैक्टिव 3D अनुप्रयोगों के बीच डेटा के आदान-प्रदान के लिए किया जाता है। यह फ़ाइल प्रारूप कोलाडा (सहयोगात्मक डिजाइन गतिविधि) एक्सएमएल स्कीमा पर आधारित है जो ग्राफिक्स सॉफ्टवेयर अनुप्रयोगों के बीच डिजिटल संपत्तियों के आदान-प्रदान के लिए एक खुला मानक एक्सएमएल स्कीमा है। इसे ISO द्वारा सार्वजनिक रूप से उपलब्ध विनिर्देश, ISO/pAS 17506 के रूप में अपनाया गया है। DAE फाइलें Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, और API जैसे [Aspose.CAD](https://products.aspose.com/cad/) जैसे अनुप्रयोगों में खोली जा सकती हैं।

## डीएई फ़ाइल प्रारूप

डीएई फ़ाइल प्रारूप [कोलाडा एक्सएमएल स्कीमा](https://www.khronos.org/files/collada_spec_1_5.pdf) पर आधारित है जहां सभी तत्वों को एक्सएमएल टैग के रूप में परिभाषित किया गया है। यह विविध DCC और 3D प्रोसेसिंग टूल को 3D परिसंपत्तियों के लिए उत्पादन पाइपलाइन में बाँधने में सक्षम बनाता है। इसमें ज्योमेट्री, एनिमेशन, शेडर्स और फिजिक्स सहित विजुअल सीन की व्यापक एन्कोडिंग है। प्रारूप खुला है, संग्रह-ग्रेड है और मेटा जानकारी को बरकरार रखता है।

### कोलाडा टैग

कोलाडा स्कीमा टैग नीचे दिखाया गया है।
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### संपत्ति टैग

एसेट टैग फ़ाइल के लेखक और परिवेश का वर्णन करता है

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### कैमरा लाइब्रेरी

कोलाडा संपत्ति पुस्तकालयों के अंदर निहित है। कैमरा लाइब्रेरी में आश्चर्यजनक रूप से कैमरे हैं। सामान्य कैमरे परिप्रेक्ष्य या ऑर्थोग्राफ़िक हैं। कैमरा लाइब्रेरी टैग को निम्नानुसार परिभाषित किया गया है।
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### रोशनी

आम रोशनी बिंदु, स्थान या दिशात्मक हैं
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### सामग्री उदाहरण

सामग्री उदाहरण प्रभाव निम्नानुसार परिभाषित किए गए हैं।
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### आम प्रभाव

सामान्य प्रभाव ओपनजीएल 1 राज्य की तरह कार्य करते हैं और इसे निम्नानुसार परिभाषित किया जा सकता है।

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### ज्यामिति गुण

ज्यामिति ओपनजीएल विशेषताओं का वर्णन करती है और निम्नानुसार परिभाषित की जाती है।
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### दृश्य दृश्य

दृश्य दृश्य एकता दृश्यों की तरह होते हैं और इसमें नोड्स का पदानुक्रम निम्नानुसार होता है।
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## संदर्भ
* [कोलाडा 1.5.0 विनिर्देश](https://www.khronos.org/files/collada_spec_1_5.pdf)

