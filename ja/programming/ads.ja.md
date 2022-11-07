
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS ファイル - Ada 仕様ファイル形式",
  "description":"ADSファイルを作成して開くことができる例とAPIを使用して,ADSファイル形式とは何かについて学びます.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .ADS ファイルとは?

ADS ファイルは、Ada プログラミング プロジェクトの仕様ファイルです。これは、Java のクラス、または C++ の場合のヘッダーと実装のペアに似ています。 Ada パッケージの公開仕様と非公開仕様は、.ads ファイルに保存されます。対照的に、.adb ファイルには、実装または Ada 本体が含まれています。 [C++](/programming/cpp/) と同様に、Ada は OOP に依存しない仕様と実装の分離を提供します。

ADS ファイルは、Microsoft Notepad、Notepad++、Atom などの任意のテキスト エディターで開くことができます。

## ADS ファイル形式

ADS ファイルは単純なプレーン テキスト ファイル形式で、任意のテキスト エディターで開いたり編集したりできます。 Ada パッケージは階層に編成できます。子ユニットは、次の方法で宣言できます。

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## 参考文献

* [Ada パッケージ](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

