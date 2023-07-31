{
  "date" : "2019-10-11",
  "keywords" :["वीसीएक्सप्रोज", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "विजुअल सी++ प्रोजेक्ट", "प्रोग्रामिंग गाइड"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"वीसीएक्सप्रोज",
  "description":"VCXPROJ फ़ाइल स्वरूप और API के बारे में जानें जो VCXPROJ फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## VCXPROJ फ़ाइल क्या है?

.vcxproj एक्सटेंशन वाली फ़ाइल एक Microsoft Visual C++ प्रोजेक्ट फ़ाइल है जो [C++](/hi/programming/cpp/) प्रोजेक्ट जानकारी संग्रहीत करती है। इसमें ऐसी जानकारी शामिल है जिसका उपयोग MSBuild प्रोजेक्ट सिस्टम द्वारा अंतिम आउटपुट को संकलित करने और बनाने के लिए किया जाता है। विज़ुअल C++ प्रोजेक्ट्स का VCXPROJ .NET प्रोजेक्ट्स के लिए [CSPROJ](/hi/ प्रोग्रामिंग/csproj/) के समान है। VCXPROJ फाइलों में कोई कोड नहीं होता है, लेकिन परियोजना के निर्माण के लिए परियोजना के लिए परिभाषित सभी वर्गों, लक्ष्यों और गुणों को संदर्भित करता है। इन्हें सादे पाठ संपादकों में या अधिमानतः Microsoft Visual Studio IDE में खोला जा सकता है।


## VCXPROJ फ़ाइल स्वरूप - अधिक जानकारी

VCXPROJ फ़ाइलें टेक्स्ट फ़ाइलें हैं जो [XML](/hi/web/xml/) फ़ाइल स्वरूप में बनाई गई हैं। इन्हें किसी भी टेक्स्ट एडिटर में खोला जा सकता है लेकिन इन फ़ाइलों को खोलने और संपादित करने के लिए Microsoft Visual Studio IDE का उपयोग करने की अत्यधिक अनुशंसा की जाती है। इन्हें मैन्युअल संपादन के लिए डिज़ाइन नहीं किया गया था। गलतियाँ आईडीई को क्रैश या अप्रत्याशित तरीके से व्यवहार करने का कारण बन सकती हैं।

एक नमूना VCXPROJ फ़ाइल की सामग्री इस प्रकार है।

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ फ़ाइल तत्व

एक विशिष्ट VCXPROJ फ़ाइल में कई तत्व होते हैं जैसा कि उपरोक्त XML उदाहरण में देखा जा सकता है। [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) Microsoft द्वारा प्रत्येक फ़ाइल तत्व को विस्तार से समझाया गया है और इसे संदर्भित किया जा सकता है डेवलपर के नजरिए से।

#### परियोजना तत्व

यह VCXPROJ फाइल का रूट नोड है। MSBuild संकलन के लिए बिल्ड संस्करण और डिफ़ॉल्ट लक्ष्य को पढ़ने के लिए इस तत्व का उपयोग करता है।

#### प्रोजेक्ट कॉन्फ़िगरेशन आइटम समूह तत्व

इसमें प्रोजेक्ट कॉन्फ़िगरेशन जानकारी शामिल है जिसमें बिल्ड विधि (डीबग या रिलीज), 32 या 64-बिट संकलन, अनुकूलन विकल्प और अन्य शामिल हो सकते हैं। इस समूह की जानकारी का उपयोग आईडीई द्वारा परियोजना को लोड करने के लिए किया जाता है।

#### परियोजना विन्यास तत्व

VCXPROJ फ़ाइल में ProjectConfiguration तत्वों में बिल्ड और प्लेटफ़ॉर्म के बारे में जानकारी होती है जिसके लिए प्रोजेक्ट लोड किया जाता है। इसका नाम `$(कॉन्फ़िगरेशन)|$(प्लेटफ़ॉर्म)` के फ़ॉर्मैट में होना चाहिए।

#### वैश्विक संपत्ति समूह तत्व

इस खंड में ऐसी सेटिंग्स हैं जो परियोजना स्तर के लिए जानकारी प्रदान करती हैं जैसे:

* प्रोजेक्टगाइड
* रूट नेमस्पेस
* एप्लिकेशन प्रकार या एप्लिकेशन प्रकार संशोधन


## संदर्भ

* [VCXPROJ संरचना - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [सी++ प्रोजेक्ट फ़ाइलें](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

