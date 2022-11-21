{
  "date" : "2019-10-11",
  "keywords" :[ "ltx dosyası", "ltx dosya formatı", "ltx dosyası nedir", "dosya", "ltx örneği", "ltx dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Lateks Belge Dosyası",
  "description":"LTX dosya formatı ve LTX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## LTX dosyası nedir?

.ltx uzantılı bir kayıt, LaTex olarak bilinen dizgi çerçevesi ile hazırlanmış, kitap tabanlı bir biçimlendirme dili belgesidir. Vakaların büyük bir bölümünde, farklı alanlardaki dağıtımlar, mektuplar, kitaplar ve diğer karşılaştırmalı kayıtlar için dizgileri karakterize etmek için kullanılır. Lateks kayıt tasarımı, belirli hesaplamalar, arşiv düzenleme siparişleri ve en küçük incelikleri kullanarak raporu yükseltir. TeXworks, Texmaker, LaTeX Editor, proTeXt ve Notepad++ gibi lateks işlemciler, Tex kayıtlarını açmak ve değiştirmek için kullanılabilir.

## LTX Dosya Biçimi

LATEX belgeleri, herhangi bir kelime işlemcide değiştirilebilen düz metin kayıtlarıdır. Metin dizgi çerçevesi genellikle bilimsel toplulukta, özellikle matematik, yazılım mühendisliği, finansal yönler, tasarım ve benzer şekilde diğerleri alanlarında kullanılır. Normalde eğik bir noktalama işaretiyle (/tr/) başlayan ve dalgalı desteklerle toplanmış bir dizi komut içerir. Bir LTX dosyasındaki açıklamalar/yorumlar, yüzde iki kat görüntü (%%) ile başlar ve biter. LTX dosyaları, [.tex](/tr/page-description-language/tex/) ve [.latex](/tr/word-processing/latex/) dosyasına benzer ve genellikle bu biçimlerde kaydedilmiş lateks belgeleri bulacaksınız.

### LTX Örneği

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
* [Lateks](http://mally.stanford.edu/~sr/computing/latex-example.html)

