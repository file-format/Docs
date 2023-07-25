{
  "date" : "2019-10-11",
  "keywords" :["乳胶文件","乳胶文件格式","什么是乳胶文件","文件","乳胶示例","乳胶文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Latex 文档文件",
  "description":"了解 LATEX 文件格式和可以创建和打开 LATEX 文件的 API。",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## 什么是 .LATEX 文件？

具有 .latex 扩展名的文件是使用称为 LaTex 的排版系统创建的基于文本的标记语言文件。在大多数情况下，它用于定义各种领域的出版物、信件、书籍和其他类似编目的排版。 Latex 文件格式使用专门的算法、用于格式化文档的命令以及最细微的细节来增强文档。 TeXworks、Texmaker、LaTeX Editor、proTeXt 和 Notepad++ 等 Latex 处理器可用于打开和编辑 Tex 文件。

## 乳胶文件格式

LATEX 文件是可以在任何文本编辑器中编辑的纯文本文件。 Tex排版系统在学术界被广泛使用，尤其是在数学、计算机科学、经济学、工程等领域。它由一组命令组成，通常以反斜杠开头并用花括号分组。 tex 文件中的注释以双百分号 (%%) 开始和结束。

### LATEX 示例

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
