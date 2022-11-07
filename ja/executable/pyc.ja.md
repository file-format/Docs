{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"PYC ファイル形式と,PYC ファイルを作成して開くことができる API について学びます。",
  "title" :"PYC ファイル形式 - Python コンパイル済みファイル",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## .PYC オプション番号

PYC ファイルは、Python プログラミング言語で記述されたソース コードから生成されたコンパイル済み出力ファイルです。 Python インタープリターを使用して PY ファイルを実行すると、実行用のバイトコードに変換されます。同時に、コンパイルされたバイトコードも .pyc ファイルとして保存され、必要に応じて後でキャッシュから再利用できます。

## PYC ファイル形式の構造

PYC ファイルはバイトコードであり、そのファイル形式の仕様は公開されていません。ただし、一部のソースによる調査では、[PYC ファイルの構造](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) は次のもので構成されます。

* `4 バイトのマジック番号`r - マーシャリング コードが変更されるたびに変化する単純な 2 バイトと、2 バイトの 0d0a。
* `4 バイトの変更タイムスタンプ` - ソースが変更された場合に再コンパイルできるように、.pyc を生成したソース ファイルの Unix 変更タイムスタンプ。
* 「整列化されたコード オブジェクト」 - ソース ファイルをコンパイルした結果のコード オブジェクトの marshal.dump の出力。

## 参考文献

* [.pyc ファイルの構造](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

