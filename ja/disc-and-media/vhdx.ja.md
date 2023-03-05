{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VHDX ファイル形式と,VHDX ファイルを作成して開くことができる API について学びます。",
  "title" :"VHDX ファイル形式 - VHDX ファイルとは?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## .VHDX オプション番号

VHDX ファイルは、仮想ハード ディスク v2 ファイル形式のディスク イメージ ファイルです。これには、ソフトウェアのテストまたは特定のオペレーティング システムを必要とするソフトウェアの実行のための通常のマシンとしてロードして使用できるオペレーティング システム全体が含まれています。 VHDX は完全なディスク イメージですが、1 つのファイルに格納されます。 Parallels Desktop、Windows Virtual Machine、Virtual Box などの仮想マシン ソフトウェアは、ディスク イメージを読み込んで開くことができます。

VHDX ファイルは、Hyper-V Manager で [VHD](/disc-and-media/vhd/) に、VirtualBox で [VDI](/disc-and-media/vdi/) に変換できます。

## VHDX ファイル形式 - 詳細情報

VHDX ファイル形式の詳細は完全に文書化されており、[VHDX ファイル形式の仕様](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) としてオンラインで入手できます。 ) Microsoft ドキュメンテーション。これは VHD 形式の拡張であり、拡張機能が含まれています。 VHDX ファイル形式は、仮想ハード ディスクおよび仮想ハード ディスク ファイル層で使用できる追加機能を提供します。より最適化されており、ストレージ ハードウェアの構成と機能の結果が向上しています。 VHDXファイルを開くことができます

### VHDX での仮想ハードディスクのサポート

3 種類の仮想ハードディスクをサポートしています。

1. **固定仮想ハードディスク** - 固定データ サイズが割り当てられた仮想ハードディスク。仮想ハードディスクのサイズは、データの追加または削除によって変化しません。

1. **ダイナミック仮想ハードディスク** - ダイナミック ディスク サイズの仮想ハードディスク。そのサイズは常に、書き込まれる実際のデータとメタデータと同じ大きさです。データが追加または削除されると、ファイル サイズが動的に増加します。

1. **差分仮想ハード ディスク** - 親仮想ハード ディスク ファイルと比較して、変更されたブロックのセットとして現在の仮想ハード ディスクを表します。

## 参考文献

* [VHDX ファイル形式の仕様](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - ウィキペディアによる](https://en.wikipedia.org/wiki/VHD_(file_format))

