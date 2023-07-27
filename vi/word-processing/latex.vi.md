{
  "date" : "2019-10-11",
  "keywords" :[ "tệp latex", "định dạng tệp latex", "tệp latex là gì", "tệp", "ví dụ về latex", "phần mở rộng tệp latex","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - Tệp tài liệu latex",
  "description":"Tìm hiểu về định dạng tệp LATEX và API có thể tạo và mở tệp LATEX.",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Tập tin LATEX là gì?

Tệp có phần mở rộng .latex là tệp ngôn ngữ đánh dấu dựa trên văn bản được tạo bằng hệ thống sắp chữ được gọi là LaTex. Trong hầu hết các trường hợp, nó được sử dụng để xác định cách sắp chữ cho các ấn phẩm, thư từ, sách và các mục lục tương tự khác trong các lĩnh vực khác nhau. Định dạng tệp latex nâng cao tài liệu bằng các thuật toán chuyên biệt, các lệnh để định dạng tài liệu và các chi tiết nhỏ nhất. Có thể sử dụng các bộ xử lý latex như TeXworks, Texmaker, LaTeX Editor, proTeXt và Notepad++ để mở và chỉnh sửa các tệp Tex.

## Định dạng tệp LATEX

Các tệp LATEX là các tệp văn bản thuần túy có thể được chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào. Hệ thống sắp chữ Tex được sử dụng rộng rãi trong giới học thuật, đặc biệt là trong các lĩnh vực toán học, khoa học máy tính, kinh tế, kỹ thuật và các lĩnh vực tương tự khác. Nó bao gồm một tập hợp các lệnh thường bắt đầu bằng dấu gạch chéo ngược và được nhóm bằng dấu ngoặc nhọn. Nhận xét trong tệp tex bắt đầu và kết thúc bằng ký hiệu phần trăm kép (%%).

### Ví dụ LATEX

Nội dung sau đây có thể được dán vào một tệp văn bản để tạo một tài liệu LaTex đơn giản.

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

Đầu ra của tệp lệnh ở trên sẽ trông như thế này:

{{< figure src="../latex-example.png" alt="Định dạng tệp latex" >}}

## Người giới thiệu ##

* [TEX - Wikipedia](https://vi.wikipedia.org/wiki/TeX)
