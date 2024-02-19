{
  "date": "2019-10-11",
  "keywords": [
    "ltx file",
    "ltx file format",
    "what is an ltx file",
    "file",
    "ltx example",
    "ltx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LTX - ল্যাটেক্স ডকুমেন্ট ফাইল",
  "description": "LTX ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি LTX ফাইল তৈরি এবং খুলতে পারে৷",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ltx-bn"
    }
  },
  "lastmod": "2021-05-18"
}

## একটি LTX ফাইল কি?

.ltx এক্সটেনশন সহ একটি রেকর্ড হল একটি বই ভিত্তিক মার্কআপ ভাষা নথি যা LaTex নামে পরিচিত টাইপসেটিং কাঠামোর সাথে তৈরি। কেসগুলির একটি বড় অংশে, এটি বিভিন্ন ক্ষেত্রে বিতরণ, অক্ষর, বই এবং অন্যান্য তুলনামূলক রেকর্ডিংয়ের জন্য টাইপসেটিংগুলিকে চিহ্নিত করতে ব্যবহার করা হয়। ল্যাটেক্স রেকর্ড ডিজাইন নির্দিষ্ট গণনা, সংরক্ষণাগার সাজানোর আদেশ এবং ক্ষুদ্রতম সূক্ষ্মতা ব্যবহার করে প্রতিবেদনটিকে আপগ্রেড করে। ল্যাটেক্স প্রসেসর, উদাহরণস্বরূপ, TeXworks, Texmaker, LaTeX Editor, proTeXt এবং Notepad++ ব্যবহার করা যেতে পারে টেক্স রেকর্ড খুলতে এবং পরিবর্তন করতে।

## LTX ফাইল ফরম্যাট

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX উদাহরণ

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


