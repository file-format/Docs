{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف ASM - تنسيق ملف رمز مصدر لغة التجميع" ,
  "description":"تعرف على تنسيق ملف ASM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASM وفتحها." ,
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-04-03"
}

## ما هو ملف ASM؟ ##

ملف ASM هو برنامج مكتوب بلغة البرمجة منخفضة المستوى والمعروفة باسم لغة التجميع. يتم استخدامه بشكل أساسي لكتابة التعليمات البرمجية المتعلقة بالأجهزة مثل برمجة وحدات التحكم الصغيرة. تمت كتابة البرنامج باستخدام بناء جملة لغة تجميع بسيط يتضمن المشغلين والمعاملات لتنفيذ عمليات مختلفة. تتم كتابة ملفات ASM وتحريرها في برامج تحرير النصوص ويتم تنفيذها باستخدام برنامج مجمع مثل HLA أو MASM أو FASM أو NASM أو GAS.

## تنسيق ملف ASM

تتكون ملفات ASM من سلسلة من العمليات التي يتم تنفيذها بواسطة المجمّع لإنشاء ** رمز كائن **. رمز الكائن الناتج هو ترجمة مجموعات من فن الإستذكار وأنماط العنونة إلى معادلاتها العددية.

### مثال على تنسيق ملف ASM

فيما يلي مثال على تطبيق ** Hello World ** لمعمارية x86.
```
global  go
extern  _ExitProcess@4
extern  _GetStdHandle@4
extern  _WriteConsoleA@20

section .data
msg:    db      'Hello, World', 10
handle: db      0
written:
db      0

section .text
go:
; handle = GetStdHandle(-11)
push    dword -11
call    _GetStdHandle@4
mov     [handle], eax

; WriteConsole(handle, &msg[0], 13, &written, 0)
push    dword 0
push    written
push    dword 13
push    msg
push    dword [handle]
call    _WriteConsoleA@20

; ExitProcess(0)
push    dword 0
call    _ExitProcess@4
```

## المرجعي ##

* [لغة التجميع - بواسطة ويكيبيديا](https://en.wikipedia.org/wiki/Assembly_language)
* [لغة التجميع - التركيب الأساسي](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

