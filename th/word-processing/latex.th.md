{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ลาเท็กซ์", "รูปแบบไฟล์ลาเท็กซ์", "ไฟล์ลาเท็กซ์คืออะไร", "ไฟล์", "ตัวอย่างลาเท็กซ์", "นามสกุลไฟล์ลาเท็กซ์","ส่วนขยาย", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LATEX - ไฟล์เอกสารลาเท็กซ์",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LATEX และ API ที่สามารถสร้างและเปิดไฟล์ LATEX",
  "linktitle" : "LATEX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## ไฟล์ LATEX คืออะไร??

ไฟล์ที่มีนามสกุล .latex เป็นไฟล์ภาษามาร์กอัปแบบข้อความที่สร้างขึ้นด้วยระบบการเรียงพิมพ์ที่เรียกว่า LaTex ในกรณีส่วนใหญ่ ใช้เพื่อกำหนดการเรียงพิมพ์สำหรับสิ่งพิมพ์ จดหมาย หนังสือ และรายการอื่นๆ ที่คล้ายกันในหลากหลายสาขา รูปแบบไฟล์ลาเท็กซ์ช่วยปรับปรุงเอกสารโดยใช้อัลกอริทึมพิเศษ คำสั่งสำหรับการจัดรูปแบบของเอกสาร และรายละเอียดที่น้อยที่สุด สามารถใช้ตัวประมวลผลลาเท็กซ์ เช่น TeXworks, Texmaker, LaTeX Editor, proTeXt และ Notepad++ เพื่อเปิดและแก้ไขไฟล์ Tex

## รูปแบบไฟล์ LATEX

ไฟล์ LATEX เป็นไฟล์ข้อความล้วนที่สามารถแก้ไขได้ในโปรแกรมแก้ไขข้อความ ระบบการเรียงพิมพ์ข้อความถูกใช้อย่างแพร่หลายในวงวิชาการ โดยเฉพาะในสาขาคณิตศาสตร์ วิทยาการคอมพิวเตอร์ เศรษฐศาสตร์ วิศวกรรม และอื่นๆ ในทำนองเดียวกัน ประกอบด้วยชุดคำสั่งโดยทั่วไปที่ขึ้นต้นด้วยเครื่องหมายแบ็กสแลชและจัดกลุ่มด้วยวงเล็บปีกกา ความคิดเห็นในไฟล์ tex เริ่มต้นและสิ้นสุดด้วยสัญลักษณ์เปอร์เซ็นต์สองเท่า (%%)

### ตัวอย่างน้ำยางข้น

สามารถวางเนื้อหาต่อไปนี้ในไฟล์ข้อความเพื่อสร้างเอกสาร LaTex อย่างง่าย

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

ผลลัพธ์ของไฟล์คำสั่งด้านบนควรมีลักษณะดังนี้:

{{< figure src="../latex-example.png" alt="รูปแบบไฟล์ลาเท็กซ์" >}}

## อ้างอิง ##

* [TEX - Wikipedia](https://en.wikipedia.org/wiki/TeX)
* [ยาง](http://mally.stanford.edu/~sr/computing/latex-example.html)

