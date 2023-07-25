{
  "date" : "2019-10-11",
  "keywords" :[ "ltx 파일", "ltx 파일 형식", "ltx 파일이란", "파일", "ltx 예제", "ltx 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - 라텍스 문서 파일",
  "description":"LTX 파일 형식과 LTX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## .LTX 파일이란?

.ltx 확장자를 가진 레코드는 LaTex로 알려진 조판 프레임워크로 만든 책 기반 마크업 언어 문서입니다. 대부분의 경우 배포판, 편지, 책 및 기타 다른 분야의 비교 녹음을 위한 조판을 특성화하는 데 사용됩니다. Latex 레코드 디자인은 특정 계산, 아카이브 정렬 순서 및 가장 작은 세부 사항을 활용하여 보고서를 업그레이드합니다. TeXworks, Texmaker, LaTeX Editor, proTeXt 및 Notepad++와 같은 라텍스 프로세서를 사용하여 Tex 레코드를 열고 변경할 수 있습니다.

## LTX 파일 형식

LATEX 문서는 모든 워드 프로세서에서 변경할 수 있는 일반 텍스트 레코드입니다. Tex 조판 프레임워크는 일반적으로 수학, 소프트웨어 엔지니어링, 금융 측면, 디자인 및 기타 분야의 학계에서 사용됩니다. 일반적으로 비스듬한 구두점(/ko/)으로 시작하고 물결 모양의 지지대와 함께 모인 명령 무리가 포함되어 있습니다. LTX 파일의 비고/코멘트는 이중 퍼센트 이미지(%%)로 시작하고 끝납니다. LTX 파일은 [.tex](/ko/page-description-language/tex/) 및 [.latex](/ko/word-processing/latex/) 파일과 유사하며 이러한 형식으로 저장된 라텍스 문서를 종종 찾을 수 있습니다.

### LTX 예

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
