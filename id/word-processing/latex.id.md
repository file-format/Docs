{
  "date" : "2019-10-11",
  "keywords" :[ "file lateks", "format file lateks", "apa itu file lateks", "file", "contoh lateks", "ekstensi file lateks", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Berkas Dokumen Lateks",
  "description":"Pelajari tentang format file LATEX dan API yang dapat membuat dan membuka file LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Apa itu file LATEX?

File dengan ekstensi .latex adalah file bahasa markup berbasis teks yang dibuat dengan sistem penyusunan huruf yang dikenal sebagai LaTex. Dalam sebagian besar kasus, ini digunakan untuk menentukan pengaturan huruf untuk publikasi, surat, buku, dan katalog serupa lainnya di berbagai bidang. Format file lateks menyempurnakan dokumen menggunakan algoritme khusus, perintah untuk memformat dokumen, dan detail terkecil. Prosesor lateks seperti TeXworks, Texmaker, LaTeX Editor, proTeXt, dan Notepad++ dapat digunakan untuk membuka dan mengedit file Tex.

## Format File LATEX

File LATEX adalah file teks biasa yang dapat diedit di editor teks apa pun. Sistem typesetting Tex banyak digunakan di dunia akademis terutama di bidang matematika, ilmu komputer, ekonomi, teknik, dan sejenisnya. Ini terdiri dari satu set perintah yang biasanya dimulai dengan garis miring terbalik dan dikelompokkan dengan kurung kurawal. Komentar dalam file tex dimulai dan diakhiri dengan simbol persen ganda (%%).

### Contoh LATEX

Konten berikut dapat disisipkan dalam file teks untuk membuat dokumen LaTex sederhana.

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

Output dari file perintah di atas akan terlihat seperti ini:

{{< figure src="../latex-example.png" alt="Format File Lateks" >}}

## Referensi ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
