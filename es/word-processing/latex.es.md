{
  "date" : "2019-10-11",
  "keywords" :[ "archivo de látex", "formato de archivo de látex", "qué es un archivo de látex", "archivo", "ejemplo de látex", "extensión de archivo de látex", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Archivo de documento de látex",
  "description":"Obtenga más información sobre el formato de archivo LATEX y las API que pueden crear y abrir archivos LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## ¿Qué es un archivo LATEX?

Un archivo con extensión .latex es un archivo de lenguaje de marcado basado en texto creado con el sistema de composición conocido como LaTex. En la mayoría de los casos, se utiliza para definir la composición tipográfica de publicaciones, cartas, libros y otras catalogaciones similares en varios campos. El formato de archivo Latex mejora el documento utilizando algoritmos especializados, comandos para formatear el documento y los detalles más pequeños. Los procesadores Latex como TeXworks, Texmaker, LaTeX Editor, proTeXt y Notepad++ se pueden usar para abrir y editar archivos Tex.

## Formato de archivo LATEX

Los archivos LATEX son archivos de texto sin formato que se pueden editar en cualquier editor de texto. El sistema de composición tipográfica Tex se usa ampliamente en el mundo académico, especialmente en los campos de las matemáticas, la informática, la economía, la ingeniería y otros similares. Se compone de un conjunto de comandos que normalmente comienzan con una barra invertida y se agrupan con llaves. Los comentarios en un archivo tex comienzan y terminan con símbolos de doble porcentaje (%%).

### Ejemplo de LÁTEX

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

