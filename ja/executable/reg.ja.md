{
  "date" : "2021-08-02",
  "keywords" :["regファイル","regファイル形式","regファイルとは","ファイル","reg例","regファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"REG ファイル形式と,REG ファイルを作成して開くことができる API について学びます。",
  "title" :"REG - Windows レジストリ ファイル",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## .REG ファイルとは?
REG ファイルは、拡張子が .reg の単なるテキスト ファイルです。これらのファイルは通常、レジストリから典型的なキーをエクスポートすることによって作成されます。これらのファイルは、レジストリのバックアップとしても使用できます (特に、変更を行う前にこの手順が重要です!)。レジストリ ハッキングの実行方法を示しているのと同じサイトで、それらをダウンロード可能なファイルとして利用できるようにしたものもあることがわかります。 REG ファイルは、レジストリを手動で変更し、それらの変更をエクスポートするのに役立ちます。ファイルを少しクリーンアップしてから、他のユーザーと共有してください。

## REGファイル形式
REG ファイル形式は、INI ベースの構文を使用して Windows レジストリの一部をエクスポートおよびインポートするために設計されました。 Windows レジストリは、Microsoft Windows オペレーティング システムおよび Windows レジストリを使用するその他のアプリケーションの低レベル設定を保持するリレーショナル データベースまたは階層データベースです。別の言い方をすれば、レジストリまたは Windows レジストリは、Microsoft Windows オペレーティング システムのすべてのバージョンにインストールされているプログラムとハードウェアの情報、オプション、設定、およびその他の値で構成されていると言えます。
### REGファイルの構文
REG ファイル構文の一部として、いくつかの重要な要素を次に示します。
- **RegistryEditorVersion**: たとえば、Windows 2000、Windows XP、および Windows Server 2003 用の「Windows レジストリ エディター バージョン 5.00」。
- **空白行**: 新しいレジストリ パスの開始を示します。
- **RegistryPathx**: インポートする最初の値を保持するサブキーのパス。
- **DataItemNamex**: インポートするデータ項目の名前。
- **DataTypex**: レジストリ値のデータ型。

キーは、次の構文を使用して .reg ファイルに保存されます。
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
「値の名前」の代わりに「@」を使用して、キーのデフォルト値を編集できます。
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
＃＃＃ 例
REG ファイルの例を次に示します。
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## 参考文献

* [Windows レジストリ - ウィキペディアによる](https://en.wikipedia.org/wiki/Windows_Registry)
* [.reg ファイルを使用してレジストリ サブキーと値を追加、変更、または削除する方法](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- reg ファイルを使用したレジストリ サブキーと値 9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


