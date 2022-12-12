{
  "date" : "2019-10-11",
  "keywords" :[ "soubor ltx", "formát souboru ltx", "co je soubor ltx", "soubor", "příklad ltx", "přípona souboru ltx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex Document File",
  "description":"Další informace o formátu souboru LTX a rozhraních API, která mohou vytvářet a otevírat soubory LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Co je soubor LTX?

Záznam s příponou .ltx je dokument značkovacího jazyka založený na knize vytvořený pomocí rámce pro sázení známého jako LaTex. Ve velké části případů se používá k charakterizaci sazby pro distribuce, dopisy, knihy a další srovnávací záznamy v různých oblastech. Návrh latexových záznamů aktualizuje sestavu pomocí specifických výpočtů, příkazů pro uspořádání archivu a nejmenších jemností. Latexové procesory, například TeXworks, Texmaker, LaTeX Editor, proTeXt a Notepad++, lze použít k otevírání a úpravě záznamů Tex.

## Formát souboru LTX

Dokumenty LATEXu jsou záznamy ve formátu prostého textu, které lze měnit v libovolném textovém procesoru. Sázecí rámec Tex je obecně využíván ve vědecké komunitě zejména v oblasti matematiky, softwarového inženýrství, finančních aspektů, projektování a podobně. Obsahuje spoustu příkazů obvykle začínajících šikmou interpunkční čárou (/cs/) a shromážděných s vlnitými podpěrami. Poznámky/komentáře v souboru LTX začínají a končí dvojnásobným procentem obrázků (%%). Soubory LTX jsou podobné souborům [.tex](/cs/page-description-language/tex/) a [.latex](/cs/word-processing/latex/) a často najdete latexové dokumenty uložené v těchto formátech.

### Příklad LTX

Následující obsah lze vložit do textového souboru a vytvořit jednoduchý dokument LaTex.

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

Výstup příkazového souboru výše by měl vypadat takto:

{{< figure src="../latex-example.png" alt="Formát souboru Latex" >}}

## Reference ##

* [TEX - Wikipedie](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

