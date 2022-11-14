{
  "date" : "2019-10-11",
  "keywords" :[ "archivo ltx", "formato de archivo ltx", "qué es un archivo ltx", "archivo", "ejemplo ltx", "extensión de archivo ltx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Archivo de documento de látex",
  "description":"Obtenga información sobre el formato de archivo LTX y las API que pueden crear y abrir archivos LTX",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## ¿Qué es un archivo LTX?

Un registro con extensión .ltx es un documento de lenguaje de marcado basado en un libro hecho con el marco de composición conocido como LaTex. En gran parte de los casos, se utiliza para caracterizar las composiciones tipográficas para distribuciones, cartas, libros y otros registros comparativos en diferentes campos. El diseño de registros de látex actualiza el informe utilizando cálculos específicos, órdenes para organizar el archivo y las sutilezas más pequeñas. Los procesadores Latex, como TeXworks, Texmaker, LaTeX Editor, proTeXt y Notepad ++, se pueden utilizar para abrir y modificar archivos Tex.

## Formato de archivo LTX

Los documentos LATEX son registros de texto sin formato que se pueden modificar en cualquier procesador de texto. El marco de composición tipográfica de Tex se utiliza generalmente en la comunidad académica, especialmente en los campos de las matemáticas, la ingeniería de software, los aspectos financieros, el diseño y otros. Contiene un montón de comandos que normalmente comienzan con una línea de puntuación oblicua (/es/) y se reúnen con soportes ondulados. Las observaciones/comentarios en un archivo LTX comienzan y terminan con dos porcentajes de imágenes (%%). Los archivos LTX son similares a los archivos [.tex](/es/page-description-language/tex/) y [.latex](/es/word-processing/latex/) y a menudo encontrará documentos latex guardados en estos formatos.

### Ejemplo LTX

El siguiente contenido se puede pegar en un archivo de texto para crear un documento LaTex simple.

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

La salida del archivo de comando anterior debería verse así:

{{< figure src="../latex-example.png" alt="Formato de archivo de látex" >}}

## Referencias ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [Látex](http://mally.stanford.edu/~sr/computing/latex-example.html)

