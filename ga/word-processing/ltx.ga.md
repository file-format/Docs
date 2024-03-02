{
  "date": "2019-10-11",
  "keywords": [
"comhad ltx",
"Formáid comhaid ltx",
"cad is comhad ltx ann",
"comhad",
"sampla ltx",
"Síneadh comhad ltx",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LTX - Comhad Doiciméad LaTeX",
  "description": "Foghlaim faoi fhormáid comhaid LTX agus APIanna ar féidir leo comhaid LTX a chruthú agus a oscailt.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-gax"
}
},
  "lastmod": "2021-05-18"
}

## Cad is comhad LTX ann?

Is doiciméad teanga marcála bunaithe ar leabhar é taifead a bhfuil síneadh .ltx air agus a dhéantar leis an gcreat clóchuradóireachta ar a dtugtar LaTex. I gcuid mhór de na cásanna, úsáidtear é chun na clóchur a shainiú do dháiltí, litreacha, leabhair, agus taifeadtaí comparáideacha eile i réimsí éagsúla. Déanann dearadh taifead laitéis an tuarascáil a uasghrádú trí úsáid a bhaint as ríomhanna sonracha, as orduithe chun an chartlann a shocrú, agus as na mionghnéithe is lú. Is féidir próiseálaithe laitéis, mar shampla, TeXworks, Texmaker, LaTeX Editor, proTeXt, agus Notepad++ a úsáid chun taifid Tex a oscailt agus a athrú.

## Formáid Chomhaid LTX

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX Sampla

Is féidir an t-ábhar seo a leanas a ghreamú i gcomhad téacs chun doiciméad simplí LaTex a chruthú.

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

Ba cheart go mbeadh cuma mar seo ar aschur an chomhaid ordaithe thuas:

{{< figure src="../latex-example.png" alt="Formáid Chomhaid LaTeX" >}}

## Tagairtí ##

* [TEX - Vicipéid](https://en.wikipedia.org/wiki/TeX)


