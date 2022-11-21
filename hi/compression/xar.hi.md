{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - एक्स्टेंसिबल आर्काइव फ़ाइल स्वरूप",
  "description":"XAR फ़ाइल स्वरूप और API के बारे में जानें जो XAR फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## एक एक्सएआर फाइल क्या है?

.xar (एक्सटेंसिबल आर्काइव फॉर्मेट) एक्सटेंशन वाली फाइल एक यूनिक्स आर्काइव है जो कंप्रेस्ड या नॉन-कंप्रेस्ड फॉर्मेट में हो सकती है। इसका उपयोग मैक ओएस पर पैकेजों की स्थापना के लिए भी किया जाता है। XAR ओपन-सोर्स है और सफारी ब्राउजर के साथ उपयोग के लिए मैक ओएस एक्स 10.5 का हिस्सा रहा है।

## एक्सएआर फ़ाइल प्रारूप

एक [XAR](https://github.com/mackyle/xar/wiki/xarformat) फ़ाइल में तीन मुख्य क्षेत्र होते हैं।

* हैडर
* विषयसूची
* ढेर

### XAR हैडर

XAR हेडर को निम्नानुसार संरचित किया गया है।

|फ़ील्ड|डेटा प्रकार|बाइट्स में आकार|
---|---|---|
|मैजिक|अहस्ताक्षरित इंट 32|4|
|आकार|अहस्ताक्षरित इंट 16|2|
|संस्करण|अहस्ताक्षरित इंट 16|2|
|TOC लंबाई संपीड़ित|अहस्ताक्षरित Int 64|8|
|TOC लंबाई असंपीड़ित|अहस्ताक्षरित Int 64|8|
|चेकसम|अहस्ताक्षरित इंट 32|4|
|संदेश डाइजेस्ट नाम |नल टर्मिनेटेड||

एक्सएआर हेडर की सी संरचना को निम्नानुसार परिभाषित किया जा सकता है।
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
ध्यान दें कि हेडर के सभी क्षेत्र (जादू, आकार, संस्करण, toc_length_compressed, toc_length_uncompressed, cksum_alg) हमेशा XAR फ़ाइलों में नेटवर्क बाइट (उर्फ बिग एंडियन) क्रम में संग्रहीत होते हैं।

### एक्सएआर सामग्री तालिका (टीओसी)

सामग्री की तालिका एक XML दस्तावेज़ है जिसे (और अवश्य) UTF-8 के रूप में एन्कोड किया जाना चाहिए। इसे फ़ाइल की शुरुआत में संग्रहीत किया जाता है, जिससे व्यक्तिगत फ़ाइल को निकालने के लिए संग्रह के माध्यम से स्कैन करना आसान हो जाता है। XAR संग्रह आपको अलग-अलग संपीड़न योजनाओं जैसे [GZIP](/hi/compression/gz/), [BZIP2](/hi/compression/bz2), और अन्य समान का उपयोग करके स्वतंत्र रूप से संग्रह में अलग-अलग फ़ाइलों को संपीड़ित/एन्कोड करने देता है।

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### ढेर

संपीड़ित टोक के तुरंत बाद हीप शुरू हो जाता है। यह TOC द्वारा संदर्भित डेटा का एक असंरचित ढेर है। टीओसी में सूचीबद्ध ऑफसेट मान ढेर की शुरुआत से शुरू होते हैं। टीओसी में लंबाई मान हीप (संपीड़ित या नहीं) में संग्रहीत बाइट्स की वास्तविक संख्या को संदर्भित करता है जबकि आकार मान आइटम के निकाले गए आकार को संदर्भित करता है (यदि आवश्यक हो तो डीकंप्रेस करने के बाद)।

## संदर्भ

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [एक्सएआर - विकिपीडिया](https://en.wikipedia.org/wiki/Xar_(archiver))

