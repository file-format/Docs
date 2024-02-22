{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "एमपीके फ़ाइल - आर्कजीआईएस मैप पैकेज फ़ाइल प्रारूप",
  "description":"एमपीके फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एमपीके फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-hi",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## एमपीके फ़ाइल क्या है?

एमपीके फ़ाइल एक आर्कजीआईएस मैप पैकेज फ़ाइल है जो आर्कजीआईएस के साथ बनाई गई है। इसमें एक .mxd मानचित्र दस्तावेज़ और संबंधित डेटा शामिल है। इसके अलावा, इसमें अतिरिक्त जानकारी जैसे संदर्भित परतें, प्रतीक और अन्य संसाधन शामिल हैं। एमपीके फ़ाइल का उपयोग अन्य उपयोगकर्ताओं के साथ मानचित्र और डेटा साझा करने के लिए किया जाता है। यह मूल डेटा स्रोत वाले अन्य लोगों की उपलब्धता को समाप्त कर देता है और मोबाइल डिवाइस पर उपयोग किए जाने वाले मानचित्रों को वितरित करने में भी मदद करता है।

## एमपीएक्स फ़ाइल स्वरूप

एमपीएक्स फ़ाइलों का आंतरिक फ़ाइल प्रारूप विवरण डेवलपर के संदर्भ के लिए सार्वजनिक रूप से उपलब्ध नहीं है।

### आर्कजीआईएस का उपयोग करके एमपीके फ़ाइल बनाएं

एमपीके फ़ाइलें आर्कजीआईएस का उपयोग करके बनाई जा सकती हैं। मैप पैकेज मेनू में इस रूप में साझा करें विकल्प का उपयोग एक .mpk फ़ाइल बनाने के लिए किया जा सकता है जिसमें मानचित्र दस्तावेज़ और उसके सभी संदर्भित डेटा और संसाधन शामिल हैं। इस एमपीके फ़ाइल को फिर दूसरों के साथ साझा किया जा सकता है और मानचित्र और डेटा देखने के लिए आर्कमैप और आर्कजीआईएस प्रो में खोला जा सकता है।

### पायथन का उपयोग करके एमपीके फ़ाइल बनाएं

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### एक फ़ोल्डर में सभी मानचित्र दस्तावेज़ों के लिए मानचित्र पैकेज बनाने के लिए पायथन का उपयोग करना

निम्नलिखित पायथन कोड एक निर्दिष्ट फ़ोल्डर में मौजूद सभी मानचित्र दस्तावेज़ों के लिए मानचित्र पैकेज ढूंढता है और बनाता है।

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## संदर्भ

* [पैकेज मैप](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


