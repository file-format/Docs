{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NSF ファイル形式と,NSF ファイルを作成して開くことができる API について学びます。",
  "title" :"NSF ファイル形式 - Lotus Notes データベース形式",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .NSF オプション番号

拡張子が .nsf (Notes Storage Facility) のファイルは、以前は Lotus Notes として知られていた [IBM Notes ソフトウェア](https://en.wikipedia.org/wiki/HCL_Domino) で使用されるデータベース ファイル形式です。電子メール、予定、ドキュメント、フォーム、ビューなどのさまざまな種類のオブジェクトを格納するスキーマを定義します。このすべての情報は、PST/OST ファイルと同様に、ビジネス コラボレーション用の単一の NSF ファイルに含まれています。 NSF ファイルを開くことができるアプリケーションには、IBM Lotus Notes や IBM Domino などがあります。

## NSF ファイル形式の仕様

NSF ファイルは本質的にバイナリであり、その仕様は Joachim Metz によって [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%) で入手できます。 20file%20format.asciidoc)。これらの詳細に従って、NSF ファイルは次のもので構成されます。

* ファイルヘッダー
* データベース ヘッダー

さらに、次のもので構成されています。

* スーパーブロック
* バケット記述子ブロック
* ビットマップ
* Relocation Vector バケットの記録
* 要約バケット
* 非集計バケット


### NSF ファイル ヘッダー

NSF ファイル ヘッダーのサイズは 6 バイトです。以下で構成されています。

|オフセット|サイズ|値|説明|
---|---|---|---|
0|2|0x1a 0x00|署名|
2|4| |データベースのヘッダー サイズ|

### データベース ヘッダー

NSD データベース ヘッダーには、次の確認済みの値が含まれています。

* データベース情報
* データベース識別子 (DBID)
* 複製情報
* データベース情報バッファ フラグ
* 題名
* カテゴリー
* クラス
・デザインクラス（テンプレート名）
* 特記事項識別子
* パディング
* データベース情報 2
* データベース情報 3
* データベース情報 4
* データベース情報 5
* パディング
* データベース インスタンス識別子 (DBIID)
* 複製履歴

## 参考文献

* [NSF 形式 - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

