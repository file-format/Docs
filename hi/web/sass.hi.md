---
date: 2019-10-11
keywords: sass, .sass, sass फ़ाइल स्वरूप, sass फ़ाइलों को कैसे खोलें, वाक्यात्मक रूप से भयानक स्टाइलशीट, css प्रीप्रोसेसर, sass
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: सास फ़ाइल स्वरूप
linktitle: Sass
description: "Sass फ़ाइल स्वरूप और API के बारे में जानें जो Sass फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## एसएएसएस फाइल क्या है? ##

सैस (सिंटैक्टिकली विस्मयकारी स्टाइल शीट) एक प्रीप्रोसेसर स्क्रिप्टिंग भाषा है। इसे [CSS](/hi/web/css/) में संकलित किया गया है और इसे .sass एक्सटेंशन के साथ संग्रहीत किया गया है। Sass में दो सिंटैक्स होते हैं, मूल इंडेंटेशन पर आधारित होता है जो .sass एक्सटेंशन का उपयोग करता है और नया SCSS CSS जैसे ब्लॉक फॉर्मेटिंग के साथ होता है जो .scss एक्सटेंशन का उपयोग करता है।

## सास ## का उपयोग क्यों करें

सैस शैलियों को बनाए रखने में वास्तव में सहायक है क्योंकि यह कई सुविधाएँ प्रदान करता है जैसे चर, नेस्टिंग, मिश्रण, आयात और चयनकर्ता विरासत का परिचय देता है जो शैलियों के साथ काम करना मज़ेदार बनाता है।

## एसएएसएस फाइलों का उपयोग कैसे करें ##

एसएएसएस फाइलें सीधे [एचटीएमएल](/hi/वेब/एचटीएमएल/) दस्तावेज में शामिल नहीं होती हैं, बल्कि उन्हें सीएसएस फाइलों में बदल दिया जाता है जो एचटीएमएल फाइलों में शामिल होती हैं। [आधिकारिक Sass साइट](https://sass-lang.com/install) पर दिए गए निर्देशों का पालन करके आप अपने सिस्टम के Sass को स्थापित कर सकते हैं।

Sass को या तो पहले से सहेजी गई SASS फ़ाइल को परिवर्तित करके या परिवर्तनों को देखकर और फ़ाइल सहेजे जाने पर परिवर्तित करके CSS में परिवर्तित किया जा सकता है। दोनों के लिए कमांड नीचे दिए गए हैं।

### एक बार कन्वर्ट करें ###

कमांड का पहला पैरामीटर सोर्स एसएएसएस फाइल है और दूसरा पैरामीटर आउटपुट सीएसएस फाइल है।

```cmd
sass main.sass main.css
```

### परिवर्तन के लिए देखें ###

उपरोक्त कमांड को एक अतिरिक्त *वॉच* फ्लैग के साथ चलाया जा सकता है जो कमांड को चालू रखता है और जैसे ही Sass फ़ाइल सहेजी जाती है, आउटपुट CSS उत्पन्न होता है।

```cmd
sass --watch main.sass main.css
```

## सास सिंटेक्स ##

Sass वेरिएबल्स, नेस्टिंग, मिक्सिंस, इम्पोर्ट्स, सेलेक्टर इनहेरिटेंस आदि को सपोर्ट करता है। नीचे दिए गए इन फीचर्स के उदाहरण हैं।

### चर ###

चर का उपयोग पुन: प्रयोज्य जानकारी जैसे प्राथमिक रंग या बटन के लिए पैडिंग सेट करने के लिए किया जा सकता है। यह उपयोगी साबित हो सकता है यदि भविष्य में आपको उस जानकारी को बदलने की आवश्यकता हो, आप इसे केवल एक स्थान पर बदल दें और यह हर जगह अपडेट हो जाए।

** सास **

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**उत्पन्न सीएसएस**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### घोंसला बनाना ###

CSS चयनकर्ताओं को HTML के पदानुक्रम के समान नेस्टेड किया जा सकता है। निम्नलिखित उदाहरण में, स्पैन को h1 ब्लॉक के अंदर नेस्ट किया गया है।

** सास **

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**उत्पन्न सीएसएस**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### मिश्रण ###

मिक्सिन्स का उपयोग समान गुणों को एक साथ समूहित करने के लिए किया जाता है जो कई स्थानों पर उपयोग किए जाते हैं। मिक्सिन्स भी पैरामीटर का समर्थन करते हैं।

** सास **

**मिक्सिन घोषित करना**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**मिक्सिन का उपयोग करना**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**उत्पन्न सीएसएस**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### बढ़ाना ###

एक्सटेंड / इनहेरिटेंस उन मामलों में उपयोगी साबित हो सकता है जहां एक चयनकर्ता के गुणों को दूसरे चयनकर्ता के साथ साझा करने की आवश्यकता होती है। नीचे दिए गए उदाहरण में, *.error-notice* चयनकर्ता *.error-text* चयनकर्ता के सभी गुण लेता है और बॉर्डर और पैडिंग गुण जोड़ता है।

** सास **

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**उत्पन्न सीएसएस**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### आयात ###

आयात करना उपयोगी हो सकता है यदि आप कार्यक्षमता या किसी अन्य संरचना के आधार पर अपनी शैलियों को अलग-अलग फाइलों में संरचित करते हैं। आप इन सभी फ़ाइलों को एक प्राथमिक SASS फ़ाइल में आयात कर सकते हैं जिसे बाद में CSS में बदल दिया जाता है। आयात करते समय, आपको आयात निर्देश में फ़ाइल एक्सटेंशन निर्दिष्ट करने की आवश्यकता नहीं है। Sass सभी SASS फ़ाइलों को सीधे संकलित करता है। आयात फ़ाइलों को सीधे संकलित करने से बचने के लिए, आप उनके नाम के प्रारंभ में अंडरस्कोर (_) जोड़कर उन्हें आंशिक बना सकते हैं। आंशिक सामान्य सास फ़ाइलों के समान आयात किए जाते हैं।

** सास **

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

आउटपुट CSS में सभी आयातित फ़ाइलों की शैलियाँ होंगी।

## संदर्भ ##

- [सास - विकिपीडिया] (https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [सास](https://sass-lang.com/)

