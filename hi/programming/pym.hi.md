---
date: 2022-05-09
लेखक:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM फ़ाइल स्वरूप - PYM मैक्रो प्रीप्रोसेसर फ़ाइल
linktitle: PYM
description: "PYM फ़ाइल स्वरूप और API के बारे में जानें जो PYM फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## पीवाईएम फाइल क्या है?

PYM फ़ाइल एक मैक्रो प्रीप्रोसेसर फ़ाइल है जो Python प्रोग्रामिंग भाषा पर आधारित है। इसे वीआरविस रिसर्च और स्टोर मैक्रो शॉर्टकट्स द्वारा विकसित किया गया था। जब PYM फ़ाइल की व्याख्या Python दुभाषिया के प्रीप्रोसेसिंग चरण द्वारा की जाती है, तो इन शॉर्टकट्स को उनके पूर्ण पाठ के प्रतिस्थापन के रूप में विस्तारित किया जाता है। इसके अलावा, एक तीसरा, वैकल्पिक ऑपरेशन जो एक मैक्रो प्रीप्रोसेसर द्वारा किया जा सकता है, फ़ाइल समावेशन है। PYM फाइलें पाठ संपादकों जैसे Notepad, Notepad++, Apple TextEdit, और Linux पर VI में खोली जा सकती हैं।

## पीवाईएम फ़ाइल प्रारूप

PYM फाइलें डिस्क में सादे पाठ फ़ाइलों के रूप में सहेजी जाती हैं। एक PYM फ़ाइल में `#include` निर्देश का उपयोग करके अन्य फ़ाइलें भी शामिल हो सकती हैं।

### पीवाईएम सिंटैक्स

PYM स्टेटमेंट "" #begin python और "#end python" मार्करों के बीच शामिल हैं जैसा कि नीचे दिखाया गया है।

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM मैक्रो विस्तार

PYM मैक्रो विस्तार को दो अनुक्रमों अर्थात <[ और ]> द्वारा दर्शाया गया है। ये विशेष html टैग हैं और एक पंक्ति में कहीं भी दिखाई दे सकते हैं। एक छोटा PYM उदाहरण इस प्रकार है।

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

PYM के माध्यम से इसे चलाने का आउटपुट इस प्रकार है:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## संदर्भ ##

* [पीवाईएम - पायथन पर आधारित मैक्रो प्रीप्रोसेसर](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM दुभाषिए](https://github.com/interpreters/pym)

