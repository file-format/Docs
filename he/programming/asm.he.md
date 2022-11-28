{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ ASM - פורמט קובץ קוד מקור של שפת Assembly",
  "description":"למד על פורמט קובץ ASM וממשקי API שיכולים ליצור ולפתוח קובצי ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## מהו קובץ ASM? ##

קובץ ASM הוא תוכנית שנכתבה בשפת התכנות ברמה נמוכה המכונה שפת assembly. הוא משמש בעיקר לכתיבת קוד הקשור לחומרה כגון לתכנות מיקרו-בקרים. התוכנית נכתבת באמצעות תחביר שפת assembly פשוט הכולל אופרטורים ואופרנדים לביצוע פעולות שונות. קבצי ASM נכתבים ונערכים בעורכי טקסט ומבוצעים באמצעות תוכנת אסמבלר כגון HLA, MASM, FASM, NASM או GAS.

## פורמט קובץ ASM

קבצי ASM מורכבים מרצף של פעולות שמבוצעות על ידי אסמבלר כדי ליצור **קוד אובייקט**. קוד האובייקט המתקבל הוא תרגום של שילובים של אמנויות ומצבי הפנייה למקבילות המספריות שלהם.

### דוגמה לפורמט קובץ ASM

להלן דוגמה ליישום **Hello World** עבור ארכיטקטורת x86.
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

## התייחסות ##

* [שפת האסיפה - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Assembly_language)
* [שפת Assembly - תחביר בסיסי](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

