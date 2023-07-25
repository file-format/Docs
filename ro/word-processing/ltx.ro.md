{
  "date" : "2019-10-11",
  "keywords" :[ "fișier ltx", "format fișier ltx", "ce este un fișier ltx", "fișier", "exemplu ltx", "extensie fișier ltx", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Fișier document latex",
  "description":"Aflați despre formatul de fișier LTX și despre API-urile care pot crea și deschide fișiere LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Ce este un fișier LTX?

O înregistrare cu extensia .ltx este un document cu limbaj de marcare bazat pe cărți, realizat cu cadrul de compunere cunoscut sub numele de LaTex. Într-o mare parte din cazuri, este utilizat pentru a caracteriza compozițiile pentru distribuții, scrisori, cărți și alte înregistrări comparative în diferite domenii. Designul înregistrărilor din Latex îmbunătățește raportul utilizând calcule specifice, comenzi pentru aranjarea arhivei și cele mai mici subtilități. Procesoarele Latex, de exemplu, TeXworks, Texmaker, LaTeX Editor, proTeXt și Notepad++ pot fi utilizate pentru a deschide și modifica înregistrările Tex.

## Format de fișier LTX

Documentele LATEX sunt înregistrări cu text simplu care pot fi modificate în orice procesor de text. Cadrul de tipărire Tex este, în general, utilizat în comunitatea academică, în special în domeniile matematicii, ingineriei software, aspectelor financiare, proiectării și altele asemenea. Conține o grămadă de comenzi care încep în mod normal cu o linie de punctuație oblică (/ro/) și adunate cu suporturi ondulate. Observațiile/comentariile dintr-un fișier LTX încep și se termină cu imagini de două ori procente (%%). Fișierele LTX sunt similare cu fișierul [.tex](/ro/page-description-language/tex/) și [.latex](/ro/word-processing/latex/) și veți găsi adesea documente latex salvate în aceste formate.

### Exemplu LTX

Următorul conținut poate fi lipit într-un fișier text pentru a crea un document LaTex simplu.

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

Ieșirea fișierului de comandă de mai sus ar trebui să arate astfel:

{{< figure src="../latex-example.png" alt="Format de fișier latex" >}}

## Referințe ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
