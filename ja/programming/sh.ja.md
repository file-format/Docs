{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash シェル スクリプト ファイル",
  "description":"SH ファイル形式と,SH ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## .SH ファイル拡張子

拡張子が .sh のファイルは、Unix シェルによって実行されるコンピューター プログラムを含むスクリプト言語コマンド ファイルです。ファイル処理、プログラムの実行、その他のタスクなどの操作を実行するために順次実行される一連のコマンドを含めることができます。これらは、ユーザーがコマンド ライン インターフェイスから実行するか、複数の操作を同時に実行するためにバッチで実行します。スクリプト ファイルは、Windows、MacOS、Linux OS 上の Notepad、Notepad++、Vim、Apple Terminal、およびその他の同様のアプリケーションなどのテキスト エディターで開くことができます。

## SHファイル形式

SH ファイルは、定義された構文に従ってプレーン テキストで記述されます。これらのスクリプト ファイルは以下をサポートします。

* `Comments` - コメントは # で始まり、シェルによって無視されます。
* `Shortcuts` - コマンドの名前を変更して、短く簡単に実行できるようにするために使用できます。
* `Batch Jobs` - 手動で入力する必要があるいくつかのコマンドを自動的に実行できます。これにより、ユーザーがシーケンスの各ステージをトリガーするのを待つ必要がなくなります。
* `Generalization` - 単純なループを使用して、ある画像から別の画像への変換などの操作に対して、より多くの一般化を実現します。

## SHファイルの例

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## SHファイルを実行するには？
SH ファイルは通常、Linux で実行されます。Windows でも、sh ファイルを実行するには、Putty などのソフトウェアを使用して Linux ターミナルに接続する必要があります。以下は、Linux 端末で SH ファイルを実行する手順です。

1. Linux ターミナルを開き、SH ファイルがあるディレクトリに移動します。
2. `chmod` コマンドを使用して、スクリプトに実行権限を設定します (まだ設定されていない場合)。
3. 次のいずれかを使用してスクリプトを実行します。
1. `./filename.sh`
2. `sh ファイル名.sh`
3. `bash スクリプト名-here.sh`

## 参考文献

* [初心者のための Bashscripting](https://help.ubuntu.com/community/Beginners/BashScripting)
* [シェルスクリプト](https://www.shellscript.sh/)

