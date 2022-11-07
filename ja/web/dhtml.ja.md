{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml ファイル", "dhtml ファイル形式", "dhtml ファイルの種類", "ファイル", "種類", "dhtml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - 動的 HTML ファイル形式",
  "description":"DHTML ファイル形式と,DHTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .DHTML ファイルとは?

拡張子が .dhtml のファイルは、動的な [HTML](/web/html/) ファイルで、Web ページの動的コンテンツの作成に使用されます。 DHTML で作成された Web 要素はイベント ドリブンであり、ページをリロードする必要はありません。ほとんどの場合、DHTML ファイルは、ドロップダウン メニュー、フローティング レイヤー、ロールオーバー ボタン、その他の動的コンテンツなど、Web ページの動的コンテンツを作成するために使用されます。日常生活の中で、メニュー項目にマウスを合わせると、動的な html 要素に出くわし、さらにサブメニュー オプションが開きます。 DHTML は、[HTML](/web/html/)、[Javascript](/web/js/)、HTML DOM、HTML イベント、および [CSS](/web/css/) などの Web テクノロジーを利用して動的な要素の振る舞い。

## DHTML ファイル形式

DHTML ファイルは、Web 要素の動的な動作を実装するための DHTML コードを含むプレーン テキスト ファイルです。


### DHTML DOM

DHTML ドキュメント オブジェクト モデル (DOM) は、次の図に示すように、要素、属性、およびテキストを含むツリー構造である HTML DOM に基づいています。

{{< figure src="../dhtml.png" alt="HTMLDOM" >}}

`Document` ノードを使用して、さまざまな機能を実装するためにいくつかの関数を呼び出すことができます。次の例では、DHTML で JavaScript の document.write() メソッドを単純に使用しています。

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

このコードは、ブラウザに出力するテキスト「Hello World」を書き込みます。

### DHTML イベント

|S.No.|イベント|発生|
---|---|---|
|1|onabort|ユーザーがページまたはメディア ファイルの読み込みを中止したときに発生します。|
|2|onblur|ユーザーが HTML オブジェクトを離れたときに発生します。|
|3|onchange|ユーザーがオブジェクトの値を変更または更新したときに発生します。|
|4|onclick|ユーザーが HTML 要素をクリックすると発生またはトリガーされます。|
|5|ondblclick|ユーザーが HTML 要素を 2 回同時にクリックすると発生します。|
|6|onfocus|ユーザーが HTML 要素にフォーカスしたときに発生します。このイベント ハンドラは、onblur とは反対に機能します。|
|7|onkeydown|ユーザーがキーボード デバイスのキーを押すとトリガーされます。このイベント ハンドラーは、すべてのキーに対して機能します。|
|8|onkeypress|ユーザーがキーボードのキーを押すとトリガーされます。このイベント ハンドラーは、すべてのキーに対してトリガーされるわけではありません。|
|9|onkeyup|オブジェクトまたは要素を押した後、ユーザーがキーボードからキーを離したときに発生します。|
|10|onload|オブジェクトが完全に読み込まれたときに発生します。|
|11|onmousedown|ユーザーが HTML 要素の上でマウスのボタンを押すと発生します。|
|12|onmousemove|ユーザーが HTML オブジェクト上でカーソルを移動すると発生します。|
|13|onmouseover|ユーザーがカーソルを HTML オブジェクトの上に移動すると発生します。|
|14|onmouseout|マウス ポインターが HTML 要素の外に出たときに発生またはトリガーされます。|
|15|onmouseup|マウス ボタンが HTML 要素上で離されたときに発生またはトリガーされます。|
|16|onreset|フォームをリセットするためにユーザーが使用します。|
|17|onselect|Web ページでコンテンツまたはテキストを選択した後に発生します。|
|18|onsubmit|フォームの送信後にユーザーがボタンをクリックするとトリガーされます。|
|19|onunload|ユーザーが Web ページを閉じたときにトリガーされます。|

## 参考文献

* [動的 HTML - ウィキペディア](https://en.wikipedia.org/wiki/Dynamic_HTML)

