{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx ファイル", "ascx ファイル形式", "ascx ファイルの種類", "ファイル", "種類", "ascx ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCXファイル形式",
  "description" :"ASCX ファイルとは何か,および ASCX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## .ASCX オプション番号

拡張子が .ascx のファイルは、Web ページで再利用可能なコンポーネントとして使用されるユーザー コントロールです。コントロール ボックスからページにドラッグすることで、任意の ASP Web サイトで参照されます。 ASCX ユーザー コントロールが中央ソースとしてプロジェクトに追加され、ユーザー コントロールの変更が Web サイト全体に反映されます。インターネットを介して 2 つのオブジェクト内で通信するメカニズムを定義する ASMX ファイルとは異なり、ASCX ファイルは、ページまたは Web サイトに埋め込むためのユーザー コントロールです。

## ASCX ファイル形式

ASCX ファイルはプレーン テキスト形式で書き込まれ、.ascx.cs で終わる Web ページのようなコード ビハインド機能を使用できます。ユーザー コントロールのマークアップ コードは、次の例に示すように @Control ディレクティブで始まります。

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

この Web ユーザー コントロールは、ページ フッター、ヘッダー、ある種のサイト ナビゲーションなど、多くのページで再利用できます。 Web ユーザー コントロールには、他のコントロールと同様に、視覚的な動作を設定するのに役立つプロパティ、メソッド、およびイベントがあります。

### web.configにユーザーコントロールを登録する例

多くのページで単一のユーザー コントロールを使用するために、Web コントロールを web.config に登録できます。これにより、各ページに個別に登録する代わりに、すべての Web サイトを制御できます。次のサンプル コードは、Web コントロールを web.config に登録して、Web サイト全体のフッターとして表示する方法を定義しています。

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## 参考文献

* [ASCX と ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX ユーザー コントロール](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

