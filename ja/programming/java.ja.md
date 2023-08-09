---
date: 2019-10-11
keywords: java,.java,java ファイル形式,java ファイルの開き方,java ファイルの実行方法,java ファイル,java サンプル コード
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java ファイル形式
linktitle: Java
description: "Java ファイル形式と,Java ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Java ファイルとは何ですか? ##
Java ソース コードを含み、.java ファイル拡張子で保存されたファイルは、Java ファイルと呼ばれます。 Java は、ゲーム、モバイル、Web、およびデスクトップ アプリケーションの開発に最も広く使用されているテクノロジの 1 つです。 Java はプラットフォームに依存しないため、Windows、Mac、Linux、Raspberry Pi などで問題なく動作します。Java は C# や C++ に非常に似ているため、これらの言語を簡単に切り替えることができます。

## 簡単な歴史 ##

Java プロジェクトは、1991 年 6 月に James Gosling、Mike Sheridan、および Patrick Naughton によって開始されました。 Java は当初、Oak という名前でした。後に Green に改名され、最終的に Java に改名されました。 James Gosling は、C/C++ に似た構文で Java を設計しました。 Java の最初の公開バージョンは、1996 年に Sun Microsystems によってリリースされました。 Java が急速に普及する原因となったすべての一般的なシステムで実行できます。 1998 年 12 月の Java 2 のリリースにより、さまざまなタイプのプラットフォーム用の複数の構成が構築されました。バージョンは次のとおりでした

- J2EE (Java EE): エンタープライズ ソリューション向け
- J2ME (Java ME): モバイルアプリケーション向け
- J2SE (Java SE): デスクトップアプリケーション用

2006 年 11 月 19 日、Java 仮想マシン (JVM) が Sun によって無料のオープンソース ソフトウェアとしてリリースされました。 2009 年から 2010 年にかけて Oracle Corporation が Sun Microsystems を買収した後、James Gosling は 2010 年 4 月 2 日に Oracle を辞任しました。

## Java コードを実行/実行する方法 ##

Java コードを実行するには、最初にコンパイルする必要があります。そのためには、Java SDK が必要です。 Java SDK は、Java コードをバイトコード クラス ファイルにコンパイルします。 Eclipse や IntelliJ Idea などの IDE には、Java コードをコンパイルして実行するためのコード補完と使いやすいインターフェイスを提供することで、Java ファイルの操作を容易にするものがあります。

## Java ファイル形式 ##

Java の構文は C および C++ の影響を強く受けましたが、C++ とは異なり、Java はほとんどオブジェクト指向言語として構築されました。 Java では、すべてのコードがクラス内に記述され、すべてのデータ項目がオブジェクトです。 C++ とは対照的に、Java は演算子のオーバーロードや多重継承をサポートしていません。

### Java サンプルコード ###

以下は、Java 構文の例です。

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
上記のコードでは、 **public** キーワードがアクセス修飾子を示しています。このクラスは、クラス階層外のクラスからアクセスできることを示しています。アクセス修飾子は **protected** (同じパッケージ内でアクセス可能) または **private** (メソッドは同じクラスからのみアクセス可能) にすることもできます。メソッドの前の **static** は、クラスの特定のインスタンスなしでメソッドを呼び出すことができることを示します。 **void** は、メソッドが何も返さないことを示します。文字列をコンソールに出力します。 System.out.println コマンドを使用します。このコマンドでは、*System* クラスに静的フィールド *out* があり、これは *println* メソッドを含む *PrintStream* クラスのインスタンスです。

Java ファイルのファイル名は、クラス名と同じにする必要があります。したがって、コード例の Java ファイルは *ExampleApp.java* という名前になります。

## 参照 ##

- [Java (プログラミング言語) - ウィキペディア](https://en.wikipedia.org/wiki/Java_(programming_language))

