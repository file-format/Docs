{
  "date": "2019-10-11",
  "keywords": [
"ltx faylı",
"ltx fayl formatı",
"ltx faylı nədir",
"fayl",
"ltx nümunəsi",
"ltx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LTX - Lateks Sənəd Faylı",
  "description": "LTX faylları yarada və aça bilən LTX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LTX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-lt-azx"
}
},
  "lastmod": "2021-05-18"
}

## LTX faylı nədir?

.ltx uzantısı olan qeyd LaTex kimi tanınan yazı çərçivəsi ilə hazırlanmış kitaba əsaslanan işarələmə dili sənədidir. İşlərin böyük bir hissəsində, müxtəlif sahələrdə paylamalar, məktublar, kitablar və digər müqayisəli qeydlər üçün yazı tiplərini xarakterizə etmək üçün istifadə olunur. Lateks qeyd dizaynı xüsusi hesablamalar, arxivin təşkili üçün sifarişlər və ən kiçik incəliklərdən istifadə etməklə hesabatı təkmilləşdirir. Lateks prosessorları, məsələn, TeXworks, Texmaker, LaTeX Editor, proTeXt və Notepad++, Tex qeydlərini açmaq və dəyişdirmək üçün istifadə edilə bilər.

## LTX fayl formatı

LATEX documents are plain text records that can be altered in any word processor. Tex typesetting framework is generally utilized in scholarly community particularly in the fields of math, software engineering, financial aspects, designing, and likewise others. It contains a bunch of commands normally beginning with an oblique punctuation line (/) and gathered with wavy supports. Remarks/comments in an LTX file start and end with twofold percent images (%%). LTX files are similar to [.tex](/page-description-language/tex/) and [.latex](/word-processing/latex/) file and you will often find latex documents saved in these formats.

### LTX Nümunəsi

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


