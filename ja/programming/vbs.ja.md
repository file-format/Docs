{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "ファイル", "拡張子", "ファイル形式", "Visual Basic Script", "プログラミング ガイド", "vbs の例", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic スクリプト ファイル",
  "description":"VBS ファイル形式と,VBS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## .VBS オプション番号

VBS または VBScript は、Microsoft Visual Basic のスクリプト版と接続されています。コンピューティング環境では、ユーザーはその多くの側面にアクセスして制御することができます。 VBScript では、**Component Object Model** という名前のモデルを使用して、環境の要素とツールを利用できます。この環境は、VBScript の作業と実行のために指定されています。

Web 開発の分野でクライアントからアクセスされると、Javascript と同じように機能します。また、Web ページの処理のためにサーバーによって使用されます。 [HTML](/web/html/) のアプリケーションなど、他のタイプのスクリプト ファイルで考慮することができます。


## 簡単な歴史 ##

これは、Microsoft が Windows スクリプト用に指定したテクノロジの一部として、1996 年に初めてリリースされました。当初は、Web 開発者を支援するために特別に開発されました。同年、Microsoft Windows の Internet Explorer というエクスプローラーが、Visual Basic Script の機能とともにリリースされました。

テクノロジと Web 開発の進歩に伴い、多くの高度な機能を備えた VBScript の多くのバージョンがリリースされました。さらに、来年には、このスクリプト言語が Microsoft Windows の一部となり、新しい機能が追加されます。

## 技術仕様 ##

サーバー側の Web ページには、**Active Server Pages** などのツールが VBScript と共に使用されます。このスクリプト言語は、Windows のスクリプト コンポーネントでも使用できます。この言語のファイルは、Windows では .vbs 拡張子で保存されます。

この言語のコードで使用されるループなどの多くの制御構造があります。また、コマンド ラインであり、名前付きまたは名前なしの引数も含まれます。この言語のファイルは、フォルダまたは Windows オペレーティング システムのデスクトップに簡単に保存できます。 Microsoft Script Editor のような VBScript プログラム用の特定の統合開発環境はありませんが、この言語の開発機能を提供します。

VBScript が Windows のスクリプト ホストによってホストされる場合、VBScript は、スクリプト言語に非常に一般的なさまざまな機能を提供しますが、Visual Basic 6.0 では使用できません。簡単または直接アクセスを伴う機能には、ネットワーク プリンター、無名および名前付きコマンド ライン引数、stdout および stdin、ネットワーク共有、Windows Management Instrumentation、グループ メンバーシップなどのネットワークのユーザー情報などがあります。

## VBS ファイル形式の例 ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## 参照 ＃＃

* [VBS - ウィキペディアによる](https://en.wikipedia.org/wiki/VBScript)



