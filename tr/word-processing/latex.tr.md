{
  "date" : "2019-10-11",
  "keywords" :[ "lateks dosyası", "lateks dosya biçimi", "lateks dosyası nedir", "dosya", "lateks örneği", "lateks dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Lateks Belge Dosyası",
  "description":"LATEX dosya formatı ve LATEX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## LATEX dosyası nedir?

.latex uzantılı bir dosya, LaTex olarak bilinen dizgi sistemiyle oluşturulan metin tabanlı bir biçimlendirme dili dosyasıdır. Çoğu durumda, çeşitli alanlarda yayınlar, mektuplar, kitaplar ve diğer benzer kataloglama için dizgileri tanımlamak için kullanılır. Lateks dosya biçimi, özel algoritmalar, belgenin biçimlendirilmesi için komutlar ve en küçük ayrıntıları kullanarak belgeyi geliştirir. TeXworks, Texmaker, LaTeX Editor, proTeXt ve Notepad++ gibi lateks işlemciler, Tex dosyalarını açmak ve düzenlemek için kullanılabilir.

## LATEX Dosya Biçimi

LATEX dosyaları, herhangi bir metin düzenleyicide düzenlenebilen düz metin dosyalarıdır. Tex dizgi sistemi akademide özellikle matematik, bilgisayar bilimi, ekonomi, mühendislik ve benzeri alanlarda yaygın olarak kullanılmaktadır. Genellikle bir ters eğik çizgi ile başlayan ve kaşlı ayraçlarla gruplandırılmış bir dizi komuttan oluşur. Bir tex dosyasındaki yorumlar çift yüzde sembolleriyle (%%) başlar ve biter.

### LATEX Örneği

Aşağıdaki içerik, basit bir LaTex belgesi oluşturmak için bir metin dosyasına yapıştırılabilir.

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

Yukarıdaki komut dosyasının çıktısı şöyle görünmelidir:

{{< figure src="../latex-example.png" alt="Lateks Dosya Biçimi" >}}

## Referanslar ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
