{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - 設定ファイル",
  "description":"CONFIGファイルの例と,CONFIGファイルを作成して開くことができるAPIを使用して,CONFIGファイル形式について学びます。",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## CONFIG ファイルとは何ですか?
CONFIG ファイルは構成ファイルと呼ばれます。いくつかのコンピュータ ソフトウェアのパラメータと主要な設定を構成するために使用されます。一部のソフトウェアは、起動時に **構成ファイル** のみを読み取ります。構成ファイルの変更を定期的にチェックする人もいます。

## コンフィグファイル形式
**CONFIG ファイル形式**は、サーバー プロセス、ソフトウェア アプリケーション、およびオペレーティング システムの設定に使用されます。プログラマーは、一定期間後に構成ファイルを何度も読み取り、現在のプロセスに変更を適用するようにソフトウェアに指示するコードを作成できます。 CONFIG ファイルの sysntax には、決定的な標準や強力な規則はありません。たとえば、Microsoft の Web.config ファイルは、[XML](/web/xml/) ベースのタグセットで構成される CONFIG ファイル形式に属しています。 Microsoft Visual Studio またはその他のテキスト エディターで編集できます。

## 構成ファイルの例:
構成ファイルは、規則、標準、または規則に従って作成されていないため、これらのファイルは異なる形式を使用して記述されている可能性があります。 .config ファイルは、XML、[JSON](/web/json/)、またはその他の形式に基づいている場合があります。以下は、よく知られているオペレーティング システムとソフトウェアの構成ファイルの例です。

### Linux の構成ファイル
すべての Linux プログラムは、CPU が通常の操作を実行するために実行する **オペコード** のリストを保持する実行可能ファイルです。ほとんどすべてのプログラムの操作は、構成ファイルを変更することで、要件に合わせてカスタマイズできます。 Linux システムのいくつかの構成ファイルは、/etc ディレクトリにあります。構成ファイルは、次のカテゴリに分類できます。
|カテゴリ|例|コメント|
---|---|---|
|アクセス ファイル|/etc/host.conf|ネットワーク ドメイン サーバーにホスト名の検索方法を指示します。|
|起動とログイン/ログアウト|/etc/rc.d/rc.local|公式ではありません。 rc、rc.sysinit、または /etc/inittab から呼び出すことができます。|
|ファイル システム|/etc/mtools.conf|DOS タイプのファイル システムでのすべての操作 (mkdir、コピー、フォーマットなど) の構成。|
|システム管理|/etc/shells|システムで利用可能な「シェル」のリストを保持します。|
|ネットワーク|/etc/gated.conf|gated の設定。 gated デーモンによってのみ使用されます。|
|システム コマンド|/etc/logrotate.conf|ダイナミック リンカーの構成。|
|Daemons|/etc/httpd.conf|Web サーバーである Apache の構成ファイル。通常、このファイルは /etc にはありません。|
|ユーザープログラム| /etc/lynx.cfg|プロキシ設定|
### AWS CONFIG ファイルの例
頻繁に使用される構成設定と認証情報は、AWS CLI によって維持される CONFIG ファイルに保存できます。 CONFIG ファイルは、次の形式を使用するプレーンテキスト ファイルである必要があります。
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG ファイルの例
OpenSSH クライアント側構成ファイルは CONFIG という名前で、.ssh ディレクトリに保存されます。 SSH CONFIG ファイルは、次の構造で構成されています。
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG ファイルの例
Python CONFIG ファイルは次のようになります。

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## 参考文献

* [Linux 構成ファイルについて](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [構成と認証情報ファイルの設定](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Python の構成ファイル](https://martin-thoma.com/configuration-files-in-python/)

