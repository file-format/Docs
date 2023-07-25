{
  "date" : "2019-10-11",
  "keywords" :[ "tệp ltx", "định dạng tệp ltx", "tệp ltx là gì", "tệp", "ví dụ ltx", "phần mở rộng tệp ltx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - Tệp tài liệu latex",
  "description":"Tìm hiểu về định dạng tệp LTX và các API có thể tạo và mở tệp LTX.",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## Tệp LTX là gì?

Bản ghi có phần mở rộng .ltx là một tài liệu ngôn ngữ đánh dấu dựa trên sách được tạo bằng khung sắp chữ được gọi là LaTex. Trong phần lớn các trường hợp, nó được sử dụng để mô tả cách sắp chữ cho các bản phân phối, thư từ, sách và bản ghi so sánh khác trong các lĩnh vực khác nhau. Thiết kế bản ghi latex nâng cấp báo cáo bằng cách sử dụng các tính toán cụ thể, yêu cầu sắp xếp kho lưu trữ và các chi tiết nhỏ nhất. Bộ xử lý latex, chẳng hạn như TeXworks, Texmaker, LaTeX Editor, proTeXt và Notepad++ có thể được sử dụng để mở và chỉnh sửa các bản ghi Tex.

## Định dạng tệp LTX

Các tài liệu LATEX là các bản ghi văn bản thuần túy có thể được thay đổi trong bất kỳ trình xử lý văn bản nào. Khung sắp chữ Tex thường được sử dụng trong cộng đồng học thuật, đặc biệt là trong các lĩnh vực toán học, công nghệ phần mềm, khía cạnh tài chính, thiết kế, v.v. Nó chứa một loạt các lệnh thường bắt đầu bằng dấu chấm câu xiên (/vi/) và được tập hợp lại bằng các giá đỡ lượn sóng. Nhận xét/nhận xét trong tệp LTX bắt đầu và kết thúc bằng hình ảnh phần trăm gấp đôi (%%). Các tệp LTX tương tự như tệp [.tex](/vi/page-description-language/tex/) và [.latex](/vi/word-processing/latex/) và bạn sẽ thường tìm thấy các tài liệu latex được lưu ở các định dạng này.

### Ví dụ LTX

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
