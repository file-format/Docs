{
  "date" : "2019-10-11",
  "keywords" :[ "JAR",".jar","jarファイルとは","jarファイルの開き方","拡張子","ファイル","jarファイル","jarファイル形式",".jar拡張子" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java アーカイブ ファイル形式",
  "description":"JAR ファイルの形式と,JAR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .JAR ファイルとは?

拡張子が .jar のファイルは、さまざまなアプリケーション関連のファイルを 1 つのファイルとして含む Java アーカイブ ファイルです。このファイル形式は、複数の HTTP 接続を作成しないようにすることで、ダウンロードした Java アプレットを HTTP トランザクション経由でブラウザーにロードする速度を下げるために作成されました。 1 つの JAR ファイルには、Java クラス ファイル ([.class](/programming/class/))、[画像](/image/)、および [サウンド](/audio/) を含めることができます。アプリケーション開発者は、JAR ファイル内の個々の項目にデジタル署名を付けて、その発信元を認証できます。 JAR ファイルは、その API に関連する特定の機能を含む関数 API を作成するために定期的に使用されます。

## JAR ファイル形式

JAR ファイルは、個々のコンテンツ ファイルを 1 つのファイルにアーカイブする一般的な [ZIP ファイル形式](/compression/zip/) に基づいています。 JAR ファイル形式は圧縮をサポートしているため、ダウンロードのファイル サイズが小さくなり、ダウンロード時間がさらに短縮されます。 [JAR ファイルの仕様](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) Oracle の記事には、JAR ファイルの内部仕様に関する完全な詳細が記載されています。

### マニフェストファイル

JAR ファイルが作成されると、JAR ファイルの内容に関するメタデータ情報を含むマニフェスト ファイルがその中に自動的に作成されます。このファイルは、JAR ファイル内にパッケージ化されている内容を示しています。一般的なマニフェスト ファイルは次のようになり、JAR ファイルに含まれるフォルダーとクラスが示されます。

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### マニフェスト仕様

マニフェストの仕様は、Oracle によって次のように定義されています。

`manifest-file`: main-section newline \*individual-section

`main-section`: version-info newline \*main-attribute

`version-info`: Manifest-Version : バージョン番号

`バージョン番号` : 数字+{.数字+}*

`main-attribute`: (正当なメイン属性) 改行

`individual-section`: Name : value newline \*perentry-attribute

`perentry-attribute`: (正当な perentry 属性) 改行

`改行` : CR LF | LF | CR (後に LF が続かない)

`digit`: {0-9}

### 実行可能な JAR

JAR ファイルは、Microsoft Windows オペレーティング システム上の他のアプリケーションと同様に、Java 仮想マシン (JVM) で実行できるアプリケーションで構成することもできます。この場合、JVM は、public static void main メソッドを持つ任意のクラスであるアプリケーションのエントリ ポイントを認識する必要があります。マニフェスト ファイルは、次の形式の `Main-Class` ヘッダーでそのようなクラスを識別します。

```
Main-Class: com.example.MyClassName
```



## 参考文献

※【JARファイル概要】(https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR ファイル形式](https://en.wikipedia.org/wiki/JAR_(file_format))

