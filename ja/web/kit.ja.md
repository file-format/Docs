{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KIT ファイル形式と,KIT ファイルを作成して開くことができる API について学びます。",
  "title" :"KIT ファイル形式 - CodeKit ファイル",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .KIT ファイルとは何ですか?

拡張子が .kit のファイルは、[CodeKit](https://codekitapp.com/) プログラミング言語アプリケーションで作成された HTML ファイルです。既存の [HTML](/web/html/) ファイルに加えて `imports` と `variables` が含まれているため、静的なサイトに最適です。 CodeKit は KIT ファイルを HTML にコンパイルし、静的 Web サイト ファイルとして簡単に使用できます。

## キットファイル形式

KIT ファイルは、インポートと変数を追加で含む HTML ファイルです。これらはプレーン テキスト ファイルとして保存され、任意のテキスト エディターまたは Web ファイル エディターで開くことができます。

### KIT ファイルのインポート

ほぼすべての種類のファイルをキット ファイルにインポートできます。以下は、ファイルを .kit ファイルにインポートするために使用されるインポート構文です。

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

インポートを KIT ファイルに追加して保存すると、インポートされるファイルのテキストに置き換えられます。 @import の代わりに @include を使用することもできます。

### KIT ファイルでの複数のインポート

コンマ区切りのリストを使用して、一度に複数のファイルをインポートすることもできます。

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## 参考文献

※【キットとは】(https://codekitapp.com/help/kit/)

