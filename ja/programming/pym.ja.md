---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM ファイル形式 - PYM マクロ プリプロセッサ ファイル
linktitle: PYM
description: "PYM ファイル形式と,PYM ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYM オプション番号

PYM ファイルは、Python プログラミング言語に基づくマクロ プリプロセッサ ファイルです。 VRVis Research によって開発され、マクロのショートカットを保存します。 PYM ファイルが Python インタープリターの前処理段階で解釈されると、これらのショートカットは全文の置換として展開されます。さらに、マクロ プリプロセッサで実行できる 3 番目のオプションの操作は、ファイル インクルードです。 PYM ファイルは、Notepad、Notepad++、Apple TextEdit、Linux の VI などのテキスト エディターで開くことができます。

## PYM ファイル形式

PYM ファイルはプレーン テキスト ファイルとしてディスクに保存されます。 PYM ファイルには、`#include` ディレクティブを使用して他のファイルを含めることもできます。

### PYM 構文

以下に示すように、PYM ステートメントは ""#begin python マーカーと "#end python" マーカーの間に含まれます。

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM マクロ展開

PYM マクロ展開は、<[ と ]> の 2 つのシーケンスで表されます。これらは特別な html タグで、行のどこにでも表示できます。ちょっとした PYM の例は次のとおりです。

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

これを PYM で実行した場合の出力は次のとおりです。

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## 参照 ##

* [PYM - Python ベースのマクロ プリプロセッサ](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM インタープリター](https://github.com/interpreters/pym)

