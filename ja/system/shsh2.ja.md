{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 ファイル - iOS SHSH Blob ファイル形式",
  "description":"SHSH2 ファイルとは何かについて学びます。",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## SHSH2ファイルとは何ですか?

SHSH blob または ECID SHSH とも呼ばれる SHSH2 ファイルは、iPhone、iPad、iPod などの iOS デバイスのファームウェアのアップデートを認証および検証するために Apple によって使用されるデジタル署名です。これには、ECID (Exclusive Chip ID) として知られるデバイスの一意の識別子が含まれています。デバイスにインストールされているファームウェアのバージョンに関する情報も含まれています。

## SHSH2 ファイル形式 - 詳細情報

SHSH2 ファイルはバイナリ ファイル形式でディスクに保存され、このファイル形式の内部ファイル構造の詳細は公開されていません。

新しいバージョンの iOS が iPhone、iPad、Mac などの Apple デバイスにインストールされると、SHSH2 ファイルが生成されます。この SHSH2 ファイルは Apple サーバーに送信され、Apple サーバーがこのデジタル署名ファイルを読み取って検証します。この情報に基づいて、サーバーはインストールを許可または禁止します。

更新が要求された場合も同様のことが起こります。ユーザーが iTunes または別のソフトウェアを通じてデバイスのアップデートまたは復元をリクエストすると、Apple のサーバーはアップデートの続行を許可する前に、SHSH2 ファイルがデバイスの ECID およびファームウェアのバージョンと一致することを確認します。

## 参考文献

* [SHSH Blob - Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
※【TSSセーバー】(https://tsssaver.1conan.com/v2/)

