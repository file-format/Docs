{
  "date" : "2019-10-11",
  "keywords" :["クラス",".class","クラスファイルとは","クラスファイルの開き方","拡張子","ファイル","クラスファイル","クラスファイル形式",".class拡張子", "Java のクラスファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"クラス - Java クラス ファイル形式",
  "description":"クラス ファイルの形式と,クラス ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## クラスファイルとは？

**Java のクラス ファイル**は、Java 仮想マシン (JVM) によって実際に実行される [.java](/programming/java/) クラスのコンパイル済み出力です。クラス ファイルは、個別に実行することも、他のパッケージ ファイルと一緒に [JAR](/programming/jar/) ファイルの一部としてバンドルすることもできます。これらは、コマンド ライン インターフェイスから **`javac`** コマンドを使用して作成できます。 [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) や NetBeans などの一部の Java IDE は、プロジェクトの Java から .class 出力ファイルを作成します。ファイル。

## クラスファイル形式

Java クラス ファイルは、JVM によって実行される中間コードであるバイトコードで構成されます。クラス ファイルは 8 ビット バイトのストリームで構成され、マルチバイト データ項目は常にビッグ エンディアン順に格納されます。

### クラスファイルの構造

クラスファイルの構造は以下のとおりです。
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
どこ：

* u1 = 符号なしの 1 バイト量
* u2 = 符号なし 2 バイトの数量
* u4 = 符号なし 4 バイト量

.class ファイル構造の詳細は、Oracle [クラス ファイル形式](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) で説明されており、以下で参照できます。参照用の開発者。これらのフィールドの概要は次のとおりです。

* `magic` - マジック アイテムは、クラス ファイル形式を識別するマジック ナンバーを提供します。値は 0xCAFEBABE です。
* `minor_version`、`major_version` - minor_version および major_version アイテムの値は、このクラス ファイルのマイナーおよびメジャー バージョン番号です。
* `constant_pool_count` - constant_pool_count 項目の値は、constant_pool テーブル内のエントリ数に 1 を加えた値に等しくなります。 long 型および double 型の定数を除き、constant_pool インデックスは、0 より大きく、constant_pool_count より小さい場合に有効と見なされます。
* `constant_pool[]` - constant_pool は、さまざまな文字列定数、クラス名とインターフェイス名、フィールド名、および ClassFile 構造とそのサブ構造内で参照されるその他の定数を表す構造 (§4.4) のテーブルです。各 constant_pool テーブル エントリの形式は、最初の「タグ」バイトによって示されます。
* `access_flags` - access_flags 項目の値は、このクラスまたはインターフェースへのアクセス許可とプロパティを示すために使用されるフラグのマスクです。
* `this_class` - this_class 項目の値は、constant_pool テーブルへの有効なインデックスでなければなりません。
* `super_class` - クラスの場合、super_class 項目の値はゼロであるか、constant_pool テーブルへの有効なインデックスでなければなりません。
* `interfaces_count` - interfaces_count アイテムの値は、このクラスまたはインターフェイス タイプの直接スーパー インターフェイスの数を示します。
* `interfaces[]` - インターフェイス配列の各値は、constant_pool テーブルへの有効なインデックスである必要があります。
* `fields_count` - fields_count 項目の値は、fields テーブル内の field_info 構造の数を示します。
* `fields[]` - fields テーブルの各値は、このクラスまたはインターフェイスのフィールドの完全な説明を提供する field_info 構造体でなければなりません。
* `methods_count` - methods_count 項目の値は、メソッド テーブル内の method_info 構造体の数を示します。
* `methods[]` - メソッド テーブルの各値は、このクラスまたはインターフェイスのメソッドの完全な説明を提供する method_info 構造体でなければなりません。 method_info 構造体の access_flags 項目に ACC_NATIVE フラグと ACC_ABSTRACT フラグのどちらも設定されていない場合、メソッドを実装する Java 仮想マシン命令も提供されます。
* `attributes_count` - attributes_count 項目の値は、このクラスの属性テーブル内の属性 (§4.7) の数を示します。
* `attributes[]` - 属性テーブルの各値は、attribute_info 構造体でなければなりません。




## 参考文献

* [クラスファイル形式](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

