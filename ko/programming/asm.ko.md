{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM 파일 형식 - 어셈블리 언어 소스 코드 파일 형식",
  "description":"ASM 파일을 생성하고 열 수 있는 ASM 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## .ASM 파일이란? ##

ASM 파일은 어셈블리 언어로 알려진 저수준 프로그래밍 언어로 작성된 프로그램입니다. 주로 마이크로 컨트롤러 프로그래밍과 같은 하드웨어 관련 코드를 작성하는 데 사용됩니다. 프로그램은 다른 작업을 수행하는 연산자와 피연산자를 포함하는 간단한 어셈블리 언어 구문을 사용하여 작성되었습니다. ASM 파일은 텍스트 편집기에서 작성 및 편집되며 HLA, MASM, FASM, NASM 또는 GAS와 같은 어셈블러 프로그램을 사용하여 실행됩니다.

## ASM 파일 형식

ASM 파일은 **객체 코드**를 생성하기 위해 어셈블러가 실행하는 일련의 작업으로 구성됩니다. 결과 개체 코드는 니모닉과 주소 지정 모드의 조합을 해당 수치로 변환한 것입니다.

### ASM 파일 형식 예

다음은 x86 아키텍처용 **Hello World** 애플리케이션의 예입니다.
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

## 참조 ##

* [어셈블리 언어 - Wikipedia 제공](https://en.wikipedia.org/wiki/Assembly_language)
* [어셈블리 언어 - 기본 구문](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

