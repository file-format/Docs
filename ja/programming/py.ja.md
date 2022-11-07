---
date: 2019-10-11
keywords: py, python, .py, py ファイル形式, py ファイルの開き方, py ファイルの実行方法, python ファイルの実行方法, python の実行方法
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY ファイル形式
linktitle: PY
description: "PY ファイル形式と,PY ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## .PY オプション番号##

拡張子が .py のファイルには、Python ソース コードが含まれています。 Python 言語は、今日では非常に有名な言語になりました。システム スクリプト、Web およびソフトウェア開発、数学に使用できます。 Python はクロスプラットフォームの互換性をサポートしています。これは、Python で開発されたアプリケーションが、Windows、MAC、Linux、Raspberry Pi などのさまざまなプラットフォームで動作できることを意味します。Python は、英語に似たシンプルで読みやすい構文を提供します。開発者は、Python コードを数行書くだけで、適切なソフトウェア アプリケーションを作成できます。 Python はインタープリター システム上で実行されるため、コードを記述したらすぐに実行できるため、プロトタイピングに非常に適しています。

## 簡単な歴史 ##

Python は、1980 年代後半に Guido van Rossum によって ABC プログラミング言語の後継として考案されました。その実装は、1989 年 12 月に Van Rossum を唯一の主任開発者として開始しました。彼は 2018 年 7 月 12 日まで Python に取り組んでいました。2019 年 1 月、アクティブな Python コア開発者は、Nick Coghlan、Brett Cannon、Carol Willing、Barry Warsaw、Van Rossum で構成される 5 人のメンバーで構成される「Steering Council」を選出し、プロジェクトを率いました。

### バージョン ###

- Python 2.0 は 2000 年 10 月 16 日にリリースされました。
- Python 3.0 は 2008 年 12 月 3 日にリリースされました。

## py ファイルの実行方法 ##

インストールされている Python のバージョンを確認するには、次のコマンドを使用できます。

```cmd
python --version
```

これにより、コンソールにバージョンが出力されます

```cmd
Python 3.7.4
```

Python がマシンにインストールされていない場合は、[python.org](https://www.python.org/) にアクセスして、関連するオペレーティング システム用の Python をダウンロードしてインストールできます。

Python スクリプトを実行するには、次のコマンドを使用できます。

```cmd
python helloworld.py
```

*helloworld.py* は、次のコードを含むスクリプト ファイルです。

```py
print("Hello World from Python")
```

これにより、コンソール ウィンドウに次のように出力されます。

```cmd
Hello World from Python
```

注: IDE を使用している場合は、画面にボタンが表示されるか、Python を実行するためのさまざまなキーボード ショートカットが提供されます。たとえば、再生ボタンは、Python スクリプトを実行できる PyCharm のエディターでガターに表示されます。

## PY ファイル形式 ##

Python は読みやすさを考慮して設計されており、英語や数学と類似しています。 Python では、他の言語で使用されるセミコロンや括弧とは対照的に、改行を使用して完全なコマンドを示します。スコープ、ループ、および関数について、Python は、他の言語で使用される中括弧とは対照的に、インデントと空白に依存しています。

### 構文 ###

以下は、Python 構文の例です。

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## 参照 ##

- [Python (プログラミング言語) - ウィキペディア](https://en.wikipedia.org/wiki/Python_(programming_language))

