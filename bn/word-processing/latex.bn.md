{
  "date": "2019-10-11",
  "keywords": [
    "latex file",
    "latex file format",
    "what is an latex file",
    "file",
    "latex example",
    "latex file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ল্যাটেক্স - ল্যাটেক্স ডকুমেন্ট ফাইল",
  "description": "LATEX ফাইল বিন্যাস এবং API সম্পর্কে জানুন যেগুলি LATEX ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-latex-bn"
    }
  },
  "lastmod": "2021-05-18"
}

## একটি LATEX ফাইল কি?

.latex এক্সটেনশন সহ একটি ফাইল হল একটি টেক্সট-ভিত্তিক মার্কআপ ল্যাঙ্গুয়েজ ফাইল যা LaTex নামে পরিচিত টাইপসেটিং সিস্টেমের সাথে তৈরি করা হয়। বেশিরভাগ ক্ষেত্রে, এটি বিভিন্ন ক্ষেত্রে প্রকাশনা, চিঠিপত্র, বই এবং অন্যান্য অনুরূপ ক্যাটালগিংয়ের জন্য টাইপসেটিংস সংজ্ঞায়িত করতে ব্যবহৃত হয়। ল্যাটেক্স ফাইল ফরম্যাট বিশেষ অ্যালগরিদম, নথির বিন্যাসের জন্য কমান্ড এবং ক্ষুদ্রতম বিবরণ ব্যবহার করে নথিটিকে উন্নত করে। ল্যাটেক্স প্রসেসর যেমন TeXworks, Texmaker, LaTeX Editor, proTeXt, এবং Notepad++ Tex ফাইলগুলি খুলতে এবং সম্পাদনা করতে ব্যবহার করা যেতে পারে।

## ল্যাটেক্স ফাইল ফরম্যাট

LATEX ফাইলগুলি হল প্লেইন টেক্সট ফাইল যা যেকোনো টেক্সট এডিটরে এডিট করা যায়। টেক্স টাইপসেটিং সিস্টেমটি একাডেমিয়ায় বিশেষ করে গণিত, কম্পিউটার বিজ্ঞান, অর্থনীতি, প্রকৌশল এবং একইভাবে অন্যান্য ক্ষেত্রে ব্যাপকভাবে ব্যবহৃত হয়। এটি সাধারণত একটি ব্যাকস্ল্যাশ দিয়ে শুরু করে এবং কোঁকড়া ধনুর্বন্ধনী দিয়ে গোষ্ঠীবদ্ধ কমান্ডের একটি সেট নিয়ে গঠিত। একটি টেক্স ফাইলে মন্তব্যগুলি দ্বিগুণ শতাংশ চিহ্ন (%%) দিয়ে শুরু এবং শেষ হয়।

### ল্যাটেক্স উদাহরণ

একটি সাধারণ LaTex নথি তৈরি করতে নিম্নলিখিত বিষয়বস্তু একটি পাঠ্য ফাইলে আটকানো যেতে পারে।

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

উপরের কমান্ড ফাইলের আউটপুট এই মত হওয়া উচিত:

{{< figure src="../latex-example.png" alt="ল্যাটেক্স ফাইল ফরম্যাট" >}}

## তথ্যসূত্র ##

* [TEX - উইকিপিডিয়া](https://en.wikipedia.org/wiki/TeX)


