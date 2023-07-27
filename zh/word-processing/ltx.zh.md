{
  "date" : "2019-10-11",
  "keywords" :["ltx 文件","ltx 文件格式","什么是 ltx 文件","文件","ltx 示例","ltx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - 乳胶文档文件",
  "description":"了解 LTX 文件格式和可以创建和打开 LTX 文件的 API。",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## 什么是一 .ltx 文件？

带有 .ltx 扩展名的记录是使用称为 LaTex 的排版框架制作的基于书籍的标记语言文档。在很大一部分案例中，它被用来表征不同领域的分布、信件、书籍和其他比较记录的排版。 Latex 记录设计利用特定的计算、归档的排列顺序和最细微的细节来升级报告。 Latex 处理器，例如 TeXworks、Texmaker、LaTeX Editor、proTeXt 和 Notepad++ 可用于打开和更改 Tex 记录。

## LTX 文件格式

LATEX 文档是可以在任何文字处理器中更改的纯文本记录。 Tex 排版框架通常用于学术社区，特别是在数学、软件工程、金融方面、设计等领域。它包含一堆命令，通常以斜标点线 (/zh/) 开头，并以波浪形支撑聚集在一起。 LTX 文件中的备注/注释以两倍百分比图像 (%%) 开头和结尾。 LTX 文件类似于 [.tex](/zh/page-description-language/tex/) 和 [.latex](/zh/word-processing/latex/) 文件，您经常会发现以这些格式保存的 Latex 文档。

### LTX 示例

可以将以下内容粘贴到文本文件中以创建简单的 LaTex 文档。

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

上述命令文件的输出应如下所示：

{{< figure src="../latex-example.png" alt="乳胶文件格式" >}}

## 参考 ＃＃

* [TEX - 维基百科](https://en.wikipedia.org/wiki/TeX)
