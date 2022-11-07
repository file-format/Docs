{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "ファイル形式", "ファイルの種類", ".asa ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP構成ファイル",
  "description" :"ASA ファイルとは何か,および ASA ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## .ASA ファイルとは?

ASA ファイルは、[ASP](/web/asp/)/ASP.NET プロジェクト用に作成された構成ファイルです。これには、アプリケーションのグローバル レベルでアクセスできるように意図された変数、contains、および関数の宣言が含まれます。プロジェクト内のすべてのページがこれらの変数と関数にアクセスできるため、これらを書き換える必要がありません。そのような例の 1 つが、他の ASP Web サイト ページからアクセスできるようにルート ディレクトリに格納されている Global.asa ページです。 Global.asa ファイルはオプションですが、使用する場合、各アプリケーションは Global.asa ファイルを 1 つだけ持つことができます。

## ASA ファイル形式 - 詳細情報

ASA ファイルは、次の情報を含むプレーン テキスト ファイルです。

※応募イベント
* セッションイベント
* \<object>宣言
* TypeLibrary 宣言
* #include ディレクティブ

## ASA ファイルの例

Global.asa ファイルは次のようになります。

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## 参考文献

* [ASP Global.asa ファイル - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

