{
  "date" : "2019-10-11",
  "keywords" :[ "fichier latex", "format de fichier latex", "qu'est-ce qu'un fichier latex", "fichier", "exemple latex", "extension de fichier latex", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Fichier de documents en latex",
  "description":"En savoir plus sur le format de fichier LATEX et les API qui peuvent créer et ouvrir des fichiers LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Qu'est-ce qu'un fichier LATEX ?

Un fichier avec l'extension .latex est un fichier de langage de balisage textuel créé avec le système de composition connu sous le nom de LaTex. Dans la plupart des cas, il est utilisé pour définir les compositions pour les publications, les lettres, les livres et autres catalogages similaires dans divers domaines. Le format de fichier Latex améliore le document à l'aide d'algorithmes spécialisés, de commandes de formatage du document et des moindres détails. Les processeurs Latex tels que TeXworks, Texmaker, LaTeX Editor, proTeXt et Notepad++ peuvent être utilisés pour ouvrir et modifier des fichiers Tex.

## Format de fichier LATEX

Les fichiers LATEX sont des fichiers de texte brut qui peuvent être modifiés dans n'importe quel éditeur de texte. Le système de composition Tex est largement utilisé dans le milieu universitaire, en particulier dans les domaines des mathématiques, de l'informatique, de l'économie, de l'ingénierie et autres. Il comprend un ensemble de commandes commençant généralement par une barre oblique inverse et regroupées avec des accolades. Les commentaires dans un fichier tex commencent et se terminent par des symboles de pourcentage double (%%).

### Exemple LATEX

Le contenu suivant peut être collé dans un fichier texte pour créer un simple document LaTex.

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

La sortie du fichier de commandes ci-dessus devrait ressembler à ceci :

{{< figure src="../latex-example.png" alt="Format de fichier latex" >}}

## Références ##

* [TEX - Wikipédia](https://en.wikipedia.org/wiki/TeX)
* [Latex](http://mally.stanford.edu/~sr/computing/latex-example.html)

