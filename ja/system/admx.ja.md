{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX ファイル - グループ ポリシー管理テンプレート ファイル形式",
  "description":"ADMX ファイル形式と ADMX ファイルを開く方法について説明します。",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADMX ファイルとは何ですか?

ADMX ファイルは、グループ内のコンピューターのグループを管理する Microsoft Windows グループ ポリシー ソフトウェアによって使用されるポリシー構成ファイルです。これは XML ベースの管理テンプレート ファイルであり、Windows Vista Service Pack 1 で導入されました。ADMX ファイルには、ユーザー アカウント、オペレーティング システム構成、およびアプリケーションの構成設定が含まれています。 ADMX ファイルは、多くのコンピュータ システムを集中管理するための構成を保存および展開するために使用されます。

ADMX ファイルは、XML 互換のテキスト エディタまたは Microsoft グループ ポリシー オブジェクト エディタを使用して作成または編集できます。

## ADMX ファイル形式 - 詳細情報

ADMX ファイルは、人間が判読できる汎用 [XML](/ja/web/xml/) ファイル形式で保存されます。これは多言語ファイル形式であり、異なる言語のシステム管理者が同じ ADMX ファイルを操作できるようになります。 ADMX ファイルは、Unicode 形式のテキスト ファイル形式である古い [ADM](/ja/system/adm/) ファイル形式を置き換えました。 ADMX ファイルは、特定のグループ ポリシー設定が変更されたときに変更されるレジストリ キーを指定します。

### ADMX ファイルで何ができるのですか?

ADMX ファイルは、グループの一部であるユーザー コンピューターにどのようなアクションを許可するかを定義します。グループ ポリシーは、Active Directory ソフトウェアと組み合わせてルール セットを適用します。 ADMX ファイルは、ドメイン内の中心的な場所である Windows OS 上の中央ストアから管理されます。

作業環境に展開された ADMX ファイルを使用すると、管理者は次のようなポリシーを実装できます。

* インターネットの使用を制御する
* 特定の種類のファイルのダウンロード
* システム上でのリムーバブル デバイスの使用

## 参考文献

* [管理用テンプレート ファイル - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 管理用テンプレート ファイルの管理](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

