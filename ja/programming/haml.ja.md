{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML ファイル形式 - Haml ソース コード ファイル",
  "description":"HAML ファイル形式と,HAML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## .HAML ファイルとは?

HAML ファイルは、[Haml](https://haml.info/) 言語で記述されたソース コードを含む HTML 抽象化マークアップ言語ファイルです。 ERB (Ruby テンプレート スクリプト) の代わりとして使用できます。 HAML ファイルには、Web ドキュメントの HTML を生成するためのテンプレート ソース コードが含まれています。 ERB ファイルは、ファイルの拡張子を変更して app/views フォルダー内のこれらのファイルを Haml に置き換えるだけで置き換えることができます。 HAML ファイルは、Microsoft Notepad、Notepad++、Apple TextEdit、

## HAML ファイル形式

HAML ファイルは、プレーン テキスト ファイルとしてディスクに保存されるソース ファイルです。 HAML 構文で記述されたコードが含まれています。 HAML は **<>** タグを **%** 記号に置き換えて、コードをより単純で簡単にします。次の簡単な例に示すように、ERB ファイルは HAML でドロップイン置換できます。

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML の例

以下は、HAML の Hello World の例です。

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
次の HTML 出力にレンダリングされます。

```
<p class="sample" id="welcome">Hello, World!</p>
```

## 参考文献

* [HAML - Github](https://github.com/haml/haml)

