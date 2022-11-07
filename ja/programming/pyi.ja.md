---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI ファイル形式 - Python インターフェイス定義
linktitle: PYI
description: "PYI ファイル形式と,PYI ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYI ファイルとは?

PYI ファイルは、インターフェースを実装するためのコード スタブ リファレンスを含む Python インターフェース定義ファイルです。各 Python モジュールは、通常の Python ファイルであるがメソッドが空の .pyi スタブとして表されます。 PYI ファイルの構文は、通常の Python モジュールの構文と同じです。空のメソッドの実装は、モジュールが作成された特定の目的を達成するためにエンド ユーザーに残されます。 PYI ファイルは、プログラムの完全な実装を含む [PY](/programming/py/) ファイルとは異なります。 PYI ファイルは、メモ帳、メモ帳++、Microsoft Visual Studio Code、JetBrains PyCharm などのテキスト エディターで開くことができます。

## PYI ファイル形式

PYI ファイルは、任意のテキスト エディターで開くことができるプレーン テキスト ファイルとして保存されます。 Python は、コードの実行時に型チェックを行うインタープリター言語です。このような場合、開発者がアプリケーションの作成中にモジュールの型を手動で定義および確認できるという点で、PYI ファイルは有益です。

## 参照 ##

* [インターフェース - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM インタープリター](https://github.com/interpreters/pym)

