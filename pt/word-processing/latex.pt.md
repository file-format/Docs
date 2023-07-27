{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo latex", "formato de arquivo latex", "o que é um arquivo latex", "arquivo", "exemplo latex", "extensão do arquivo latex", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Arquivo de Documento Látex",
  "description":"Saiba mais sobre o formato de arquivo LATEX e APIs que podem criar e abrir arquivos LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## O que é um arquivo LATEX?

Um arquivo com extensão .latex é um arquivo de linguagem de marcação baseada em texto criado com o sistema de composição conhecido como LaTex. Na maioria dos casos, é usado para definir as composições tipográficas de publicações, cartas, livros e outras catalogações semelhantes em diversos campos. O formato de arquivo látex aprimora o documento usando algoritmos especializados, comandos para formatação do documento e os mínimos detalhes. Processadores de látex como TeXworks, Texmaker, LaTeX Editor, proTeXt e Notepad++ podem ser usados para abrir e editar arquivos Tex.

## Formato de arquivo LATEX

Os arquivos LATEX são arquivos de texto simples que podem ser editados em qualquer editor de texto. O sistema de composição Tex é amplamente utilizado na academia, especialmente nas áreas de matemática, ciência da computação, economia, engenharia e outras similares. É composto por um conjunto de comandos geralmente começando com uma barra invertida e agrupados com chaves. Comentários em um arquivo tex começam e terminam com símbolos de porcentagem dupla (%%).

### Exemplo de LATEX

O conteúdo a seguir pode ser colado em um arquivo de texto para criar um documento LaTex simples.

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

A saída do arquivo de comando acima deve ficar assim:

{{< figure src="../latex-example.png" alt="Formato de arquivo látex" >}}

## Referências ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
