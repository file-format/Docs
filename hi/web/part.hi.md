{
  "date" : "2021-06-24",
  "keywords" :["भाग", "आंशिक", "विस्तार", "फ़ाइल", "प्रारूप", "वेब", "डाउनलोड किया गया"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"भाग - आंशिक रूप से डाउनलोड की गई फ़ाइल",
  "description":"PART फ़ाइल स्वरूप और API के बारे में जानें जो PART फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## पार्ट फ़ाइल क्या है? ##

आंशिक फ़ाइल या .part एक्सटेंशन आंशिक रूप से डाउनलोड की गई फ़ाइल होती है। इसका उपयोग तब किया जाता है जब डाउनलोड चल रहा हो या किसी समस्या के कारण बाधित हो गया हो, जिससे डाउनलोड प्रबंधक को जब भी संभव हो डाउनलोड को फिर से शुरू करने का अवसर मिलता है।
इसका मतलब यह है कि ब्राउज़र, जैसे कि फ़ायरफ़ॉक्स या फाइल ट्रांसफर प्रोग्राम जैसे eMule, eMule plus, FlashGet, आदि फ़ाइल के एक हिस्से को स्टोर करता है, जिसे पार्ट फ़ाइल कहा जाता है, जबकि डाउनलोडिंग आपके डिवाइस पर हो रही है। यह भाग फ़ाइल आपको दिखाएगी कि क्या डाउनलोड प्रगति पर है या पूरा होने से पहले बाधित हो गया है। इतना ही नहीं, बल्कि PART फाइल डाउनलोड पूरा होने तक सभी डेटा को स्टोर करती है, यही कारण है कि यदि आप डाउनलोड को फिर से शुरू करना चाहते हैं तो उनमें से कुछ को बाद में फिर से शुरू किया जा सकता है।

## भाग फ़ाइल स्वरूप ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
