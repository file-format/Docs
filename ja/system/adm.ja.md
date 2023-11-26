{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM ファイル - 管理用テンプレート ファイル形式",
  "description":"ADM ファイル形式と ADM ファイルを開く方法について学びます。",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADM ファイルとは何ですか?

ADM ファイルは、レジストリ ファイル内のレジストリ ベースのポリシー設定の場所を指定するために Microsoft グループ ポリシー ソフトウェアによって使用されるテンプレート ファイルです。これは、グループの一部であるコンピューターのグループを管理するためのポリシーを定義するためにシステム管理者によって使用されます。この情報は、グループの管理のために作成されるグループ ポリシー オブジェクト (GPO) の一部になります。

ADM ファイルは、Microsoft グループ ポリシー オブジェクト エディターを使用して開くことができます。

## ADM ファイル形式 - 詳細情報

ADM ファイルは、Unicode 形式のテキスト ファイルとして保存されます。これらは主に、Windows Vista および Windows 7 レジストリ内のレジストリ ベースのポリシー設定の場所を説明するために使用されます。

ADM ファイルはサポートされなくなり、[ADMX](/ja/system/admx/) ファイルに置き換えられました。 GPA は、Microsoft Windows Vista Service Pack 1 以降を実行しているコンピュータでは、次のデフォルトの ADM ファイルを無視します。

* システム.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## 参考文献

* [管理用テンプレート ファイル - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 管理用テンプレート ファイルの管理](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

