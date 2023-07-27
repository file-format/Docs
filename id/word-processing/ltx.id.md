{
  "date" : "2019-10-11",
  "keywords" :[ "file ltx", "format file ltx", "apa itu file ltx", "file", "contoh ltx", "ekstensi file ltx", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - File Dokumen Lateks",
  "description":"Pelajari tentang format file LTX dan API yang dapat membuat dan membuka file LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Apa itu file LTX?

Catatan dengan ekstensi .ltx adalah dokumen bahasa markup berbasis buku yang dibuat dengan kerangka penyusunan huruf yang dikenal sebagai LaTex. Dalam sebagian besar kasus, ini digunakan untuk mengkarakterisasi pengaturan huruf untuk distribusi, surat, buku, dan rekaman komparatif lainnya di berbagai bidang. Desain catatan lateks meningkatkan laporan menggunakan perhitungan khusus, urutan pengaturan arsip, dan seluk-beluk terkecil. Prosesor lateks seperti TeXworks, Texmaker, LaTeX Editor, proTeXt, dan Notepad++ dapat digunakan untuk membuka dan mengedit file Tex.

## Format File LTX

Dokumen LATEX adalah catatan teks biasa yang dapat diubah dalam pengolah kata apa pun. Kerangka kerja penyusunan huruf Tex umumnya digunakan dalam komunitas ilmiah khususnya di bidang matematika, rekayasa perangkat lunak, aspek keuangan, desain, dan juga lainnya. Ini berisi banyak perintah yang biasanya dimulai dengan tanda baca miring (/id/) dan dikumpulkan dengan dukungan bergelombang. Keterangan/komentar dalam file LTX dimulai dan diakhiri dengan gambar dua kali lipat persen (%%). File LTX mirip dengan file [.tex](/id/page-description-language/tex/) dan [.latex](/id/word-processing/latex/) dan Anda akan sering menemukan dokumen lateks yang disimpan dalam format ini.

### Contoh LTX

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
