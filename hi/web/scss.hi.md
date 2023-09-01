---
date: 2019-10-11
keywords: scss, .scss, scss फ़ाइल स्वरूप, scss फ़ाइलें कैसे खोलें, वाक्यात्मक रूप से भयानक स्टाइलशीट, css प्रीप्रोसेसर, sass
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS फ़ाइल स्वरूप - Sass कैस्केडिंग स्टाइल शीट
linktitle: SCSS
description: "SCSS फ़ाइल स्वरूप और API के बारे में जानें जो SCSS फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## एससीएसएस फ़ाइल क्या है? ##

एससीएसएस सैस (सिंटैक्टिकली विस्मयकारी स्टाइलशीट) का दूसरा सिंटैक्स है जो इंडेंटेशन के बजाय ब्रैकेट का उपयोग करता है। SCSS को इस तरह से डिज़ाइन किया गया था कि एक मान्य CSS3 फ़ाइल भी एक मान्य SCSS फ़ाइल है। SCSS फाइलें .scss एक्सटेंशन के साथ स्टोर की जाती हैं।

## एससीएसएस ## का उपयोग क्यों करें

चूंकि वेबसाइटों के डिजाइन जटिल होते जा रहे हैं जिसके परिणामस्वरूप बड़ी [css](/hi/web/css/) फाइलें बन रही हैं। ऐसी फाइलों को बनाए रखना कठिन होता है। यह वह जगह है जहाँ SCSS आता है। SCSS CSS विकास में चर, नेस्टिंग, मिश्रण, आयात और चयनकर्ता विरासत का परिचय देता है। ये जोड़ डिजाइन के साथ काम करना और अधिक मजेदार बनाते हैं।

## एससीएसएस फाइलों का उपयोग कैसे करें ##

एससीएसएस फाइलें सीधे [html](/hi/web/html/) दस्तावेज में सीएसएस की तरह शामिल नहीं हैं। इसके बजाय, SCSS फाइलें CSS फाइलों में बदल जाती हैं जो HTML फाइलों में शामिल होती हैं। अपने सिस्टम पर एससीएसएस स्थापित करने के लिए, [आधिकारिक सैस साइट](https://sass-lang.com/install) पर दिए गए निर्देशों का पालन करें।
एससीएसएस को सीएसएस में बदलने के लिए, आप या तो पहले से सहेजी गई एससीएसएस फ़ाइल को परिवर्तित कर सकते हैं या परिवर्तन के लिए देख सकते हैं और फ़ाइल को सहेजे जाने के रूप में परिवर्तित कर सकते हैं। दोनों के लिए कमांड नीचे दिए गए हैं।

### एक बार कन्वर्ट करें ###

पहला पैरामीटर स्रोत SCSS फ़ाइल है और दूसरा पैरामीटर आउटपुट CSS फ़ाइल है।

```cmd
sass main.scss main.css
```

### परिवर्तन के लिए देखें ###

कमांड में एक अतिरिक्त *वॉच** फ़्लैग होता है जो कमांड को चालू रखता है और जैसे ही SCSS फ़ाइल सहेजी जाती है, आउटपुट CSS उत्पन्न होता है।

```cmd
sass --watch main.scss main.css
```

## एससीएसएस सिंटेक्स ##

SCSS वेरिएबल्स, नेस्टिंग, मिक्सिंस, इम्पोर्ट्स, सेलेक्टर इनहेरिटेंस आदि को सपोर्ट करता है। इन विशेषताओं के उदाहरण नीचे दिए गए हैं।

### चर ###

वेरिएबल्स के उपयोग से, आप सेव बटन के लिए प्राथमिक रंग या पृष्ठभूमि रंग जैसी पुन: प्रयोज्य जानकारी सेट कर सकते हैं। यह उपयोगी है यदि आपको उस जानकारी को बदलने की आवश्यकता है, तो आप इसे केवल एक स्थान पर बदलते हैं और जहां भी इसका उपयोग किया जाता है, यह अपडेट हो जाता है।

**एससीएसएस**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

आप HTML के पदानुक्रम के समान CSS चयनकर्ताओं को नेस्ट कर सकते हैं। नीचे दिए गए उदाहरण में, स्पैन को h1 ब्लॉक के अंदर नेस्ट किया गया है।

**एससीएसएस**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

मिक्सिन्स का उपयोग समान गुणों को एक साथ समूहित करने के लिए किया जा सकता है जो एक साथ कई स्थानों पर उपयोग किए जाते हैं। आप मिक्सिक्स को पैरामीटर भी पास कर सकते हैं।

**एससीएसएस**

**मिक्सिन घोषित करना**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**मिक्सिन का उपयोग करना**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

एक्सटेंड / इनहेरिटेंस उन मामलों में उपयोगी है जहां एक चयनकर्ता के गुणों को दूसरे चयनकर्ता के साथ साझा करने की आवश्यकता होती है। नीचे दिए गए उदाहरण में, *.error-notice* चयनकर्ता *.error-text* चयनकर्ता के सभी गुण लेता है और बॉर्डर और पैडिंग गुण जोड़ता है।

**एससीएसएस**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

चिंताओं को अलग करने में आयात उपयोगी हो सकता है। आप शैलियों को इस प्रकार विभाजित कर सकते हैं कि शीर्ष लेख शैलियाँ एक अलग फ़ाइल में हों, पादलेख शैलियाँ एक अलग फ़ाइल में हों, शैलियों में उपयोग किए जाने वाले सभी रंग चर एक अलग फ़ाइल में हो सकते हैं, आदि। इस तकनीक का उपयोग करके, शैलियाँ व्यवस्थित रहती हैं। आप केवल अपनी मुख्य SCSS फ़ाइल में फ़ाइलें आयात करें जैसा कि नीचे दिए गए उदाहरण में दिखाया गया है। आपको आयात निर्देश में फ़ाइल एक्सटेंशन निर्दिष्ट करने की आवश्यकता नहीं है। Sass सभी SCSS फ़ाइलों को सीधे संकलित करता है। आयात फ़ाइलों को सीधे संकलित करने से बचने के लिए, आप उनके नाम से पहले अंडरस्कोर (_) जोड़कर उन्हें आंशिक बना सकते हैं। आप अंडरस्कोर के बिना सामान्य एससीएसएस फाइलों के समान आंशिक आयात कर सकते हैं।

**एससीएसएस**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

आउटपुट CSS में सभी आयातित फ़ाइलों की शैलियाँ होंगी।

## संदर्भ ##

- [एससीएसएस - विकिपीडिया](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [सास](https://sass-lang.com/)

