{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आईडीएक्स - उच्च दक्षता वीडियो कोडेक",
  "description":"IDX फ़ाइल स्वरूप और API के बारे में जानें जो IDX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## आईडीएक्स फाइल क्या है?

एक आईडीएक्स फ़ाइल एक उपशीर्षक अनुक्रमणिका फ़ाइल है जो एक .sub (VobSub उपशीर्षक) फ़ाइल के अंदर उपशीर्षक के लिए मेटाडेटा जानकारी की सूची को इंगित करती है। यह वोबसब सॉफ़्टवेयर एप्लिकेशन द्वारा बनाया और उपयोग किया जाता है जो उपयोगकर्ताओं को डीवीडी से उपशीर्षक निकालने और एक एसयूबी फ़ाइल में डंप करने देता है। आईडीएक्स फाइलों में टाइमस्टैम्प और बाइट ऑफ़सेट होते हैं जो प्रत्येक उपशीर्षक को इंगित करने के लिए उपयोग किए जाते हैं। VobSub हमेशा संबंधित SUB फ़ाइल के साथ एक IDX फ़ाइल बनाता है।

## IDX फ़ाइल स्वरूप - अधिक जानकारी

IDX फाइलें उत्पन्न होती हैं और सादे पाठ फ़ाइलों के रूप में सहेजी जाती हैं जिन्हें किसी भी पाठ संपादक में खोला जा सकता है। एक आईडीएक्स फ़ाइल में ऐसी जानकारी होती है जिसे मीडिया प्लेयर द्वारा स्क्रीन पर प्रदर्शित करने के लिए उपशीर्षक पाठ का रंग, स्क्रीन पर उपशीर्षक पाठ की स्थिति जैसे मापदंडों को पढ़ने के लिए पढ़ा जाता है।

### आईडीएक्स उपशीर्षक सेटिंग्स

एक विशिष्ट IDX फ़ाइल इस मेटाडेटा जानकारी को फ़ाइल के प्रारंभ में संग्रहीत करती है। उपशीर्षक सेटिंग्स **#** से शुरू होती हैं। टाइमस्टैम्प और छवि संदर्भ इन सभी उपशीर्षक सेटिंग्स के बाद जोड़े जाते हैं और **टाइमस्टैम्प:** से शुरू होते हैं।

## IDX फ़ाइल स्वरूप उदाहरण

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## आईडीएक्स फ़ाइल का उपयोग कैसे करें?

यदि आपके पास मूवी के लिए उप और आईडीएक्स फ़ाइलें हैं, तो आप इन उपशीर्षकों को मूवी के साथ वापस चला सकते हैं जिसके लिए ये बनाए गए हैं। कई एप्लिकेशन जैसे वीएलसी, जीओएम प्लेयर, पॉटप्लेयर, या पावरडीवीडी में इन एसयूबी और आईडीएक्स फाइलों को लोड करने और मूवी के साथ चलाने की क्षमता है। सॉफ्टवेयर एप्लिकेशन SUB और IDX उपशीर्षक फ़ाइलों को [.mkv](/hi/video/mkv/) फ़ाइलों में भी एम्बेड कर सकते हैं।

## आईडीएक्स को एसआरटी में बदलें

[SRT](/hi/video/srt/) (SubRip फ़ाइल स्वरूप) SubRip फ़ाइल स्वरूप में सहेजी गई एक साधारण उपशीर्षक फ़ाइल है। यह आमतौर पर VobSub फ़ाइल स्वरूप की तुलना में अधिक उपयोग किया जाता है। इस प्रकार, यदि आप SUB/IDX फ़ाइलों को SRT फ़ाइल स्वरूप में कनवर्ट करना चाहते हैं, तो तृतीय पक्ष उपकरण उपलब्ध हैं जिनका उपयोग इसे प्राप्त करने के लिए किया जा सकता है। Sub/IDX to SRT कन्वर्टर, SubtitleTools.com पर उपलब्ध एक ऐसा टूल है जो SUB और IDX फ़ाइलों को इनपुट के रूप में लेता है और इन VobSub उपशीर्षकों को SRT फ़ाइलों में परिवर्तित करता है।

## संदर्भ

* [वोबसब](https://www.videohelp.com/software/VobSub)
* [वीओबीसब - विकी मल्टीमीडिया](https://wiki.multimedia.cx/index.php?title=VOBsub)

