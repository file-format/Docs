{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"कॉन्फ़िग - कॉन्फ़िगरेशन फ़ाइल",
  "description":"CONFIG उदाहरण और API के साथ CONFIG फ़ाइल स्वरूप के बारे में जानें जो CONFIG फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## कॉन्फ़िग फ़ाइल क्या है?
कॉन्फ़िग फ़ाइल को कॉन्फ़िगरेशन फ़ाइल के रूप में जाना जाता है; कई कंप्यूटर सॉफ्टवेयर के लिए पैरामीटर और प्राथमिक सेटिंग्स को कॉन्फ़िगर करने के लिए उपयोग किया जाता है। कुछ सॉफ्टवेयर अपने स्टार्टअप पर केवल अपनी **कॉन्फ़िगरेशन फ़ाइलें** पढ़ते हैं। अन्य समय-समय पर परिवर्तनों के लिए कॉन्फ़िगरेशन फ़ाइलों की जाँच करते हैं।

## कॉन्फिग फ़ाइल स्वरूप
**कॉन्फ़िग फ़ाइल स्वरूप** का उपयोग सर्वर प्रक्रियाओं, सॉफ़्टवेयर अनुप्रयोगों और ऑपरेटिंग सिस्टम सेटिंग्स के लिए किया जाता है। एक प्रोग्रामर एक निश्चित समय अवधि के बाद बार-बार कॉन्फ़िगरेशन फ़ाइलों को पढ़ने के लिए सॉफ़्टवेयर को निर्देश देने के लिए कोड लिख सकता है और वर्तमान प्रक्रिया में परिवर्तनों को लागू कर सकता है। CONFIG फ़ाइल सिंटैक्स के लिए कोई निश्चित मानक या मजबूत परंपराएँ नहीं हैं। उदाहरण के लिए, Microsoft की Web.config फ़ाइल CONFIG फ़ाइल प्रारूप से संबंधित है, जिसमें एक [XML](https://docs.fileformat.com/web/xml/) आधारित टैगसेट होते हैं; Microsoft Visual Studio या किसी अन्य पाठ संपादक के साथ संपादित किया जा सकता है।

## कॉन्फ़िगरेशन फ़ाइलों के उदाहरण:
चूंकि, कॉन्फ़िगरेशन फ़ाइलें किसी नियम, मानक या परिपाटी का पालन करके नहीं बनाई जाती हैं, इन फ़ाइलों को विभिन्न स्वरूपों का उपयोग करके लिखा जा सकता है। एक .config फ़ाइल XML, [JSON](https://docs.fileformat.com/web/json/) या किसी अन्य प्रारूप पर आधारित हो सकती है। जाने-माने ऑपरेटिंग सिस्टम और सॉफ्टवेयर के लिए कॉन्फ़िगरेशन फ़ाइलों के उदाहरण निम्नलिखित हैं:

### लिनक्स में कॉन्फ़िगरेशन फ़ाइलें
प्रत्येक लिनक्स प्रोग्राम एक निष्पादन योग्य फ़ाइल है जिसमें विशिष्ट संचालन को पूरा करने के लिए CPU द्वारा निष्पादित **opcodes** की सूची होती है। लगभग हर प्रोग्राम के संचालन को उसकी कॉन्फ़िगरेशन फ़ाइलों को बदलकर आपकी आवश्यकताओं के अनुसार अनुकूलित किया जा सकता है। लिनक्स सिस्टम में कई कॉन्फ़िगरेशन फ़ाइलें /etc निर्देशिका में हैं। कॉन्फ़िगरेशन फ़ाइलों को निम्न श्रेणियों में वर्गीकृत किया जा सकता है:
|श्रेणी|उदाहरण| टिप्पणियाँ|
---|---|---|
|फ़ाइलों तक पहुंचें|/etc/host.conf|नेटवर्क डोमेन सर्वर को बताता है कि होस्टनाम कैसे देखें||
|बूटिंग और लॉगिन/लॉगआउट|/etc/rc.d/rc.local|आधिकारिक नहीं। rc, rc.sysinit, या /etc/inittab.| से कॉल किया जा सकता है
|फ़ाइल सिस्टम|/etc/mtools.conf|एक डॉस-प्रकार फ़ाइल सिस्टम पर सभी संचालन (mkdir, कॉपी, प्रारूप, आदि) के लिए विन्यास।|
|सिस्टम एडमिनिस्ट्रेशन|/etc/shells|सिस्टम के लिए उपलब्ध संभावित "शेल्स" की सूची रखता है।|
|नेटवर्किंग|/etc/gated.conf|gate के लिए कॉन्फ़िगरेशन। केवल गेटेड डेमॉन द्वारा उपयोग किया जाता है||
|सिस्टम कमांड|/etc/logrotate.conf|डायनामिक लिंकर के लिए कॉन्फ़िगरेशन||
|डेमन्स|/etc/httpd.conf|अपाचे, वेब सर्वर के लिए विन्यास फाइल। यह फ़ाइल आमतौर पर /etc.| में नहीं है
|उपयोगकर्ता कार्यक्रम| /etc/lynx.cfg| प्रॉक्सी सेटिंग्स |
### एडब्ल्यूएस कॉन्फिग फ़ाइल उदाहरण
अक्सर उपयोग की जाने वाली कॉन्फ़िगरेशन सेटिंग्स और क्रेडेंशियल्स को CONFIG फ़ाइलों में सहेजा जा सकता है जिन्हें AWS CLI द्वारा बनाए रखा जाता है। CONFIG फ़ाइल एक सादा पाठ फ़ाइल होनी चाहिए जो निम्न स्वरूप का उपयोग करती है:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH कॉन्फ़िग फ़ाइल उदाहरण
OpenSSH क्लाइंट-साइड कॉन्फ़िगरेशन फ़ाइल का नाम CONFIG है, और इसे .ssh निर्देशिका में संग्रहीत किया जाता है। SSH CONFIG फ़ाइल में निम्न संरचना होती है:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### पायथन CONFIG फ़ाइल उदाहरण
एक पायथन CONFIG फ़ाइल इस तरह दिख सकती है:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## संदर्भ

* [लिनक्स कॉन्फ़िगरेशन फ़ाइलों को समझना](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [कॉन्फ़िगरेशन और क्रेडेंशियल फ़ाइल सेटिंग](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [पाइथन में कॉन्फ़िगरेशन फ़ाइलें] (https://martin-thoma.com/configuration-files-in-python/)

