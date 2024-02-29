{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فرمت فایل ASM - فرمت فایل کد منبع زبان اسمبلی",
  "description":"با فرمت فایل ASM و APIهایی که می توانند فایل های ASM را ایجاد و باز کنند آشنا شوید.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-fa",
      "parent" : "programming"
}
}،
  "lastmod" : "2022-04-03"
}

## فایل ASM چیست؟ ##

یک فایل ASM برنامه ای است که به زبان برنامه نویسی سطح پایین که به زبان اسمبلی معروف است نوشته شده است. در درجه اول برای نوشتن کدهای مرتبط با سخت افزار مانند برنامه نویسی میکروکنترلرها استفاده می شود. برنامه با استفاده از دستور زبان اسمبلی ساده که شامل عملگرها و عملوندها برای انجام عملیات های مختلف است، نوشته شده است. فایل های ASM در ویرایشگرهای متن نوشته و ویرایش می شوند و با استفاده از یک برنامه اسمبلر مانند HLA، MASM، FASM، NASM یا GAS اجرا می شوند.

## فرمت فایل ASM

فایل‌های ASM شامل دنباله‌ای از عملیات هستند که توسط اسمبلر برای تولید **کد شی** اجرا می‌شوند. کد شی حاصل ترجمه‌ای از ترکیب‌های یادگاری و حالت‌های آدرس‌دهی به معادل‌های عددی آن‌ها است.

### نمونه فرمت فایل ASM

در زیر نمونه ای از اپلیکیشن **Hello World** برای معماری x86 آورده شده است.
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

## ارجاع ##

* [Assembly Language - توسط ویکی پدیا](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


