{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM ファイル形式 - アセンブリ言語ソース コード ファイル形式",
  "description":"ASM ファイル形式と,ASM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## .ASM オプション番号##

ASMファイルは、アセンブリ言語として知られる低レベルのプログラミング言語で書かれたプログラムです。主に、マイクロコントローラのプログラミングなど、ハードウェア関連のコードを書くために使用されます。プログラムは、さまざまな操作を実行するための演算子とオペランドを含む単純なアセンブリ言語構文を使用して記述されます。 ASM ファイルは、テキスト エディターで作成および編集され、HLA、MASM、FASM、NASM、GAS などのアセンブラー プログラムを使用して実行されます。

## ASM ファイル形式

ASM ファイルは、**オブジェクト コード**を生成するためにアセンブラによって実行される一連の操作で構成されています。結果として得られるオブジェクト コードは、ニーモニックとアドレッシング モードの組み合わせを、それらに相当する数値に変換したものです。

### ASM ファイル形式の例

以下は、x86 アーキテクチャの **Hello World** アプリケーションの例です。
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

## 参照 ＃＃

* [アセンブリ言語 - ウィキペディアによる](https://en.wikipedia.org/wiki/Assembly_language)
* [アセンブリ言語 - 基本構文](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

