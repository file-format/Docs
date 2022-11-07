{
  "date" : "2019-10-11",
  "keywords" :[ "latex ファイル", "latex ファイル形式", "latex ファイルとは", "ファイル", "latex の例", "latex ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - ラテックス文書ファイル",
  "description":"LATEX ファイル形式と,LATEX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## LATEX ファイルとは?

拡張子が .latex のファイルは、LaTex として知られる植字システムで作成されたテキストベースのマークアップ言語ファイルです。ほとんどの場合、出版物、手紙、本、およびさまざまな分野の他の同様のカタログの組版を定義するために使用されます。 Latex ファイル形式は、特殊なアルゴリズム、ドキュメントの書式設定のためのコマンド、および最も細かい詳細を使用して、ドキュメントを強化します。 TeXworks、Texmaker、LaTeX Editor、proTeXt、Notepad++ などの Latex プロセッサを使用して、Tex ファイルを開いて編集できます。

## LATEX ファイル形式

LATEX ファイルは、任意のテキスト エディターで編集できるプレーン テキスト ファイルです。 Tex 植字システムは、特に数学、コンピューター サイエンス、経済学、工学などの分野で、学界で広く使用されています。通常はバックスラッシュで始まり、中括弧でグループ化された一連のコマンドで構成されます。 tex ファイル内のコメントは、2 つのパーセント記号 (%%) で始まり、終わります。

### LATEX の例

次のコンテンツをテキスト ファイルに貼り付けて、簡単な LaTex ドキュメントを作成できます。

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

上記のコマンド ファイルの出力は次のようになります。

{{< figure src="../latex-example.png" alt="Latex ファイル形式" >}}

## 参照 ##

* [TEX - ウィキペディア](https://en.wikipedia.org/wiki/TeX)
* [ラテックス](http://mally.stanford.edu/~sr/computing/latex-example.html)

