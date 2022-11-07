{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT","ファイル","拡張子","ファイル形式","NUT プログラミング言語","プログラミング ガイド","NUT の例","NUT ファイル形式","リス言語",".nut 拡張子ファイル", "NUT ファイル" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - リス言語ファイル",
  "description":"NUT ファイル形式と,NUT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## .NUT オプション番号

NUT は、NUT Open Container Format ファイルを参照します。このNUTファイル形式は、Squirrelとして知られるプログラミング言語に属しています.これは、主に組み込みシステムやビデオ ゲームで使用される、オブジェクト指向の高レベルで命令型のプログラミング言語です。

リス言語は、サイズと帯域幅に応じて簡単に調整できる軽量のスクリプト言語と見なされます。これには、自動参照カウントとメモリ内のガベージ管理の利点が含まれます。

リス言語の構文は、C に似ており、スクリプト言語の機能を備えているため、開発者を引き付けます。それでも、この目的のための他のより一般的なプログラミング言語と比較して、利点はほとんどありません。



## 簡単な歴史 ##

2003 年に Alberto Demichelis によって設計されました。ただし、この言語の安定版は 2016 年にリリースされました。zlib/libpng のライセンスの下で設計されました。 2010 年にライセンスが変更され、MIT に移管されました。この言語は、[LUA](/programming/lua/) (プログラミング言語) のインスピレーションを受けたバージョンと見なされます。 Alberto が設計した Web サイトには、以前の言語をより有利にするための提案のリストがあります。


## 技術仕様 ＃＃

リス言語の機能と仕様は複数あります。動的型付けの機能、委譲のプロパティ、クラスとインターフェイスのいくつかの使用法を提供します。この言語の構文は、C 言語の構文と類似しています。 Enduro/X (クラスター アプリケーション サーバー) などのアプリケーションは、この言語を使用します。 Squirrel はビデオ ゲームにも使用されるため、OpenTTD や GTA IV などがあります。

この言語の安定版リリースは 3.0.7 です。 MirthKit として知られるツールキットは、Squirrel プログラミング言語を使用して、2 次元ゲーム用のオープンソースおよびクロスプラットフォームを提供します。この言語の性質は動的であり、ほとんどの機能は [Python](/programming/py/)、LUA などに似ています。また、レジスタ ベースの VM の実装も含まれます。 Squirrel のパフォーマンスは、LUA に比べて遅くなります。

別の「.nut」拡張子のファイル タイプもあるため、ファイルのサイズを調べて、どの NUT ファイルがあるかを確認する必要があります。 Squirrel スクリプトの NUT ファイルはほとんどの場合 1 MB 未満ですが、ビデオ NUT ファイルのサイズは通常 1 MB を超えます。


## NUT ファイル形式の例 ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## 参照 ＃＃

* [NUT - ウィキペディアによる](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



