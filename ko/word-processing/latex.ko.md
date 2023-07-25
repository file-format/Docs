{
  "date" : "2019-10-11",
  "keywords" :[ "라텍스 파일", "라텍스 파일 형식", "라텍스 파일이란", "파일", "라텍스 예", "라텍스 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - 라텍스 문서 파일",
  "description":"LATEX 파일 형식과 LATEX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## .LATEX 파일이란?

.latex 확장자를 가진 파일은 LaTex로 알려진 조판 시스템으로 만든 텍스트 기반 마크업 언어 파일입니다. 대부분의 경우 다양한 분야의 출판물, 편지, 책 및 기타 유사한 목록에 대한 조판을 정의하는 데 사용됩니다. Latex 파일 형식은 특수 알고리즘, 문서 형식 지정 명령 및 가장 작은 세부 사항을 사용하여 문서를 향상시킵니다. TeXworks, Texmaker, LaTeX Editor, proTeXt 및 Notepad++와 같은 Latex 프로세서를 사용하여 Tex 파일을 열고 편집할 수 있습니다.

## LATEX 파일 형식

LATEX 파일은 모든 텍스트 편집기에서 편집할 수 있는 일반 텍스트 파일입니다. Tex 조판 시스템은 특히 수학, 컴퓨터 과학, 경제, 공학 및 이와 유사한 분야의 학계에서 널리 사용됩니다. 일반적으로 백슬래시로 시작하고 중괄호로 묶인 일련의 명령으로 구성됩니다. tex 파일의 주석은 이중 퍼센트 기호(%%)로 시작하고 끝납니다.

### LATEX 예

다음 내용을 텍스트 파일에 붙여넣어 간단한 LaTex 문서를 만들 수 있습니다.

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

위 명령 파일의 출력은 다음과 같아야 합니다.

{{< figure src="../latex-example.png" alt="라텍스 파일 형식" >}}

## 참조 ##

* [TEX - 위키백과](https://en.wikipedia.org/wiki/TeX)
