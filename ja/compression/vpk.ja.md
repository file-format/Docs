{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK ファイル - PlayStation Vita アプリケーション パッケージ ファイル形式",
  "description":"VPK ファイル形式と,VPK ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## .VPK オプション番号

拡張子が .vpk のファイルは、Sony PlayStation Vita ゲーム コンソールにサードパーティ アプリをインストールするために使用される圧縮アーカイブ パッケージ ファイルです。これらのファイルは、PS Vita と PSTV がカスタマイズされたユーザー作成コンテンツを使用できるようにする HENkaku による脱獄 Vita PlayStation にのみインストールできます。 VPK アーカイブ ファイルには、[PNG](/image/png/) ファイルなどの画像、[.bin](/disc-and-media/bin/) などの設定ファイル、および[XML](/web/xml/) ファイル形式の構成。

## VPK ファイル形式

VPK ファイルは、標準の圧縮 [ZIP](/compression/zip/) アーカイブとしてディスクに保存されます。これらには、Vita Gaming Console にインストールされるサードパーティ アプリ用の複数のフォルダーとその他の関連ファイルが含まれる場合があります。 VPK パッケージ ファイルの内容を表示するには、拡張子を .vpu から .zip に変更し、WinZip や WinRAR などの標準の解凍ユーティリティを使用して内容を抽出します。

Valvesoftware には、開発者の観点から参照できる [VPK ファイル形式](https://developer.valvesoftware.com/wiki/VPK_File_Format) に関する詳細情報があります。

## VPK ファイルのインストール方法

VPK ファイルは、コマンド ライン ユーティリティ VPK.exe からインストールできます。 Windows OS では、パッケージ化されたすべてのファイルを含む \*.vpk を返す vpk.exe ファイルにファイルをドロップできます。または、コマンド ライン ツールを次のように使用することもできます。

### VPK の作成とファイルの追加

```
vpk <dirname>
```

### VPK ファイルの抽出

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK ビューアー

* [VRF VPK ビューア](https://github.com/SteamDatabase/ValveResourceFormat)

## 参考文献

* [VPKファイル形式](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK ファイル](https://developer.valvesoftware.com/wiki/VPK)

