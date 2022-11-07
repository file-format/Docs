{
  "date" : "2022-04-01",
  "keywords" :[ "nkit ファイル","nkit ファイル形式","nkit ファイルとは","ファイル","nkit の例","nkit ファイルの拡張子","拡張子","形式","nkit フッター","ファイル nkitのフォーマット"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"NKIT ファイル形式と,NKIT ファイルを作成して開くことができる API について学びます。",
  "title" :"NKIT - ディスク イメージ ファイル形式",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## .NKIT オプション番号

NKIT ファイルは、NintendoWii およびゲームキューブ ゲームから抽出されたデータのディスク イメージです。 NKIT は Nintendo Toolkit フォーマット用です。結果の圧縮 [ISO](/compression/iso/) ファイルは、これらのゲームのメイン データを利用して、Dolphin、Swiss、Nintendont などのエミュレータ プログラムで実行されます。 NKit は生 (iso) および圧縮 (gcz) ファイル形式で提供され、どちらもビューの再生可能性とサイズを維持するように設計されています。

## NKIT ファイル形式

NKit ファイル形式は非損失形式であり、ニンテンドー Wii およびゲームキューブの画像の縮小と復元に使用されます。形式は、ゲームキューブと Wii の各ゲームの ISO および GCZ ファイル形式で利用できます。

|システム |フォーマット |ハードウェア サポート |Dolphin サポート |復元可能 1:1 |注意事項|
---|---|---|---|---|---|
|ゲームキューブ| nkit.iso|はい|はい|はい |圧縮されたゲームキューブ iso と同じ|
|ゲームキューブ| nkit.gcz|いいえ|はい|はい |GCZ は Dolphin 独自のブロック シーク可能な圧縮形式です|
|Wii| nkit.iso|いいえ はい|はい| Dolphinでのみ再生可能なRVT-Hフォーマット|
|Wii| nkit.gcz|いいえ はい|はい| Dolphin のみでプレイ可能な GCZ の RVT-H |

### NKITヘッダー

NKIT ファイル形式のヘッダーは次のとおりです。

|オフセット |長さ |名前|
---|---|---|
|0x200 |0x4 |NKit ヘッダー 'NKIT'|
|0x204 |0x4 |NKit バージョン ' v01'|
|0x208 |0x4 |ソース画像オリジナル CRC32|
| |0x20C |0x4 |NKit CRC - NKit ファイルの CRC32 を 0x208 (GCZ の 0x4) のソース CRC と等しくします。
|0x210 |0x4 |ソース画像の長さ|
|0x214 |0x4 |Forced Junk ID (Disc IDが異なる場合 - レア - ゲームキューブのみ)|
|0x218 |0x4 |Wii 変換時に削除された場合、パーティション CRC32 を更新|

## 参照 ##

* [NKIT ファイル形式 - gbatemp による](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

