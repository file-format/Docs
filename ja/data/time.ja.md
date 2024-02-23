{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME ファイル - .time ファイルとは何ですか? Linuxでファイルが作成された時刻",
  "description" : "TIME ファイルについて学び、Linux でファイルが作成された時間を調べます",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-ja",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## TIMEファイルとは何ですか?

TIME ファイル形式は、ユーザーが自分の生活を記録、整理、共有するのに役立つ LIGHT と呼ばれる Web システムで使用されていました。基本的に、投稿のコレクションを保存し、システム内のユーザーのライフ ページ上のフォルダーを表しました。

## Linux でファイルがいつ作成されたかを確認する方法

Linux では、`stat` コマンドを使用して、ファイルがいつ作成されたかを調べることができます。その方法は次のとおりです。

ターミナルを開き、次のコマンドを入力します。

```
stat <file_path>
```

` を置き換えます<file_path>` を、興味のあるファイルへのパスに置き換えます。例:

```
stat /path/to/your/file.txt
```

このコマンドは、ファイルの作成時刻など、ファイルに関するさまざまな情報を表示します。 「Birth」または「File:」で始まる行を探します。 「誕生」時間は、ファイルがファイルシステム上にいつ作成されたかを示します。

出力の例を次に示します。

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

この例では、「誕生」時間はファイルが作成された時間を示します。

