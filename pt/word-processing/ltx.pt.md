{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo ltx", "formato de arquivo ltx", "o que é um arquivo ltx", "arquivo", "exemplo ltx", "extensão de arquivo ltx", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Arquivo de Documento Látex",
  "description":"Saiba mais sobre o formato de arquivo LTX e as APIs que podem criar e abrir arquivos LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## O que é um arquivo LTX?

Um registro com extensão .ltx é um documento de linguagem de marcação baseado em livro feito com a estrutura de composição conhecida como LaTex. Em grande parte dos casos, é utilizado para caracterizar as composições tipográficas para distribuições, cartas, livros e outros registros comparativos em diferentes áreas. O design do registro de látex atualiza o relatório utilizando cálculos específicos, ordens de organização do arquivo e as menores sutilezas. Processadores de látex, por exemplo, TeXworks, Texmaker, LaTeX Editor, proTeXt e Notepad++ podem ser utilizados para abrir e alterar registros Tex.

## Formato de arquivo LTX

Documentos LATEX são registros de texto simples que podem ser alterados em qualquer processador de texto. A estrutura tipográfica Tex é geralmente utilizada na comunidade acadêmica, particularmente nas áreas de matemática, engenharia de software, aspectos financeiros, design e outros. Ele contém vários comandos normalmente começando com uma linha de pontuação oblíqua (/pt/) e reunidos com suportes ondulados. As observações/comentários em um arquivo LTX começam e terminam com duas porcentagens de imagens (%%). Os arquivos LTX são semelhantes aos arquivos [.tex](/pt/page-description-language/tex/) e [.latex](/pt/word-processing/latex/) e você encontrará frequentemente documentos de látex salvos nesses formatos.

### Exemplo de LTX

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
* [Látex](http://mally.stanford.edu/~sr/computing/latex-example.html)

