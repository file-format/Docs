{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR ファイル形式 - TeamViewer パイロット セッション レポート ファイル",
  "description":"TPSR ファイル形式と,TPSR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## .TPSR ファイルとは何ですか?

TPSR は、TeamViewer Assist AR (以前は TeamViewer Pilot と呼ばれていました) によって使用される接続プロトコル ファイルです。 TPSR ファイルに格納される情報は、圧縮された [ZIP](/compression/zip/) ファイル形式で格納されます。 TPSR には、問題の解決とレビューの目的で、専門家と技術者の間の TeamViewer 接続の詳細な履歴が含まれています。 TPSR ファイル内に含まれる情報には、デバイスの種類、名前、アシスト AR ID、エキスパート ID、日時、および接続時間が含まれます。このデータは、圧縮された TPSR アーカイブ内の [JSON](/web/json/) ファイルに保存されます。

## TPSR ファイル形式

TPSR ファイルは ZIP アーカイブ ファイル形式でディスクに保存され、コンテンツは JSON ファイル内に保存されます。 TeamViewer で接続レポート オプションが有効になっている場合、Assist AR 接続の完了後に自動的に生成されます。

TeamViewer Assist AR を使用すると、専門家は技術者に接続して、モバイル カメラを介してリモート エンドのライブ フィードを取得できます。技術者が電話で問題を解決するのを支援できます。

## TPSRファイルを開く

TeamViewerソフトウェアのデスクトップバージョンを使用してTPSRファイルを開くことができます.コンピュータにインストールされている場合、TPSR ファイルをダブルクリックすると、TeamViewer ソフトウェアで開きます。 TPSR ファイルは [PDF](/pdf/) ファイルにエクスポートすることも、印刷してプロトコル ファイルのコピーを作成することもできます。

## 参照 ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

