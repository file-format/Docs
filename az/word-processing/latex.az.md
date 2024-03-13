{
  "date": "2019-10-11",
  "keywords": [
"lateks faylı",
"lateks fayl formatı",
"lateks faylı nədir",
"fayl",
"lateks nümunəsi",
"lateks fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LATEX - Lateks Sənəd Faylı",
  "description": "LATEX faylları yarada və aça bilən LATEX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LATEX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-late-azx"
}
},
  "lastmod": "2021-05-18"
}

## LATEX faylı nədir?

.latex uzantısı olan fayl LaTex kimi tanınan yazı sistemi ilə yaradılmış mətn əsaslı işarələmə dili faylıdır. Əksər hallarda müxtəlif sahələrdə nəşrlər, məktublar, kitablar və digər analoji kataloqlaşdırma üçün çap parametrlərini müəyyən etmək üçün istifadə olunur. Lateks fayl formatı xüsusi alqoritmlərdən, sənədin formatlaşdırılması əmrlərindən və ən xırda detallardan istifadə edərək sənədi təkmilləşdirir. TeXworks, Texmaker, LaTeX Editor, proTeXt və Notepad++ kimi lateks prosessorları Tex fayllarını açmaq və redaktə etmək üçün istifadə edilə bilər.

## LATEX fayl formatı

LATEX faylları istənilən mətn redaktorunda redaktə edilə bilən düz mətn fayllarıdır. Mətn yazma sistemi akademik mühitdə, xüsusən riyaziyyat, kompüter elmləri, iqtisadiyyat, mühəndislik və buna bənzər digər sahələrdə geniş istifadə olunur. O, adətən tərs xətt ilə başlayan və əyri mötərizələrlə qruplaşdırılmış əmrlər dəstindən ibarətdir. Tex faylındakı şərhlər ikiqat faiz simvolları ilə başlayır və bitir (%%).

### LATEX Nümunəsi

Sadə bir LaTex sənədi yaratmaq üçün aşağıdakı məzmun mətn faylına yapışdırıla bilər.

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

Yuxarıdakı əmr faylının çıxışı belə görünməlidir:

{{< figure src="../latex-example.png" alt="Lateks fayl formatı" >}}

## İstinadlar ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)


