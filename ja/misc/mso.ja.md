{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office マクロ参照ファイル",
  "description":"MSO ファイルと,MSO ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## .MSO オプション番号

MSO ファイルは、Microsoft Outlook を使用して HTML メッセージを送信するときに作成されるデータ コンテナー ファイル形式です。これは、主に Microsoft Office 2000 アプリケーションで発生します。ほとんどの場合、電子メール メッセージには **Oledata.mso** ファイルという名前が付けられています。電子メールの受信者は、そのような電子メールを開くと、同じソフトウェアがインストールされていなくても、ファイルを正しく表示できます。 MSO ファイルは、[Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b) を参照してください。

## Microsoft MSO ファイル形式

MSO ファイルは、Object Linking and Embedding (OLE) または Component Object Model (COM) 構造化ストレージ複合ファイル実装バイナリ ファイル形式とも呼ばれる Microsoft Compound Document File Format (MCDF) で保存されます。

### MSO ファイル形式の構造

MSO ファイル形式の内部ファイル形式構造は、[Structures](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) で明確に定義されています。 ) MCDF ドキュメントのセクション。ファイル アロケーション テーブル (FAT) は、セクターの割り当てとセクター チェーンを管理します。これには、32 ビットのセクター番号の配列が含まれています。配列内の各インデックスはセクター番号を表し、その値はチェーン内の次のセクターまたは特別な値を表します。

## 参考文献

* [COM 構造化ストレージ](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft 複合ドキュメント ファイル形式 (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

