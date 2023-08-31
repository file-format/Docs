{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook ストレージ ファイル形式",
  "description":"OST ファイル形式と,OST ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .OST ファイルとは?

OST またはオフライン ストレージ ファイルは、Microsoft Outlook を使用して Exchange Server に登録すると、ローカル マシン上のオフライン モードでのユーザーのメールボックス データを表します。サーバーとの接続時に Microsoft Outlook を初めて使用するときに自動的に作成されます。ファイルが作成されると、データは電子メール サーバーと同期されるため、電子メール サーバーから切断された場合でもオフラインで使用できます。 OST ファイルは、電子メール、連絡先、カレンダー情報、メモ、タスク、およびその他の同様のデータなどのメールボックス アイテムを使用できます。ユーザーは、サーバーに接続していない場合でも OST ファイルに電子メールやその他のデータ項目を作成できますが、これらはサーバーと同期されません。接続が確立されると、サーバーとローカル コピーの両方が同じレベルの情報になるように、ローカル ファイルがサーバーと再び同期されます。

## OST ファイル形式

OST (Offline Storage Table) および [PST](/email/pst/) (Personal Storage Table) ファイル形式は、ユーザーの電子メール、連絡先、および予定の保存に対応する Personal Folder File (PFF) 形式で構成されます。 PFF ファイルのデータはリトルエンディアンで保存され、すべての日付と時刻は UTC の FILETIME として表されます。 [MS-PST] では、次の 2 種類の PFF が定義されています。

* 32 ビット ANSI 形式
* 64 ビット Unicode 形式

Microsoft から入手可能な PST ファイル形式 [仕様](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) は、OST ファイル形式にも無料で適用されます。 Open Specification Promise による取り消し不能な特許ライセンス。これは、次の特徴的な要素で構成されています。

*ファイルヘッダー
* ファイルヘッダーデータ
* インデックス ブランチ ノード
* インデックス リーフ ノード
* (ファイル) オフセット インデックス
* (項目) 記述子インデックス
* ローカル記述子
*アイテムテーブルタイプ

### ヘッダー情報

OST ファイルの HEADER 構造は、ファイルの最初の 0 オフセットにあります。これには、OST ファイルに関するメタデータ情報と、上記の NDB レイヤー データ構造にアクセスするための ROOT 情報が含まれています。 HEADER 構造は、OST ファイル形式の Unicode バージョンと ANSI バージョンでは異なります。

ヘッダーは、バイト (0x21、0x42、0x44、0x4E) で表される 4 バイトのマジック ワード **!BDN** で始まります。別の 2 バイトのマジック ナンバー **SM** (0x53, 0x4D) は、ファイルの先頭からオフセット 8 にあります。バージョン情報 (ANSI または Unicode) は、ファイルの先頭から 10 のオフセットにあります。 16 進値 (0x17) は Unicode OST ファイルを指定し、0x0E または 0x0F は ANSI ファイル形式を表します。

|フィールド|説明
---|---|
|dwMagic (4 バイト)|「{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")」でなければなりません
|dwCRCPartial (4 バイト)|wMagicClient (0ffset 0x0008) から始まる 471 バイトのデータの 32 ビット CRC 値
|wMagicClient (2 バイト)|「{ 0x53, 0x4D }」でなければなりません。
|wVer (2 バイト)|ファイル形式のバージョン。この値は、ファイルが ANSI PST ファイルの場合は 14 または 15 でなければならず、ファイルが Unicode PST ファイルの場合は 23 でなければなりません。
|wVerClient (2 バイト)|クライアント ファイル形式のバージョン。このドキュメントで説明されている形式に対応するバージョンは 19 です。このドキュメントに基づく新しい PST ファイルの作成者は、この値を 19 に初期化する必要があります。
|bPlatformCreate (1 バイト) |この値は 0x01 に設定する必要があります。
|bPlatformAccess (1 バイト) |この値は 0x01 に設定する必要があります。
|dwReserved (8 バイト)|
|bidUnused (8 バイトの Unicode のみ)|Unicode PST ファイル形式が作成されたときに追加された未使用のパディング。
|bidNextP (Unicode: 8 バイト; ANSI: 4 バイト)|次のページの BID。ページには、bidIndex 値を割り当てるための特別なカウンターがあります。ページの BID の bidIndex の値は、このカウンターから割り当てられます。
|bidNextB (4 バイトの ANSI のみ): |次の BID。この値は、次に割り当てられるブロックに割り当てられる BID を示すモノトニック カウンターです。 BID 値は 4 ずつ進みます。詳細については、セクション 2.2.2.2 を参照してください。
|dwUnique (4 バイト)|これは単調に増加する値で、PST ファイルの HEADER 構造が変更されるたびに変更されます。この値の機能は、一意の値を提供し、各ヘッダーの変更後に HEADER CRC が異なることを確認することです。
|rgnid[]   (128 バイト)|32 の NID の固定配列で、それぞれが 32 の可能な NID_TYPE (NID_TYPE、NID_TYPE_NORMAL_FOLDER、NID_TYPE_SEARCH_FOLDER、NID_TYPE_NORMAL_MESSAGE、NID_TYPE_ASSOC_MESSAGE) のいずれかに対応します。
|qwUnused (8 バイト)|未使用スペース。ゼロに設定する必要があります。 Unicode PST ファイル形式のみ。
|root (Unicode: 72 バイト; ANSI: 40 バイト)|ROOT 構造 (セクション 2.2.2.5)。
|dwAlign (4 バイト)|未使用のアラインメント バイト。ゼロに設定する必要があります。 Unicode PST ファイル形式のみ。
|rgbFM (128 バイト)|非推奨の FMap。これはもう使用されていないため、0xFF で埋める必要があります。リーダーは、これらのバイトの値を無視する必要があります。
|rgbFP (128 バイト)|非推奨の FPMap。これはもう使用されていないため、0xFF で埋める必要があります。リーダーは、これらのバイトの値を無視する必要があります。
|bSentinel (1 バイト)|0x80 に設定する必要があります。
|bCryptMethod (1 バイト)|PST ファイル内のデータがどのようにエンコードされているかを示します。事前定義された値 (NDB_CRYPT_NONE、NDB_CRYPT_PERMUTE、NDB_CRYPT_CYCLIC) のいずれかに設定する必要があります。
|rgbReserved (2 バイト)|予約済み;ゼロに設定する必要があります。
|bidNextB (8 バイト)|次に使用可能な BID 値を示します。 Unicode PST ファイル形式のみ。
|bidNextB (Unicode のみ: 8 バイト)|次の BID。この値は、次に割り当てられるブロックに割り当てられる BID を示すモノトニック カウンターです。 BID 値は 4 ずつ進みます。詳細については、セクション 2.2.2.2 を参照してください。
|dwCRCFull (4 バイト)|wMagicClient から始まり、bidNextB を含む 516 バイトのデータの 32 ビット CRC 値。 Unicode PST ファイル形式のみ。
|ullReserved (8 バイト)|予約済み。ゼロに設定する必要があります。 ANSI PST ファイル形式のみ。
|dwReserved (4 バイト)|予約済み。ゼロに設定する必要があります。 ANSI PST ファイル形式のみ。
|rgbReserved2 (3 バイト)|
|b予約済み (1 バイト) |
|rgbReserved3 (32 バイト) |

## 参考文献

* [Outlook 個人用フォルダー (.ost) ファイル形式](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [個人フォルダのファイル形式仕様](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

