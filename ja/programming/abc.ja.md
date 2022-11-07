
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScriptバイトコードファイル",
  "description":"ABCファイルを作成して開くことができる例とAPIを使用して,ABCファイル形式とは何かについて学びます.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## .ABC オプション番号

拡張子が .abc のファイルは、ActionScript スクリプト ファイルをコンパイルした結果として Flash コンパイラによって作成された ActionScript バイト コード ファイルです。 ABC ファイルに含まれるバイト コードは、ActionScript 仮想マシン (AVM および AVM2) によって実行されます。バイト コードは、定数データ、AVM2 命令セットからの命令、およびさまざまな種類のメタデータで構成されます。 ABC ファイルが AVM または AVM2 にロードされると、検証が行われます。 AVM2 の概要に準拠していない場合は拒否されます。 ABCファイルは、とうの昔に廃止されたAdobe Flash Playerで開くことができます。

## ABC ファイル形式 - 詳細情報

ABC ファイルは、AVM または AVM2 仮想マシンで読み取り可能なバイナリ ファイル形式でディスクに保存されます。その内部ファイル構造は、すべての定数データ、型記述子、コード、およびメタデータを含む実行可能コード ブロックを表します。

## ABCファイル構造

ABC ファイルの構造は次のとおりです。

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC ファイルのフィールド

|フィールド名|説明|
---|---|
|minor_version, major_version|major_version および minor_version の値は、abcFile 形式のメジャーおよびマイナー バージョン番号です。|
|constant_pool|constant_pool は、整数、倍精度浮動小数点数、文字列、ネームスペース、ネームスペース セット、およびマルチネームで構成される可変長構造です。|
|method_count, method|method_count の値は、メソッド配列のエントリ数です。メソッド配列の各エントリは、可変長の method_info 構造体です。|
|metadata_count, metadata|metadata_count の値は、メタデータ配列のエントリ数です。各メタデータ エントリは、名前を一連の文字列値にマップする metadata_infostructure です。 | |
|class_count, instance, class|class_count の値は、インスタンス配列とクラス配列のエントリ数です。 | |
|script_count, script|script_count の値は、スクリプト配列内のエントリ数です。各スクリプト エントリは、このファイル内の単一のスクリプトの特性を定義する script_info 構造体です。 | |
|method_body_count, method_body|method_body_count の値は、method_body 配列のエントリ数です。各 method_bodyentry は、個々のメソッドまたは関数の命令を含む可変長の method_body_info 構造体で構成されます。|

## 参考文献

* [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

