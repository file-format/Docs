{
  "date" : "2019-10-11",
  "keywords" :[ "fișier latex", "format fișier latex", "ce este un fișier latex", "fișier", "exemplu latex", "extensie fișier latex", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Fișier document Latex",
  "description":"Aflați despre formatul de fișier LATEX și despre API-urile care pot crea și deschide fișiere LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Ce este un fișier LATEX?

Un fișier cu extensia .latex este un fișier de limbaj de marcare bazat pe text creat cu sistemul de tipărire cunoscut sub numele de LaTex. În majoritatea cazurilor, este utilizat pentru a defini compozițiile pentru publicații, scrisori, cărți și alte catalogări similare în diverse domenii. Formatul de fișier Latex îmbunătățește documentul folosind algoritmi specializați, comenzi pentru formatarea documentului și cele mai mici detalii. Procesoare Latex precum TeXworks, Texmaker, LaTeX Editor, proTeXt și Notepad++ pot fi folosite pentru a deschide și edita fișiere Tex.

## Format de fișier LATEX

Fișierele LATEX sunt fișiere text simplu care pot fi editate în orice editor de text. Sistemul de tipărire Tex este utilizat pe scară largă în mediul academic, în special în domeniile matematicii, informaticii, economiei, ingineriei și altele similare. Acesta cuprinde un set de comenzi care încep de obicei cu o bară oblică inversă și grupate cu acolade. Comentariile dintr-un fișier tex încep și se termină cu simboluri procentuale duble (%%).

### Exemplu de LATEX

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
