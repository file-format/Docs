{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks ライセンス ファイル",
  "description":"QBL ファイル形式と,QBL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## .QBL オプション番号

拡張子が .qbl のファイルは、ユーザーが購入したコピーのライセンス情報を含む QuickBooks ライセンス ファイルです。これは通常、QuickBooks がインストールされた後、「license.qbl」という名前でローカル システムに保存され、ユーザーはソフトウェアの初回実行時にソフトウェアにライセンス情報を入力します。 QBL は、QuickBooks のライセンス情報を保存するために使用された初期のファイル形式です。これは現在、QuickBooks の「qbregisteration.dat」ファイルに置き換えられており、ユーザーの確認メール、購入した DVD、またはその他の購入手段からの情報が取り込まれています。 QBL ファイルは、Windows のメモ帳、Apple TextEdit、Notepad++、Github Atom エディターなどのテキスト エディターで開くことができます。

## QBL ファイル形式 - 詳細情報

QBL ファイルは、プレーン テキスト ファイルとして作成および保存されます。これらのファイルの情報は人間が判読でき、これらのファイルをテキスト エディターで開いたときに編集/更新できます。その後、QuickBooks ソフトウェアの使用を開始するために、ライセンスおよびユーザー登録情報をこのファイルにコピーできます。 QBL ファイルは通常、Windows オペレーティング システムの Program Files\Intuit\QuickBooks\INET ディレクトリに保存されます。

QBL ファイルには、2 種類の情報が含まれています。

* `QuickBooks バージョン情報:` インストールされている QuickBooks のバージョンを指し、xx.x などの形式です。
* `ライセンス キー:` 000-000 0000-0000-0000-000 000073adbf3f 形式のテキスト。000-000 0000-0000-0000-000 はユーザーの qbregisteration キーに置き換えられます

## 参考文献

* [QuickBooks by Intuit](https://quickbooks.intuit.com/)
* [QuickBooks - qbregistration.dat ファイルの生成](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)

