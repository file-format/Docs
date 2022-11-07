{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml ファイル", "cshtml ファイル形式", "cshtml ファイルの種類", "ファイル", "種類", "cshtml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor ウェブページ",
  "description":"CSHTML ファイル形式と,CSHTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## .CSHTML ファイルとは?

拡張子が .cshtml のファイルは [C#](/programming/cs/) HTML ファイルであり、サーバー側で Razor マークアップ エンジンによって使用され、Web ページ ファイルをユーザーのブラウザーにレンダリングします。このサーバー側のコーディングは、標準の ASP.NET ページに似ており、Web ページがブラウザーに書き込まれるときにその場で動的な Web コンテンツを作成できます。サーバーは、生成されたページをブラウザーに送信する前に、ページ内のサーバー側コードを実行します。データベースへのアクセスや複雑なビューのレンダリングなどの複雑なタスク。 CSHTML ファイルは、Microsoft Visual Studio を使用して生成およびプログラミングできます。

## CSHTML ファイル形式

CSHTML ファイルは、Razor マークアップ エンジンによって概説されている構文に従うテキスト ファイルです。 Razor は C# と VB.NET の両方をサポートしており、従来の ASP や ASP.NET よりも簡単に習得して使用できます。 w3schools には、Razor の [C# と VB.NET の構文](https://www.w3schools.com/asp/razor_syntax.asp) コーディングのためのシンプルで効果的なガイドがあります。

### CSHTML の例

以下は、Razor の CSHTML ファイルで使用される C# コードの例です。

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Razor の同等の VB.NET コードは次のとおりです。

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## 参考文献

* [Razor 構文リファレンス - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

