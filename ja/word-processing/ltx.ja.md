{
  "date" : "2019-10-11",
  "keywords" :["ltxファイル","ltxファイル形式","ltxファイルとは","ファイル","ltx例","ltxファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Latex ドキュメント ファイル",
  "description":"LTX ファイル形式と,LTX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## .LTX ファイルとは?

拡張子が .ltx のレコードは、LaTex として知られる組版フレームワークで作成された書籍ベースのマークアップ言語ドキュメントです。多くの場合、配布物、手紙、書籍、およびさまざまな分野でのその他の比較記録の組版を特徴付けるために使用されます。ラテックス レコード デザインは、特定の計算、アーカイブの配置順序、および微妙な点を利用してレポートをアップグレードします。 TeXworks、Texmaker、LaTeX Editor、proTeXt、Notepad++ などの Latex プロセッサを使用して、Tex レコードを開いたり変更したりできます。

## LTX ファイル形式

LATEX 文書は、任意のワード プロセッサで変更できるプレーン テキスト レコードです。 Tex 組版フレームワークは、特に数学、ソフトウェア エンジニアリング、財務面、設計などの分野の学術コミュニティで一般的に利用されています。通常は斜めの句読点 (/) で始まり、波状のサポートで集められた一連のコマンドが含まれています。 LTX ファイルの注釈/コメントは、2 倍のパーセント画像 (%%) で始まり、終わります。 LTX ファイルは [.tex](/page-description-language/tex/) および [.latex](/word-processing/latex/) ファイルに似ており、これらの形式で保存された latex ドキュメントをよく見かけます。

### LTX の例

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
