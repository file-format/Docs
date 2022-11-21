{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ ltx", "รูปแบบไฟล์ ltx", "ไฟล์ ltx คืออะไร", "ไฟล์", "ตัวอย่าง ltx", "นามสกุลไฟล์ ltx", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LTX - ไฟล์เอกสารลาเท็กซ์",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LTX และ API ที่สามารถสร้างและเปิดไฟล์ LTX",
  "linktitle" : "LTX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-05-18"
}

## ไฟล์ LTX คืออะไร??

บันทึกที่มีนามสกุล .ltx เป็นเอกสารภาษามาร์กอัปแบบหนังสือที่สร้างด้วยเฟรมเวิร์กการเรียงพิมพ์ที่เรียกว่า LaTex ในกรณีส่วนใหญ่ จะใช้เพื่อแสดงลักษณะการเรียงพิมพ์สำหรับการกระจาย จดหมาย หนังสือ และบันทึกเปรียบเทียบอื่นๆ ในสาขาต่างๆ การออกแบบบันทึกแบบลาเท็กซ์ช่วยยกระดับรายงานโดยใช้การคำนวณเฉพาะ คำสั่งสำหรับการจัดเรียงไฟล์เก็บถาวร และรายละเอียดปลีกย่อยที่เล็กที่สุด สามารถใช้ตัวประมวลผลลาเท็กซ์ เช่น TeXworks, Texmaker, LaTeX Editor, proTeXt และ Notepad++ เพื่อเปิดและแก้ไขบันทึก Tex

## รูปแบบไฟล์ LTX

เอกสาร LATEX เป็นบันทึกข้อความธรรมดาที่สามารถแก้ไขได้ในโปรแกรมประมวลผลคำใดๆ โดยทั่วไปกรอบการเรียงพิมพ์ข้อความจะใช้ในชุมชนนักวิชาการโดยเฉพาะในสาขาคณิตศาสตร์ วิศวกรรมซอฟต์แวร์ ด้านการเงิน การออกแบบ และอื่นๆ ในทำนองเดียวกัน ประกอบด้วยคำสั่งมากมายที่ปกติจะขึ้นต้นด้วยเครื่องหมายวรรคตอนเฉียง (/th/) และรวบรวมด้วยการสนับสนุนแบบหยัก ข้อสังเกต/ความคิดเห็นในไฟล์ LTX เริ่มต้นและลงท้ายด้วยภาพสองเท่า (%%) ไฟล์ LTX คล้ายกับไฟล์ [.tex](/th/page-description-language/tex/) และ [.latex](/th/word-processing/latex/) และคุณจะพบเอกสารลาเท็กซ์ที่บันทึกในรูปแบบเหล่านี้อยู่บ่อยครั้ง

### ตัวอย่าง LTX

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

