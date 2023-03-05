{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एचएस - हास्केल स्क्रिप्ट फ़ाइल स्वरूप",
  "description":"एचएस फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एचएस फाइलें बना और खोल सकते हैं।",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# एचएस - जावा हेल्पसेट फाइल फॉर्मेट

## जावा एचएस फाइल क्या है?

जावा प्रोग्रामिंग लैंग्वेज में .hs एक्सटेंशन वाली फाइल एक हेल्प डॉक्यूमेंटेशन फाइल होती है, जिसका उपयोग JavaHelp सिस्टम द्वारा किया जाता है, जब यह किसी एप्लिकेशन द्वारा सक्रिय होता है। यह इंस्टॉल किए गए विशेष एप्लिकेशन के लिए हेल्पसेट को परिभाषित करता है और एप्लिकेशन के लिए सिस्टम सहायता के हिस्से के रूप में कई सबसेट शामिल करता है। जावा प्रोग्राम को हेल्पसेट फ़ाइल खोजने में सक्षम होना चाहिए जिसका नाम .hs एक्सटेंशन के साथ समाप्त होता है।

## जावा हेल्पसेट सूचना

एक .hs फ़ाइल में निम्न जानकारी हो सकती है।

|सूचना|विवरण|
---|---|
|मैप फ़ाइल|मैप फ़ाइल का उपयोग विषय आईडी को यूनिफ़ॉर्म रिसोर्स लोकेटर या हाइपरटेक्स्ट मार्क-अप लैंग्वेज टॉपिक फ़ाइलों के पथ नाम के साथ जोड़ने के लिए किया जाता है।|
|जानकारी देखें|वह जानकारी जो हेल्पसेट के भीतर कार्यरत नाविकों का वर्णन करती है। गुणवत्ता नेविगेटर हैं: सामग्री की तालिका, अनुक्रमणिका और पूर्ण-पाठ खोज। आगे के नेविगेटर में ग्लॉस और पसंदीदा नेविगेटर भी शामिल हैं। कस्टम नेविगेटर के बारे में डेटा आगे यहाँ संलग्न है.|
<html>|हेल्पसेट शीर्षक|द \<title> हेल्पसेट (.hs) फ़ाइल में रेखांकित किया गया है। यह शीर्षक आपकी हेल्पसेट फ़ाइल में उल्लिखित अधिकांश विंडो और किसी भी द्वितीयक विंडो के शीर्ष पर दिखाई देता है </html>
|होम आईडी|(डिफ़ॉल्ट) आईडी का शीर्षक जो तब प्रदर्शित होता है जब सहायता देखने वाले को आईडी बताए बिना कॉल किया जाता है।|
|प्रस्तुति|विंडो जिसमें सहायता विषयों को दिखाना है। यह JavaHelp 2 कंप्यूटर प्रोग्राम का एक आधुनिक समावेश है जिसे नीचे अधिक विवरण में वर्णित किया गया है \<presentation> .|
|सब-हेल्पसेट्स|यह विवेकाधीन क्षेत्र टैग का उपयोग करके स्थिर रूप से अन्य हेल्पसेट्स को शामिल करता है। इस टैग द्वारा दिखाए गए हेल्पसेट स्वाभाविक रूप से उस हेल्पसेट में संयुक्त होते हैं जिसमें टैग होता है। सम्मिश्रण के बारे में रुचि के अधिक बिंदु सम्मिश्रण हेल्पसेट्स में पाए जा सकते हैं।
|कार्यान्वयन|यह विवेकाधीन खंड एक रजिस्ट्री बनाता है जो हेल्पसेट.क्रिएटहेल्पब्रोकर विधि के भीतर उपयोग करने के लिए हेल्पब्रोकर वर्ग को चिह्नित करने के लिए महत्वपूर्ण जानकारी मैपिंग देता है। रजिस्ट्री अतिरिक्त रूप से किसी दिए गए अनुकरण क्रम के लिए ग्राहक को पदार्थ दर्शक तय करती है

## जावा एचएस फ़ाइल स्वरूप

Java HS फ़ाइलें XML फ़ाइल स्वरूप में हैं और वर्ल्ड वाइड वेब कंसोर्टियम (W3C) विस्तारित मार्कीअप लैंग्वेज प्रस्तावित अनुशंसा [PR-xml-971208](http://www.w3.org/TR/PR-xml-) पर आधारित हैं 971208). इसका मतलब यह है कि जावा एचएस फ़ाइल मानव पठनीय एक्सएमएल फ़ाइल प्रारूप में है जिसे किसी भी एक्सएमएल रीडर एप्लिकेशन में खोला जा सकता है।

### जावा एचएस फ़ाइल स्वरूप उदाहरण

[ओरेकल हेल्पसेट प्रलेखन](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html) से प्राप्त हेल्पसेट फ़ाइल का एक उदाहरण निम्नलिखित है।

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## संदर्भ
* [ओरेकल जावा हेल्पसेट फ़ाइल](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# एचएस - हास्केल स्क्रिप्ट फ़ाइल स्वरूप

## एचएस फाइल क्या है?

.hs एक्सटेंशन वाली फ़ाइल एक हास्केल स्क्रिप्ट फ़ाइल होती है जो [Haskell](https://wiki.haskell.org/Haskell) में लिखी जाती है, जो एक उन्नत विशुद्ध रूप से कार्यात्मक ओपन-सोर्स प्रोग्रामिंग भाषा है। HS फ़ाइल में लिखा गया कोड विशुद्ध रूप से फ़ंक्शंस पर आधारित है, [C](/hi/ प्रोग्रामिंग/c/), [C++](/hi/ प्रोग्रामिंग/cpp/) और इसी तरह के विपरीत, जो मजबूत और संक्षिप्त सॉफ़्टवेयर के तेजी से विकास के सिद्धांतों का पालन करते हैं। हास्केल लचीले और उच्च गुणवत्ता वाले अनुप्रयोगों का उत्पादन करने के लिए समृद्ध एपीआई, प्रोफाइलर और डिबगर्स के साथ-साथ अंतर्निर्मित संगामिति और समानता प्रदान करता है।

## एचएस फ़ाइल स्वरूप

किसी भी प्रोग्रामिंग भाषा की तरह, HS फाइलें सादे पाठ प्रारूप में लिखी जाती हैं जो मानव पठनीय होती हैं। इन्हें किसी भी उपलब्ध टेक्स्ट टूल के साथ बनाया, संपादित और देखा जा सकता है। .Hs स्रोत कोड फ़ाइल एक हास्केल कंपाइलर के साथ संकलित की जाती है, जो निष्पादन योग्य बाइनरी फ़ाइल उत्पन्न करती है।

### एचएस फ़ाइल स्वरूप उदाहरण

कोड को .hs फ़ाइल में लिखा जा सकता है और [GHC](http://haskell.org/ghc) जैसे हास्केल कंपाइलर का उपयोग करके संकलित किया जा सकता है। कोड की निम्न पंक्ति `HelloWorld.hs` के रूप में सहेजी गई है जैसा कि निम्नलिखित नमूने में दिखाया गया है।

```
main = putStrLn "Hello, World!"
```

यह कमांड का उपयोग करके संकलित किया गया है:

```
$ ghc -o hello hello.hs
```
और परिणामी निष्पादन योग्य फ़ाइल को इस प्रकार चलाया जा सकता है:

```
$ ./hello
```
यह "हैलो, वर्ल्ड!" प्रिंट करता है। आउटपुट के लिए बयान।

## संदर्भ

* [हास्केल](https://wiki.haskell.org/Haskell)
* [हास्केल 5 आसान चरणों में](https://wiki.haskell.org/Haskell_in_5_steps)

