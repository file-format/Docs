{
  "date" : "2019-10-11",
  "keywords" :[ "fichier ltx", "format de fichier ltx", "qu'est-ce qu'un fichier ltx", "fichier", "exemple ltx", "extension de fichier ltx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Fichier de documents en latex",
  "description":"En savoir plus sur le format de fichier LTX et les API qui peuvent créer et ouvrir des fichiers LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Qu'est-ce qu'un fichier LTX ?

Un enregistrement avec l'extension .ltx est un document en langage de balisage basé sur un livre créé avec le cadre de composition connu sous le nom de LaTex. Dans une grande partie des cas, il est utilisé pour caractériser les compositions pour les distributions, les lettres, les livres et autres enregistrements comparatifs dans différents domaines. La conception d'enregistrement Latex améliore le rapport en utilisant des calculs spécifiques, des commandes pour l'organisation des archives et les moindres subtilités. Les processeurs Latex, par exemple, TeXworks, Texmaker, LaTeX Editor, proTeXt et Notepad++ peuvent être utilisés pour ouvrir et modifier des enregistrements Tex.

## Format de fichier LTX

Les documents LATEX sont des enregistrements en texte brut qui peuvent être modifiés dans n'importe quel traitement de texte. Le cadre de composition Tex est généralement utilisé dans la communauté universitaire, en particulier dans les domaines des mathématiques, du génie logiciel, des aspects financiers, de la conception, etc. Il contient un tas de commandes commençant normalement par une ligne de ponctuation oblique (/fr/) et rassemblées avec des supports ondulés. Les remarques/commentaires dans un fichier LTX commencent et se terminent par deux fois plus d'images (%%). Les fichiers LTX sont similaires aux fichiers [.tex](/fr/page-description-language/tex/) et [.latex](/fr/word-processing/latex/) et vous trouverez souvent des documents latex enregistrés dans ces formats.

### Exemple LTX

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
