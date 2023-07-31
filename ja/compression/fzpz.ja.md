{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ ファイル形式 - Fritzing パーツ ファイル",
  "description":"FZPZ ファイルとは何か,および FZPZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## .FZPZ オプション番号

FZPZ ファイルは、回路プロトタイピングおよび設計アプリケーション **Fritzing** で作成された電子回路設計で使用されるコンポーネント/パーツです。 [FZP](/cad/fzp/)ファイルと4枚の[SVG](/page-description-language/svg/)画像をFritzingでまとめた圧縮アーカイブです。これらのファイルを使用する利点は、再利用性の観点から、ユーザーがそれぞれの FZPZ ファイルを共有できることです。 FZPZ 部品の共有は、回路部品を統合してより大きな PCB 設計を迅速に作成するのに役立ちます。

## FZPZ ファイル形式 - 詳細情報

FZPZ ファイルは、圧縮された [ZIP](/compression/zip/) アーカイブとしてディスクに保存されます。拡張子の名前を .fzpz から .zip に変更し、WinZIP などの標準の解凍ユーティリティを使用してアーカイブからファイルを抽出できます。

### FZPZ ファイル構造情報

前述のように、FZPZ ファイルは、プリント回路基板で使用される部品を表現するための複数のファイルを含むアーカイブ ファイルです。 FZPZ には、次のファイルが含まれています。

* `4 つの SVG ファイル` - パーツのブレッドボード、回路図、PCB、およびアイコン イメージを表す
* `FZP file` - パーツのプロパティ、コネクタ、およびバスに関する情報を含む XML ファイル

ファイルは通常、次のように名前が付けられます。

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## 参照 ##

* [fzpz 拡張機能付きの新しいパーツ](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

