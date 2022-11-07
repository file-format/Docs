{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ファイルを作成 - Xcode Makefile スクリプト ファイル",
  "description":"XCode MakeFile 形式と,MakeFile ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## MAKE ファイルとは何ですか?

MAKE ファイルは、コードのコンパイルを整理する XCode スクリプト ファイルです。複数のソースコードファイルからプログラムをコンパイルおよびリンクするために使用されます。これは、アプリケーションを更新する必要がある場合に、大規模なアプリケーションのどの部分を再コンパイルする必要があるかを判断するのに役立ちます。変更されたファイルに応じて、一連の命令を使用してファイルを実行します。

## MAKE ファイル形式の例

Make ユーティリティを使用して以下の内容を実行し、以下のように出力します。

```
hello:
	echo "hello world"
```
**出力する**

```
$ make
echo "hello world"
hello world
```

## 参考文献
* [XCode と Make - Apple フォーラム](https://developer.apple.com/forums/thread/657458)
* [Object-C ガイド](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

