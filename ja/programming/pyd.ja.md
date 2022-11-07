---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD ファイル形式 - Python 動的モジュール
linktitle: PYD
description: "PYD ファイル形式と,PYD ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYD オプション番号

PYD ファイルは、実行時に他の Python コードで実行できる Python で記述されたダイナミック リンク ライブラリです。コードの再利用を促進し、アプリケーションを作成するためのモジュール アーキテクチャを提供する 1 つ以上の Python モジュールが含まれています。 PYD ファイルは、helloworld.pyd などの .pyd 拡張子で作成および保存できます。アプリケーション開発者は、import ステートメントを使用して、アプリケーションに PYD モジュールを含めることができます。 PYD ファイルは、Windows、Mac、および Linux OS で利用可能な Python Software Foundation Python で開くことができます。

## PYD ファイル形式 - 詳細情報

PYD ファイルは Python プログラミング言語で記述され、Python コードをコンパイルすることによって生成されます。

## PY と PYD ファイル形式の違い

[PY](/programming/py/) ファイルには、そのまま実行されるソース コードが含まれており、他の Python アプリケーションで再利用可能なコードとして含めることはできません。ただし、PYD ファイルは、Windows オペレーティング システムで使用される動的にリンクされたライブラリです。

## PYD ファイルの作成方法

PYD ファイルは、exmaple.pyd などの名前のモジュールを作成することで作成できます。このモジュールには、PyMod_example() などの 1 つ以上の関数の形式ですべての機能が含まれます。プログラムがこのライブラリをインクルードして呼び出す場合、モジュールをインポートすることで実行でき、関数 PyMod_example() が実行されます。

## 参照 ##

* [C/C++ での Python 拡張機能の作成](https://sebsauvage.net/python/mingw.html)
* [Python (プログラミング言語) - ウィキペディア](https://en.wikipedia.org/wiki/Python_(programming_language))

