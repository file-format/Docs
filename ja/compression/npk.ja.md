{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPKファイル形式",
  "description":"NPK ファイル形式と,NPK ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## .NPK オプション番号

NPK ファイルは、**MikroTik** ルーターがルーターのオペレーティング システムをアップグレードするために使用するソフトウェア アップグレード パッケージ ファイルです。これは、ソフトウェア アップデートをインストールするためにルータにロードされる圧縮されたバイナリ アーカイブとして提供されます。 NPK ファイル内に含まれる情報には、IP アドレスや IP サービスなどのネットワーク情報、コネクタ情報 (イーサネット インターフェイスとシリアル ポート)、電子メールのセットアップ、ブリッジ構成、ローカル ユーザー管理が含まれます。

## NPK ファイル形式

NPK ファイルは、圧縮されたバイナリ アーカイブとして保存されます。これは、MikroTik 自身のみが使用するクローズド ファイル形式です。サードパーティを介して RouterOS アドオンを作成することは意図されていません。 NPK ファイルは MikroTik 自体によって維持され、アップグレードされたバージョンは [MikroTik](https://mikrotik.com/download) Web サイトのダウンロード セクションからダウンロードできます。

NPK ファイルがルーターにアップロードされると、再起動しない限りルーターの OS は有効になりません。そのため、ルーターの OS をアップグレードするには再起動が必要です。

## 参考文献

* [MikroTik - ルーター OS のアップグレード](https://mikrotik.com/download)
* [NPK ファイルの作成方法](https://forum.mikrotik.com/viewtopic.php?t=87126)

