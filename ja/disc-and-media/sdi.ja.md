{
  "date" : "2021-08-13",
  "keywords" :[ "sdi ファイル", "sdi ファイル形式", "sdi ファイルとは", "ファイル", "sdi の例", "sdi ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"SDI ファイルを作成して開くことができる SDI ファイル形式と API について学びます。",
  "title" :"SDI - Windows システム展開イメージ ファイル",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## .SDI ファイルとは?
拡張子が .sdi のファイルには、ロード BLOB、ブート BLOB、およびパーツ BLOB が含まれています。 Windows Embedded Studio で一般的に使用され、Windows のロードとインストール用の RAM ディスクまたはブート ディスクを作成します。 SDI は System Deployment Image の略です。 Windows Embedded Studio は、Windows 用のディスク イメージを作成するために使用されるプログラムです。実際、このプログラムには SDI ファイル マネージャー プログラムと **sdimgr.exe** というコマンド ライン ツールが含まれており、両方を使用して SDI イメージを展開、作成、および編集できます。

## SDI ファイル形式
SDI ファイル形式は、システムの起動に仮想ディスクを使用できるようにするために広く使用されています。 Microsoft Windows の一部のバージョンでは、**RAM ブート**が有効になっています。これは、SDI ファイルをメモリにロードしてそこから起動するために重要です。 SDI ファイル形式は、PXE (Preboot Execution Environment) を使用したネットワーク ブートも可能にします。また、ハードディスクのイメージングにも使用されています。
### SDI ファイルのセクション
SDI ファイル自体は、次のセクションにさらに分割できます。
- **Boot BLOB**: これには、実際のブート プログラム STARTROM.COM が含まれます。これは、ハードディスクのブート セクタに似ています。
- **ロード BLOB**: 通常、これには NTLDR が含まれ、ブート BLOB によって起動されます。
- **パート BLOB**: これには、実際のブート ランタイムが含まれます。また、ランタイムのルート ディレクトリ内に配置する必要がある boot.ini および ntdetect.com ファイルも含まれます。
- **ディスク BLOB**: これは、MBR で始まるフラットな HDD イメージです。起動の代わりに、ハード ドライブのイメージングに使用されます。また、Microsoft のユーティリティでマウントできるのはディスク BLOB のみです。


## 参考文献

* [システム展開イメージ - ウィキペディアによる](https://en.wikipedia.org/wiki/System_Deployment_Image)


