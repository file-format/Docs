{
  "date" : "2019-10-11",
  "keywords" :["एलटीएक्स फाइल", "एलटीएक्स फाइल फॉर्मेट", "एलटीएक्स फाइल क्या है", "फाइल", "एलटीएक्स उदाहरण", "एलटीएक्स फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एलटीएक्स - लेटेक्स दस्तावेज़ फ़ाइल",
  "description":"LTX फ़ाइल स्वरूप और API के बारे में जानें जो LTX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## एलटीएक्स फाइल क्या है?

.ltx एक्सटेंशन वाला एक रिकॉर्ड एक पुस्तक आधारित मार्कअप लैंग्वेज दस्तावेज़ है जिसे LaTex के नाम से जाने जाने वाले टाइपसेटिंग फ्रेमवर्क के साथ बनाया गया है। मामलों के एक बड़े हिस्से में, इसका उपयोग विभिन्न क्षेत्रों में वितरण, पत्र, पुस्तकों और अन्य तुलनात्मक रिकॉर्डिंग के लिए टाइपसेटिंग को चिह्नित करने के लिए किया जाता है। लेटेक्स रिकॉर्ड डिज़ाइन विशिष्ट गणनाओं, संग्रह की व्यवस्था के लिए आदेश, और सबसे छोटी सूक्ष्मताओं का उपयोग करके रिपोर्ट को अपग्रेड करता है। लेटेक्स प्रोसेसर, उदाहरण के लिए, TeXworks, Texmaker, LaTeX Editor, proTeXt, और Notepad++ का उपयोग Tex फ़ाइलों को खोलने और बदलने के लिए किया जा सकता है।

## LTX फ़ाइल स्वरूप

लेटेक्स दस्तावेज़ सादे पाठ रिकॉर्ड हैं जिन्हें किसी भी वर्ड प्रोसेसर में बदला जा सकता है। टेक्स टाइपसेटिंग फ्रेमवर्क का उपयोग आमतौर पर विद्वानों के समुदाय में विशेष रूप से गणित, सॉफ्टवेयर इंजीनियरिंग, वित्तीय पहलुओं, डिजाइनिंग और इसी तरह अन्य क्षेत्रों में किया जाता है। इसमें सामान्य रूप से एक तिरछी विराम चिह्न रेखा (/hi/) से शुरू होने वाले आदेशों का एक गुच्छा होता है और लहरदार समर्थन के साथ इकट्ठा होता है। एलटीएक्स फ़ाइल में टिप्पणियां/टिप्पणियां दो गुना प्रतिशत छवियों (%%) के साथ शुरू और समाप्त होती हैं। LTX फ़ाइलें [.tex](/hi/page-description-language/tex/) और [.latex](/hi/word-processing/latex/) फ़ाइल के समान होती हैं और आपको अक्सर इन स्वरूपों में सहेजे गए लेटेक्स दस्तावेज़ मिलेंगे।

### एलटीएक्स उदाहरण

एक साधारण LaTex दस्तावेज़ बनाने के लिए निम्न सामग्री को टेक्स्ट फ़ाइल में चिपकाया जा सकता है।

```
\documentclass[12pt]{article}
\usepackage{lingmacros}
\usepackage{tree-dvips}
\begin{document}

\section*{Notes for My Paper}

Don't forget to include examples of topicalization.
They look like this:

{\small
\enumsentence{Topicalization from sentential subject:\\
\shortex{7}{a John$_i$ [a & kltukl & [el &
  {\bf l-}oltoir & er & ngii$_i$ & a Mary]]}
{ & {\bf R-}clear & {\sc comp} &
  {\bf IR}.{\sc 3s}-love   & P & him & }
{John, (it's) clear that Mary loves (him).}}
}

\subsection*{How to handle topicalization}

I'll just assume a tree structure like (\ex{1}).

{\small
\enumsentence{Structure of A$'$ Projections:\\ [2ex]
\begin{tabular}[t]{cccc}
    & \node{i}{CP}\\ [2ex]
    \node{ii}{Spec} &   &\node{iii}{C$'$}\\ [2ex]
        &\node{iv}{C} & & \node{v}{SAgrP}
\end{tabular}
\nodeconnect{i}{ii}
\nodeconnect{i}{iii}
\nodeconnect{iii}{iv}
\nodeconnect{iii}{v}
}
}

\subsection*{Mood}

Mood changes when there is a topic, as well as when
there is WH-movement.  \emph{Irrealis} is the mood when
there is a non-subject topic or WH-phrase in Comp.
\emph{Realis} is the mood when there is a subject topic
or WH-phrase.

\end{document}
```

उपरोक्त कमांड फ़ाइल का आउटपुट इस तरह दिखना चाहिए:

{{< figure src="../latex-example.png" alt="लेटेक्स फ़ाइल स्वरूप" >}}

## संदर्भ ##

* [टेक्स - विकिपीडिया](https://en.wikipedia.org/wiki/TeX)
* [लेटेक्स](http://mally.stanford.edu/~sr/computing/latex-example.html)

