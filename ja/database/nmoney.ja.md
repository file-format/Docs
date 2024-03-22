{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NMONEY ファイル形式と,NMONEY ファイルを作成して開くことができる API について説明します。",
  "title" :"NMONEY ファイル - Denaro アカウント ファイル形式",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## NMONEY ファイルとは何ですか?

NMONEY ファイルは、金融取引の実績を含む金融データ ストレージ データベース ファイルです。これは Nickvision によって開発され、個人金融ソフトウェア アプリケーションである Nickvision Denaro ソフトウェアで使用されました。 NOMONEY ファイル内に保存されるデータには、口座へのクレジットおよびデビットのトランザクション情報が含まれます。

NOMONEY ファイルは、[Github](https://github.com/NickvisionApps/Denaro) アプリケーションで開くことができます。

## デナロ ソフトウェアについて

Denaro は当初 [Nickvision](https://nickvision.org/) によって製品として開発されましたが、後に [Github](https://github.com/NickvisionApps/Denaro) でホストされるオープンソース ソフトウェア アプリに変換されました。 。それ以来、アプリは Github 上でのみ変更および更新されています。アプリは、Windows App SDK (現時点では WinUI 3) を使用して Windows UI の C# で開発されています。

### デナロが提供する機能

* 最も人気があり使い慣れたタブ インターフェイスで複数のアカウントを同時に管理
* タイプ、グループ、または日付でトランザクションをフィルタリングします
※毎月発生する請求書などの繰り返し取引
* ある口座から別の口座に送金する
* アカウントからデータを CSV ファイルとしてエクスポートし、CSV、OFX、または QIF ファイルをインポートしてアカウントにトランザクションを追加します

## デナロ ファイル形式 - 詳細情報

Denaro ファイルはバイナリ ファイル形式でディスクに保存されます。財務データは、**.SQLITE3** ファイル形式のデータベース ファイルとして保存されます。 SQLITE は、SQLite ソフトウェアで作成された軽量の SQL データベース ファイルです。完全な機能を備えた信頼性の高いデータベースを提供できる自己完結型データベース エンジンを提供します。 SQLite データベース ファイルを使用すると、ネットワーク上でこれらのファイルを交換するだけで、システム間でリッチ コンテンツを共有できます。 SQLite バインディングは、C、[C#](/ja/programming/cs/)、[C++](/ja/programming/cpp/)、[Java](/ja/programming/java/)、[PHP](/ja/programming/php/) などのプログラミング言語用に存在します)。 、その他多数。

## 参考文献

※【ニックビジョン】(https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

