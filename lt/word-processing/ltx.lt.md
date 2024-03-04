{
  "date": "2019-10-11",
  "keywords": [
"ltx failą",
"ltx failo formatas",
"kas yra ltx failas",
"failą",
"ltx pavyzdys",
"ltx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LTX – latekso dokumentų failas",
  "description": "Sužinokite apie LTX failo formatą ir API, kurios gali kurti ir atidaryti LTX failus.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-ltx"
}
},
  "lastmod": "2021-05-18"
}

## Kas yra LTX failas?

Įrašas su plėtiniu .ltx yra knyga pagrįstas žymėjimo kalbos dokumentas, sukurtas naudojant rinkimo sistemą, žinomą kaip LaTex. Daugeliu atvejų jis naudojamas platinimų, laiškų, knygų ir kitų lyginamųjų įrašų įvairiose srityse apibūdinimui. Latekso įrašų dizainas atnaujina ataskaitą panaudojant specifinius skaičiavimus, archyvo sutvarkymo užsakymus ir smulkiausias subtilybes. Latekso procesoriai, pavyzdžiui, TeXworks, Texmaker, LaTeX Editor, proTeXt ir Notepad++, gali būti naudojami Tex įrašams atidaryti ir keisti.

## LTX failo formatas

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX pavyzdys

Toliau pateiktą turinį galima įklijuoti į tekstinį failą, kad būtų sukurtas paprastas LaTex dokumentas.

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

Aukščiau esančio komandos failo išvestis turėtų atrodyti taip:

{{< figure src="../latex-example.png" alt="Latekso failo formatas" >}}

## Nuorodos Nr.

* [TEX – Vikipedija](https://en.wikipedia.org/wiki/TeX)


