{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH ファイル - iPhone/iPod Touch SHSH Blob ファイル形式",
  "description":"SHSH ファイルとは何かについて学びます。",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## .SHSH ファイルとは何ですか?

署名 HaSH とも呼ばれる SHSH ファイルは、iPhone、iPad、iPod などの iOS デバイスのファームウェアのアップデートを認証および検証するために Apple によって使用されるデジタル署名です。

## SHSH と SHSH2 ファイル形式の違い

SHSH2 ファイルと同様に、SHSH ファイルには、「ECID」(Exclusive Chip ID) と呼ばれるデバイスの一意の識別子と、デバイスにインストールされているファームウェアのバージョンに関する情報が含まれています。ただし、SHSH ファイルは古いバージョンの iOS (iOS 10 より前) で使用されていたため、SHSH2 ファイルに置き換えられました。

## SHSH ファイル形式 - 詳細情報

SHSH ファイルはバイナリ ファイル形式でディスクに保存されます。このファイル形式の内部ファイル構造の詳細は公開されていません。

SHSH ファイルは、デバイスのファームウェアを Apple によって署名されなくなった以前のバージョンにダウングレードしたいユーザーにとって重要です。 Apple によって署名されているときに特定のファームウェア バージョンの SHSH ファイルを保存すると、ユーザーは後でそれを使用して Apple の署名検証をバイパスし、そのファームウェア バージョンをデバイスにインストールできます。このプロセスは「脱獄」とも呼ばれます。

## 参考文献

* [SHSH Blob - Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
※【TSSセーバー】(https://tsssaver.1conan.com/v2/)

