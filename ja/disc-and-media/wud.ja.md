{
  "date" : "2022-03-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"WUD ファイル形式と,WUD ファイルを作成して開くことができる API について学びます。",
  "title" :"WUDファイル形式 - Wii Uディスクイメージファイル",
  "linktitle" : "WUD",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-03-13"
}

## .WUD オプション番号

拡張子が .wud のファイルは、Wii U ゲーム ディスクから作成されたディスク イメージです。結果のディスク イメージ ファイルは、[Cemu](https://cemu.info/) などのビデオ ゲーム エミュレーターで読み込んで、ゲームをエミュレートできます。 WUD ファイルはサイズが大きいため、簡単に転送できるように複数のセグメントとして作成されます。ゲーム情報は、約 2 GB のファイル サイズの WUD ファイル セグメントとしてエクスポートされます。 Cemu などのオープニング アプリケーションでは、これらのセグメント化されたファイルをすべて、開く前に 1 つの WUD ファイルにマージする必要があります。

## WUD ファイル形式

WUD ファイルは独自のファイル形式でディスクに保存され、Cemu エミュレーターにロードして PC 上で Wii U アプリケーションをエミュレートできます。サイズが大きいため、WUD ファイルは [圧縮](/compression/) されてファイル サイズが縮小されます。結果の圧縮ファイルは、WUX ファイルとして知られています。

## 参考文献

* [Wii Uエミュレータ - Cemu](https://cemu.info/)
* [Cemu - ウィキペディア](https://en.wikipedia.org/wiki/Cemu)

