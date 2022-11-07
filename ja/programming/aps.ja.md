{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ リソース ファイル",
  "description":"APS の例と,APS ファイルを作成して開くことができる API を使用して,APS ファイル形式について学びます。",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## APSファイル形式とは何ですか?
APS ファイルは、Microsoft のソフトウェア開発アプリケーションである Visual C++ によって作成されます。プロジェクトに組み込まれたリソースのバイナリ表現を保存し、アプリケーションがリソースをより迅速にロードできるようにします。これらのファイルは、.aps ファイル拡張子で簡単に見つけることができます。実際、リソース エディターは resource.h ファイルを直接読み取らないため、リソース コンパイラーはそれらをリソース エディターによって使用される .aps ファイルにコンパイルします。

## APS ファイル形式
APS ファイル形式は単なるコンパイル手順であり、シンボリック データのみを格納します。コメントなどの非記号情報は、コンパイル プロセス中に破棄されます。たとえば、保存すると、リソース エディタはリソース スクリプト ファイルと resource.h ファイルを上書きします。リソース自体への変更はすべてリソース スクリプト ファイルに組み込まれたままですが、リソース スクリプト ファイルが上書きされると、コメントは常に失われます。


## 参考文献

* [リソース ファイル (C++)](https://docs.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


