{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ ASM - รูปแบบไฟล์ซอร์สโค้ดภาษาแอสเซมบลี",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ASM และ API ที่สามารถสร้างและเปิดไฟล์ ASM",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## ไฟล์ ASM คืออะไร?? ##

ไฟล์ ASM เป็นโปรแกรมที่เขียนด้วยภาษาโปรแกรมระดับต่ำที่เรียกว่าภาษาแอสเซมบลี ส่วนใหญ่จะใช้สำหรับเขียนโค้ดที่เกี่ยวข้องกับฮาร์ดแวร์ เช่น สำหรับการเขียนโปรแกรมไมโครคอนโทรลเลอร์ โปรแกรมเขียนขึ้นโดยใช้ไวยากรณ์ภาษาแอสเซมบลีอย่างง่ายที่มีตัวดำเนินการและตัวถูกดำเนินการเพื่อดำเนินการต่างๆ ไฟล์ ASM เขียนและแก้ไขในโปรแกรมแก้ไขข้อความและดำเนินการโดยใช้โปรแกรมแอสเซมเบลอร์ เช่น HLA, MASM, FASM, NASM หรือ GAS

## รูปแบบไฟล์ ASM

ไฟล์ ASM ประกอบด้วยลำดับของการดำเนินการที่ดำเนินการโดยแอสเซมเบลอร์เพื่อสร้าง **รหัสวัตถุ** รหัสอ็อบเจกต์ที่เป็นผลลัพธ์คือการแปลการรวมกันของตัวช่วยจำและโหมดการระบุที่อยู่ให้เป็นตัวเลขที่เทียบเท่ากัน

### ตัวอย่างรูปแบบไฟล์ ASM

ต่อไปนี้คือตัวอย่างแอปพลิเคชัน **Hello World** สำหรับสถาปัตยกรรม x86
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

## อ้างอิง ##

* [ภาษาแอสเซมบลี - โดยวิกิพีเดีย](https://en.wikipedia.org/wiki/Assembly_language)
* [ภาษาแอสเซมบลี - ไวยากรณ์พื้นฐาน](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

