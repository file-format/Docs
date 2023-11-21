{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO ファイル - Unix CPIO アーカイブ ファイル形式",
  "description":"CPIO ファイルとは何か,また CPIO ファイルを作成して開くことができる API について学びましょう。",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## .CPIO ファイルとは何ですか?

CPIO ファイルは、Unix の Copy In Copy Out (CPIO) 形式で作成されたアーカイブ ファイルです。非圧縮である点を除けば、TAR ファイル形式と似ています。 CPIO ファイルには、デバイス ファイル、シンボリック リンク、および拡張ファイル属性を保存できます。

## CPIO ファイル形式

CPIO アーカイブは、人間が判読できないバイナリ ファイルとして作成されます。ファイルとディレクトリのコレクションを保存します。 CPIO アーカイブの内容は、ファイル名、権限、所有権、タイムスタンプなどのメタデータ情報によって識別されます。このメタデータ情報は、システムによる横方向のアクセスのためにアーカイブ ファイルにも保存されます。

## CPIO アーカイブの形式

CPIO ファイルは、1 つ以上の連結されたメンバー ファイルで構成されます。アーカイブ内の各ファイルはヘッダーで構成され、その後にオプションでヘッダーに記載されているファイルの内容が続きます。アーカイブの最後には、TRAILER!! という名前の空のファイルで記述された別のヘッダーが含まれています。

### CPIO アーカイブの種類

CPIO アーカイブには 2 つのタイプがあります。これらはヘッダーのスタイルのみが異なります。

* ASCII アーカイブ - これらの CPIO アーカイブには、アーカイブ自体が ASCII ファイルで構成されている場合、CPIO アーカイブの一部となる印刷可能なヘッダーがあります。
* バイナリ アーカイブ - これらの CPIO アーカイブにはバイナリ ヘッダーがあります。

## CPIO アーカイブの操作

### CPIO アーカイブを作成するには?

**cpio** コマンドを使用して、Unix 系システム上に CPIO を作成できます。次のコマンドは、現在のディレクトリとそのサブディレクトリ内のすべてのファイルとディレクトリを検索します。この出力は cpio コマンドにパイプされ、archive.cpio という名前の新しい CPIO アーカイブが生成されます。

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### CPIO アーカイブからファイルを抽出するには?

次のコマンドは、既存のアーカイブからファイルを抽出します。

```
cpio -id < archive_cpio.cpio
```
標準入力から archive.cpio ファイルを読み取り、ファイルを現在のディレクトリに抽出します。


## 参考文献

* [CPIO - Wikipediaより](https://en.wikipedia.org/wiki/Cpio)
* [CPIO ファイル形式](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

