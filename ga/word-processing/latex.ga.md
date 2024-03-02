{
  "date": "2019-10-11",
  "keywords": [
"comhad laitéis",
"formáid comhaid laitéis",
"cad is comhad laitéis ann",
"comhad",
"sampla laitéis",
"síneadh comhad laitéis",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX - Comhad Doiciméid LaTeX",
  "description": "Foghlaim faoi fhormáid comhaid LATEX agus APInna ar féidir leo comhaid LATEX a chruthú agus a oscailt.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-gax"
}
},
  "lastmod": "2021-05-18"
}

## Cad is comhad LATEX ann?

Is comhad teanga marcála téacs-bhunaithe é comhad a bhfuil síneadh .latex aige a cruthaíodh leis an gcóras clóchuradóireachta ar a dtugtar LaTex. I bhformhór na gcásanna, úsáidtear é chun na clóchuradóireacht a shainiú d’fhoilseacháin, litreacha, leabhair agus catalógú eile dá samhail i réimsí éagsúla. Feabhsaíonn formáid comhaid laitéis an doiciméad trí úsáid a bhaint as halgartaim speisialaithe, orduithe chun an doiciméad a fhormáidiú, agus na sonraí is lú. Is féidir próiseálaithe laitéis mar TeXworks, Texmaker, LaTeX Editor, proTeXt, agus Notepad++ a úsáid chun comhaid Tex a oscailt agus a chur in eagar.

## Formáid Chomhaid LATEX

Is comhaid gnáth-théacs iad comhaid LATEX is féidir a chur in eagar in aon eagarthóir téacs. Úsáidtear córas clóchuradóireachta tex go forleathan san saol acadúil, go háirithe i réimsí na matamaitice, na heolaíochta ríomhaireachta, na heacnamaíochta, na hinnealtóireachta, agus réimsí eile dá samhail. Tá sé comhdhéanta de shraith orduithe a thosaíonn go coitianta le backslash agus grúpáilte le braces chatach. Tosaíonn agus críochnaíonn tuairimí i gcomhad tex le siombailí faoin gcéad dúbailte (%%).

### Sampla LATEX

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

* [TEX - Vicipéid](https://ga.wikipedia.org/wiki/TeX)


