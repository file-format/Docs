---
date: 2019-10-11
keywords: kt,.kt,kotlin ファイル形式,kotlin ファイルの開き方,kotlin ファイルの実行方法,.kt ファイル形式,kt ファイル,kotlin ファイル拡張子,.kt 拡張子,kotlin vs Java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT ファイル形式
linktitle: KT
description: "KT ファイル形式と,KT ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## .KT オプション番号##

Kotlin で記述されたソース コードは、**Kotlin ファイル拡張子**として一般に知られている .kt 拡張子で保存されます。 Kotlin は、[Java](/programming/java/) と完全に相互運用できるように JetBrains によって開発された汎用クロスプラットフォーム プログラミング言語です。 Kotlin の商標は Kotlin Foundation によって保護されています。

Kotlin は、2019 年 5 月 7 日に Google によって Android アプリ開発の推奨プログラミング言語として発表されました。Android Studio 3.0 は、2017 年 10 月に Android アプリ開発の代替手段として Kotlin のサポートを開始しました。

## Kotlin KT ファイル形式の簡単な歴史##

Kotlin は、2011 年 7 月に JetBrains によって JVM の新しいプログラミング言語として発表されました。 JetBrains のリーダーである Dmitry Jemerov 氏は、Scala 以外のほとんどの言語には探していた機能が欠けているが、Scala のコンパイルが遅いことが欠点であると述べました。 Kotlin の主な目標の 1 つは、Java と同じくらい速くコンパイルすることでした。 Kotlin プロジェクトは、2012 年 2 月に Apache 2 ライセンスの下でオープンソース化されました。

Kotlin のバージョン 1.0 は 2015 年 2 月 15 日にリリースされました。Android は、Google I/O 2017 で Android での Kotlin のファースト クラス サポートを発表しました。Kotlin 1.2 は、2017 年 11 月 28 日にリリースされ、JVM と JavaScript プラットフォーム間でコードを共有する機能を備えています。 Kotlin 1.3 は 2018 年 10 月 29 日にリリースされ、非同期プログラミングがサポートされました。 Google は、2019 年 5 月 7 日に Android アプリ開発に推奨されるプログラミング言語として Kotlin を発表しました。2020 年 8 月に Kotlin 1.4 がリリースされ、Swift/Objective-C との相互運用性をサポートするための若干の変更が加えられました。

## Kotlin 構文 ##

Kotlin は、Java よりも優れたものになるように設計されていますが、Java から Kotlin への段階的な移行を可能にするために、Java コードと相互運用できるように設計されています。

* Kotlin ではセミコロンは省略可能です。ステートメントの終わりを示すには、改行で十分です。
* Kotlin は、*val* キーワードで定義される読み取り専用変数と、*var* キーワードで定義される可変変数の 2 種類の変数をサポートしています。
* クラスはデフォルトで非公開かつ最終的です。クラスから派生するには、基本クラスを *open* キーワードで宣言する必要があります。
* Kotlin は手続き型プログラミングもサポートしています。
* Kotlin プログラムへのエントリ ポイントは、Java や C# などと同様の「メイン」関数です。

### 構文例 ###

以下は、Kotlin 構文の例です。

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

上記のコードでは、**fun** キーワードが main という名前の関数を定義しています。関数内では、読み取り専用変数 'audience' が **val** キーワードで宣言されています。 **println** メソッドを使用すると、"Hello World from Kotlin" がコンソールに出力されます。変数 Audience の値は、**$** 記号を使用して文字列に挿入されます。

## コトリンとJava
Kotlin は、多くの高度な機能を提供する Android アプリを作成するための公式言語ですが、多くのエキスパート Java 開発者はまだ Kotlin に切り替えることに関心を示していません。彼らは、Java だけですべてを行うことができると考えています。以下は、Java 開発者に切り替えるよう説得する可能性のある 2 つのテクノロジの比較です。

| |パラメータ |ジャワ |コトリン|
|--------------------|-----------------------|---------------- -|
| |シングルトン オブジェクト | √ | √ |
| |ワイルドカードの種類 | √ | Χ |
| |コンパイル |バイトコード |仮想マシン |
| |ラムダ式 | Χ | √ |
| |不変配列 | Χ | √ |
| |非公開フィールド | √ | Χ |
| |スマートキャスト | Χ | √ |
| |ヌル安全 | Χ | √ |
| |静的メンバー | √ | Χ |

## 参照 ##

- [Kotlin (プログラミング言語) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

