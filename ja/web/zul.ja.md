{
  "date" : "2021-05-24",
  "keywords" :["zul", "ファイル", "拡張子", "ファイル形式", "ファイル拡張子", "open"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK ユーザーインターフェースファイル",
  "description":"ZUL ファイル形式と,ZUL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .ZUL ファイルとは何ですか?

拡張子が .zul のファイルは、ユーザー インターフェイス マークアップ言語 (ZUML) で作成された Web ファイルであり、ユーザー インターフェイス要素の定義が含まれています。 Ajax および Java クラスは、サーバー側ファイルを開発するための [XML](/web/xml/) ベースの ZUML の使用をサポートします。 ZUL ファイル形式は、JavaScript や AJAX の知識がなくても Web およびモバイル アプリケーションを構築できる UI フレームワークである ZK によって開発されました。

## ZUL ファイル形式

ZUL ファイルは XML ベースであり、ユーザー インターフェイスを構築するためのさまざまな要素で構成されています。 ZK ローダーは、各 XML 要素を使用してコンポーネントを作成します。ページタイトル、説明などのページ要素の全体的な処理は、ZUMLの各XML処理命令によって記述されます。

### ZULの例

次の ZUML コードの例では、1 行目でページ タイトルを指定し、2 行目でタイトルと境界線を含むルート コンポーネントを作成し、3 行目でラベルとイベント リスナーを含むボタンを作成します。

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL スキーマは、http://www.zkoss.org/2005/zul/zul.xsd からダウンロードできます。
## 参考文献

* [ZUL - ZKによる](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL スキーマ](http://www.zkoss.org/2005/zul/zul.xsd)

