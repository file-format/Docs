{
  "date" : "2019-10-11",
  "keywords" :["लेटेक्स फ़ाइल", "लेटेक्स फ़ाइल स्वरूप", "लेटेक्स फ़ाइल क्या है", "फ़ाइल", "लेटेक्स उदाहरण", "लेटेक्स फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"लेटेक्स - लेटेक्स दस्तावेज़ फ़ाइल",
  "description":"लेटेक्स फ़ाइल प्रारूप और एपीआई के बारे में जानें जो लेटेक्स फाइलें बना और खोल सकते हैं।",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## लेटेक्स फ़ाइल क्या है?

.latex एक्सटेंशन वाली फाइल एक टेक्स्ट-आधारित मार्कअप लैंग्वेज फाइल है जिसे टाइपसेटिंग सिस्टम के साथ बनाया जाता है जिसे LaTex के नाम से जाना जाता है। अधिकांश मामलों में, इसका उपयोग विभिन्न क्षेत्रों में प्रकाशनों, पत्रों, पुस्तकों और अन्य समान कैटलॉगिंग के लिए टाइपसेटिंग को परिभाषित करने के लिए किया जाता है। लेटेक्स फ़ाइल प्रारूप विशेष एल्गोरिदम का उपयोग करके दस्तावेज़ को बढ़ाता है, दस्तावेज़ के प्रारूपण के लिए आदेश और सबसे छोटा विवरण। TeXworks, Texmaker, LaTeX Editor, proTeXt, और Notepad++ जैसे लेटेक्स प्रोसेसर का उपयोग टेक्स फ़ाइलों को खोलने और संपादित करने के लिए किया जा सकता है।

## लेटेक्स फ़ाइल स्वरूप

लेटेक्स फ़ाइलें सादा पाठ फ़ाइलें हैं जिन्हें किसी भी पाठ संपादक में संपादित किया जा सकता है। टेक्स टाइपसेटिंग सिस्टम का व्यापक रूप से अकादमिक क्षेत्र में विशेष रूप से गणित, कंप्यूटर विज्ञान, अर्थशास्त्र, इंजीनियरिंग और इसी तरह के अन्य क्षेत्रों में उपयोग किया जाता है। इसमें आमतौर पर बैकस्लैश से शुरू होने वाले कमांड का एक सेट होता है और घुंघराले ब्रेसिज़ के साथ समूहीकृत होता है। टेक्स फ़ाइल में टिप्पणियाँ दोहरे प्रतिशत प्रतीकों (%%) के साथ शुरू और समाप्त होती हैं।

### लेटेक्स उदाहरण

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

* [टेक्स - विकिपीडिया] (https://en.wikipedia.org/wiki/TeX)
* [लेटेक्स](http://mally.stanford.edu/~sr/computing/latex-example.html)

