{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion マークアップ言語ファイル",
  "description" :"CFML ファイルとは何か,および CFML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## .CFML オプション番号

拡張子が .cfml のファイルは、Web ページの作成に使用される ColdFusion マークアップ言語ファイルです。これは、ColdFusion アプリケーションがプログラマーによってどのように開発されるかを定義するために使用される一連の規則を指します。 ColdFusion は、[ASP](/web/asp/)、[PHP](/programming/php/) などの他の技術よりも少ない技術で、サーバー側の Web アプリケーションを迅速に作成するために使用されるプログラミング言語です。 CML ファイルを開くことができるアプリケーションには、Adobe ColdFusion 2018、Adobe ColdFusion Builder、および Adobe Dreamweaver が含まれます。

## CFML ファイル形式 - 詳細情報

CFML ファイルはマークアップ ファイルであり、タグの形式で Web 要素が含まれています。これらは、任意のテキスト エディターで開いて編集できるテキスト ファイルです。 CFML ファイルは、[HTML](/web/html/) に似たいくつかのタグで構成され、通常は開始タグと終了タグで構成されます。これらのタグには、1 つ以上の属性を含めることもできます。

### タグの構文

以下は、CFML タグの一般化された構文です。

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

ほとんどのタグは属性を受け入れ、次のように定義されています。

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

これらのタグの中には、次の構文で複数の属性を受け入れるものもあります。

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML コード例

実際の CFML タグ (`cfoutput` タグ) を使用する例を次に示します。

```
<cfoutput>
  #firstname#
</cfoutput>
```

## 参考文献

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

