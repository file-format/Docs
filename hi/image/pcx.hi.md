{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"पीसीएक्स फाइल फॉर्मेट - पेंटब्रश बिटमैप इमेज फाइल",
  "description":"PCX फ़ाइल स्वरूप और API के बारे में जानें जो PCX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## पीसीएक्स फाइल क्या है?

एक पीसीएक्स फाइल, पिक्चर एक्सचेंज फाइल, एक रेखापुंज छवि फ़ाइल प्रारूप है जिसे पीसी पेंटब्रश एप्लिकेशन के लिए मूल फ़ाइल प्रारूप के रूप में इस्तेमाल किया गया था। इसे ZSoft Corporation, USA द्वारा DOS और Windows प्लेटफॉर्म के लिए विकसित किया गया था [BMP](/hi/image/bmp/), [JPEG](/hi/image/jpeg/), और [PNG](/hi/image/png/) फ़ाइल प्रारूप। PCX फाइलें आकार में छोटी होती हैं क्योंकि वे RLE एन्कोडिंग का उपयोग करके संपीड़ित होती हैं। इसका उपयोग बहु-पृष्ठ [DCX](/hi/image/dcx/) फ़ाइल में किया जाता है जिसका मुख्य रूप से डिजिटल फ़ैक्स फ़ाइलें बनाने के लिए उपयोग किया जाता है।

## पीसीएक्स फ़ाइल प्रारूप

PCX फाइलें बाइनरी फाइल फॉर्मेट में डिस्क में सेव की जाती हैं। आंतरिक फ़ाइल प्रारूप संरचना थोड़ा एंडियन बाइट ऑर्डरिंग का अनुसरण करती है और इसमें निम्नलिखित तीन खंड होते हैं:

**`पीसीएक्स हैडर`** - एक पीसीएक्स हैडर 128 बाइट लंबा होता है। इसमें एक पहचानकर्ता, एक संस्करण संख्या, छवि आयाम, 16 पैलेट रंग, संख्या रंग विमान और प्रत्येक विमान की बिट गहराई, और संपीड़न विधि के लिए एक मूल्य शामिल है।

PCX हैडर जैसा कि ग्राफिक्स फ़ाइल स्वरूपों के विश्वकोश (द्वितीय संस्करण) के संदर्भ में नीचे दिखाया गया है।
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`इमेज डेटा`** - पीसीएक्स इमेज डेटा हेडर के ठीक बाद आता है। हेडर में फील्ड सेटिंग के आधार पर इमेज डेटा को कंप्रेस किया जा सकता है। पीसीएक्स फ़ाइल में डेटा का भंडारण निर्दिष्ट रंग के विमानों की संख्या पर निर्भर करता है। छवि डेटा पंक्तियों में व्यवस्थित है। कई विमानों के मामले में, इन्हें लाल, हरे और नीले डेटा की अनुक्रमिक व्यवस्था में पंक्ति के भीतर विमान द्वारा संग्रहित किया जाता है। यह पैटर्न विमान में प्रत्येक पंक्ति के लिए दोहराया जाता है।

## संदर्भ

* [पीसीएक्स - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/PCX)

