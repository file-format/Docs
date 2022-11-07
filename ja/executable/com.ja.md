{
  "date" : "2021-06-29",
  "keywords" :[ "com ファイル", "com ファイルとは", "ファイル", "com の例", "com ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"COM ファイル形式と,COM ファイルを作成して開くことができる API について学びます。",
  "title" :"COM - DOS コマンド ファイル形式",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## COM ファイルとは?
COM ファイルは、一連のコマンドまたは命令を実行するために使用されます。 COM ファイルは、Windows または MS-DOS から実行できる実行可能プログラムで構成されています。 EXE ファイルと同様に、COM ファイルもバイナリ形式で保存されますが、ヘッダーやメタデータがなく、最大サイズが約 64 KB であるため、EXE ファイルとは異なります。 COM ファイルを 32 ビット システムで初めて実行すると、NT 仮想 DOS マシン (NTVDM) コンポーネントをインストールするように求められます。 COM ファイルは、MS-DOS 環境をサポートする仮想マシンを使用して、64 ビット バージョンの Microsoft Windows で実行できます。

## COM ファイル形式
COM ファイル形式は、Microsoft Windows または MS-DOS で使用されるバイナリ実行形式です。その構造は一連の命令だけで構成されています。ヘッダーがなく、標準のメタデータが含まれていません。すべてのデータとコードを 1 つのセグメントにのみ格納し、バイナリのサイズは最大 64KB です。このファイル形式は、再実行しようとしても再配置されません。そのため、オペレーティング システムは事前に設定されたアドレスにそれをロードします。さらに、両方のオペレーティング システムで実行する COM ファイルを **ファット バイナリ**の形式で作成することもできます。命令レベルでの実際の互換性はありません。エントリ ポイントの命令は、機能が同じであるが両方のオペレーティング システムで異なるように選択され、プログラムを実行し、使用中のオペレーティング システムのセクションにジャンプします。基本的には、1 つのファイルで同じ手順を実行する 2 つの異なるプログラムであり、その前に使用するプログラムを選択するコードが続きます。
### COM ファイルの例
COM ファイルを実行すると、命令は最初のバイトから読み取られ、最後の命令が見つかるまで連続して実行されます。 ASM コードの例を次に示します。

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## 参考文献

* [COM ファイル - ウィキペディアによる](https://en.wikipedia.org/wiki/COM_file)

