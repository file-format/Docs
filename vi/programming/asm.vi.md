{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ASM - Định dạng tệp mã nguồn hợp ngữ",
  "description":"Tìm hiểu về định dạng tệp ASM và các API có thể tạo và mở tệp ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Tệp ASM là gì? ##

Tệp ASM là một chương trình được viết bằng ngôn ngữ lập trình cấp thấp được gọi là hợp ngữ. Nó chủ yếu được sử dụng để viết mã liên quan đến phần cứng, chẳng hạn như để lập trình bộ điều khiển vi mô. Chương trình được viết bằng cú pháp hợp ngữ đơn giản bao gồm các toán tử và toán hạng để thực hiện các hoạt động khác nhau. Các tệp ASM được viết và chỉnh sửa trong trình soạn thảo văn bản và được thực thi bằng chương trình trình biên dịch mã chương trình như HLA, MASM, FASM, NASM hoặc GAS.

## Định dạng tệp ASM

Các tệp ASM bao gồm một chuỗi các hoạt động được thực thi bởi trình biên dịch mã chương trình để tạo **mã đối tượng**. Mã đối tượng kết quả là một bản dịch của sự kết hợp của các chế độ ghi nhớ và địa chỉ thành các số tương đương của chúng.

### Ví dụ về định dạng tệp ASM

Sau đây là một ví dụ về ứng dụng **Hello World** cho kiến trúc x86.
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

## Tài liệu tham khảo ##

* [Ngôn ngữ hợp ngữ - theo Wikipedia](https://vi.wikipedia.org/wiki/Assembly_language)
* [Ngôn ngữ hợp ngữ - Cú pháp cơ bản](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

