{
  "date" : "2019-10-11",
  "keywords" :[ "एमपीकेजी फाइल", "एमपीकेजी फाइल फॉर्मेट", "एमपीकेजी फाइल क्या है", "फाइल", "एमपीकेजी उदाहरण", "एमपीकेजी फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एमपीकेजी फ़ाइल प्रारूप - मेटा पैकेज फ़ाइल",
  "description":"एमपीकेजी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एमपीकेजी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## एमपीकेजी फाइल क्या है?

.mpkg एक्सटेंशन वाली फाइल एक आर्काइव इंस्टॉलर फाइल होती है, जो ज्यादातर MacOS ऑपरेटिंग सिस्टम पर पाई जाती है। इसमें संबंधित फाइलों को अलग से रखने की आवश्यकता के बिना एप्लिकेशन की सभी आवश्यक इंस्टॉलेशन फाइलें शामिल हैं। एक एकल MPKG फ़ाइल में पैकेज फ़ाइलें [PKG](/hi/compression/pkg/) हो सकती हैं, जो अन्य फ़ाइलों के अलावा एक इंस्टॉलेशन फ़ाइल के रूप में हो सकती हैं। MPKG फ़ाइलें किसी भी सामान्य सॉफ़्टवेयर के साथ नहीं खोली जा सकतीं और Apple इंस्टालर का उपयोग करके MacOS पर स्वचालित रूप से निष्पादित की जाती हैं।

## एमपीकेजी फ़ाइल प्रारूप

एक एमपीकेजी फ़ाइल में विभिन्न प्रकार की फाइलें होती हैं जो इसमें शामिल कई पैकेजों की स्थापना के लिए आवश्यक होती हैं। इसे नीचे दी गई छवि से देखा जा सकता है जो एक नमूना MPKG फ़ाइल की ट्री संरचना है। यह ट्री संरचना MacOS टर्मिनल पर `tree` कमांड का उपयोग करके निर्यात की जाती है।

{{< figure src="../mpkg.png" alt="एमपीकेजी फ़ाइल प्रारूप" >}}

छवि में विभिन्न तत्वों का विवरण इस प्रकार है।

`पैकेज निर्देशिका` - पीकेजी फाइलों की एक सूची संग्रहीत करता है, यानी उप-पैकेज की एक सूची
`संसाधन निर्देशिका` - पीकेजी द्वारा उपयोग किए जाने वाले संसाधनों को संग्रहीत करता है, जैसे स्थानीय संसाधन और छवियां, आरटीएफ दस्तावेज, पीडीएफ दस्तावेज इत्यादि।
`Distribution.dist file` - एक xml दस्तावेज़ जिसमें स्थापित किए जाने वाले उप-पैकेज और रनटाइम स्क्रिप्ट जैसी जानकारी होती है

MPKG फ़ाइल के लिए नमूना XML फ़ाइल संबंधित उप-पैकेजों के आधार पर अनुसरण के रूप में दिख सकती है।

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/hi/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - स्थापित किया जाने वाला उप-पैकेज है। यह pkg प्रारूप में बंडल संरचना की एक निर्देशिका है। इसमें एक सामग्री उपनिर्देशिका है।

## संदर्भ

* [OSX फ्लैट पैकेज](https://matthew-brett.github.io/docosx/flat_packages.html)
* [सी++ एमपीकेजी पैकेज मैनेजर](https://github.com/puellavulnerata/mpkg)

