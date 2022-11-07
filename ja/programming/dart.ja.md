---
date: 2019-10-11
keywords: dart,.dart,dart ファイル形式,dart ファイル,dart ファイルの実行方法,.dart 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dartファイル形式
linktitle: Dart
description: "Dart ファイル形式と,Dart ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## .Dart ファイルとは? ##

Dartファイルには、モバイル、デスクトップ、ウェブ、IoT（モノのインターネット）などのアプリを構築するために使用される、Googleが開発したクライアント最適化プログラミング言語であるDartプログラミング言語のソースコードが含まれています。Dartはオブジェクト指向言語ですDart は、JavaScript またはネイティブ コードのいずれかにコンパイルできます。 Dart ファイルは、JavaScript ファイルを実行するのと同じように、有名な Web ブラウザーで実行できます。 Dart SDK に付属する Dart 仮想マシンと呼ばれるコマンド ライン ツールを使用して、Dart ファイルをコンパイルおよび実行することもできます。

## 簡単な歴史 ##

Dart プロジェクトは、Lars Bak と Kasper Lund によって設立され、最初のバージョンは 2013 年 11 月 14 日にリリースされました。当初、Dart は、Google Chrome に Dart VM を含める計画のために Web の断片化について批判されました。これらの計画は破棄され、Dart は 2015 年のバージョン 1.9 のリリースで JavaScript へのコンパイルに集中しました。

Dart 2.0 は 2018 年 8 月にリリースされ、Dart コードをネイティブの Linux、Windows、macOS プラットフォームにコンパイルする dart2native 拡張機能が導入されました。この拡張機能により、Dart SDK がこれらのプラットフォームで Dart アプリを実行する必要がないため、自己完結型の実行可能ファイルが有効になりました。この拡張機能は Flutter とも統合されているため、クロスプラットフォーム アプリを作成できます。

ECMA は、2014 年 7 月に第 1 版、2014 年 12 月に第 2 版で Dart を標準化しました。


## Dart コードの実行/実行方法 ##

Dart コードは次の方法で実行できます。

- **JavaScript としてコンパイル**:</br> Dart コードは、dart2js コンパイラを使用して JavaScript にコンパイルされます。コンパイルされた JavaScript コードは、すべての主要な Web ブラウザーと互換性があります。
- **スタンドアロン**:</br> Dart ソフトウェア開発キット (SDK) には、コマンドライン インターフェイスで Dart コードを実行できるスタンドアロンの Dart VM が付属しています。 Dart には、ユーザーが完全に機能するアプリを作成できる完全な標準ライブラリが付属しています。
- **アヘッド・オブ・タイム (AOT) コンパイル済み**:</br> Dart コードは、Flutter でモバイル アプリを構築できるマシン コードに AOT コンパイルできます。
- **ネイティブ**:</br> dart2native コンパイラを使用すると、Windows、Linux、および macOS で実行できる自己完結型の実行可能ファイルに Dart コードをコンパイルできます。

## Dart ファイル形式 ##

Dart は、インターフェイス、ミックスイン、抽象クラス、具体化されたジェネリック、および型インターフェイスをサポートする C スタイルのオブジェクト指向言語です。

### 構文 ###

以下は、Dart 構文の例です。

#### コンソールに出力 ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### ループと配列 ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

＃＃＃＃ 機能 ＃＃＃＃

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

＃＃＃＃ クラス ＃＃＃＃

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### ミックスイン ####

ミックスインは、継承せずにメソッド/変数を借用できる通常のクラスです。これは、*"with"* キーワードを使用して行います。

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## 参照 ##

- [Dart (プログラミング言語) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [ダーツ](https://dart.dev/)

