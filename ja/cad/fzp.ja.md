{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FZP ファイル形式と,FZP ファイルを作成して開くことができる API について学びます。",
  "title" :"FZP ファイル形式 - Fritzing XML パーツ記述ファイル",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## .FZP オプション番号

FZP ファイルは、[Fritzing](https://fritzing.org/) 電子回路プロトタイピングおよび設計アプリケーションによって作成された XML ファイルです。パーツのプロパティ、コネクタ、およびバスに関する情報が [XML](/web/xml/) ファイル形式で含まれています。 Fritzing では、FPZ ファイルを単独で使用することはできません。代わりに、FZPZ アーカイブ ファイルの一部としてインポートされます。

## FZP ファイル形式 - 詳細情報

FZP ファイルは、パーツのプロパティ、コネクタ、およびバスに関する情報を含む XML ファイルです。これらに加えて、FZP ファイルには、FZP ファイルのタイトル、説明、作成者、発行日に関する情報も含まれています。 Fritzing パーツ ファイルがエクスポートされると、Fritzing アプリは、FZP ファイルと 4 つの [SVG](/image/svg/) ファイルを含む [FZPZ](/compression/fzpz/) 圧縮アーカイブを作成します。

[FZP ファイル形式仕様](https://github.com/fritzing/fzp/blob/master/docs/README.md) は Fritzing の Github で公開されています。

## FZP ファイル構造の例

一般的な FZP ファイルには、次の XML 構造があります。

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## 参考文献

※【FZPファイル形式仕様】(https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [fzpz 拡張機能付きの新しいパーツ](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

