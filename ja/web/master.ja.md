{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER ファイル - ASP.NET マスター ページ ファイル形式",
  "description" :"MASTER ファイル形式と,MASTER ファイルを作成して開くための API について学びます。",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## MASTERファイルとは何ですか?

MASTER ファイルは、ASP.NET で作成されたマスター Web ページ テンプレート ファイルです。これは、MASTER ファイルと同じレイアウトと設定を持つ複数のページを作成するための開始点として使用されます。テンプレート MASTER ファイルには、ヘッダー、ナビゲーション メニュー、フッター、フォント、およびスタイル情報の設定が含まれています。 MASTER ファイルを使用すると、複数の Web ページをすばやく作成できます。

MASTER ファイルは、Microsoft Visual Studio 2022 以降を使用して開くことができます。

## MASTER ファイル形式 - 詳細情報

MASTER ファイルは HTML ファイル形式で作成および保存され、他の Web ページ ファイルと同様です。編集可能なセクションと編集不可能なセクションに分かれています。編集可能なセクションは、ユーザーの要件に合わせて変更できるセクションです。 MASTER ファイルを Microsoft Visual Studio で開くと、編集不可能なセクションはグレー表示されます。

マスター ページは、マスター ページ自体と 1 つ以上のコンテンツ ページという 2 つの部分で構成されます。

### マスターページ

マスター ページは .master 拡張子を持ち、ASP.NET で作成されます。静的テキスト、HTMLタグ、サーバー側コントロールで構成される事前定義されたレイアウトがあります。通常の .aspx ページでは、@ Page ディレクティブが使用されます。 .master ファイルの場合、これは @ Master ディレクティブに置き換えられます。

### コンテンツページ

コンテンツ ページは、マスター ページのプレースホルダー コントロールのコンテンツを表します。これらは、実際にはマスター ページの分離コードである .aspx ページです。コンテンツ ページは、以下に示すように、使用するマスター ページを指す MasterPageFile 属性を含めることにより、@ Page ディレクティブを使用してバインドされます。

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## 参考文献

* [ASP.NET マスター ページの概要](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

