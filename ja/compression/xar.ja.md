{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - 拡張可能なアーカイブ ファイル形式",
  "description":"XAR ファイル形式と,XAR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## .XAR オプション番号

拡張子が .xar (Extensible Archive Format) のファイルは、圧縮形式または非圧縮形式の UNIX アーカイブです。また、Mac OS でのパッケージのインストールにも使用されます。 XAR はオープンソースであり、Safari ブラウザで使用するために Mac OS X 10.5 に含まれています。

## XAR ファイル形式

[XAR](https://github.com/mackyle/xar/wiki/xarformat) ファイルには 3 つの主要な領域があります。

* ヘッダー
* 目次
*ヒープ

### XAR ヘッダー

XAR ヘッダーは次のような構造になっています。

|フィールド|データ型|サイズ (バイト単位)|
---|---|---|
|マジック|符号なし整数 32|4|
|サイズ|符号なし整数 16|2|
|バージョン|符号なし整数 16|2|
|TOC 長さ圧縮|符号なし Int 64|8|
|TOC 長さ 非圧縮|符号なし Int 64|8|
|チェックサム|符号なし整数 32|4|
|メッセージ ダイジェスト名 |Null 終了||

XAR ヘッダーの C 構造体は、次のように定義できます。
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
ヘッダーのすべてのフィールド (マジック、サイズ、バージョン、toc_length_compressed、toc_length_uncompressed、cksum_alg) は、常にネットワーク バイト (ビッグ エンディアン) 順で XAR ファイルに格納されることに注意してください。

### XAR 目次 (TOC)

目次は、UTF-8 としてエンコードされている (およびエンコードされている必要がある) XML ドキュメントです。ファイルの先頭に保存されるため、アーカイブをスキャンして個々のファイルを簡単に抽出できます。 XAR アーカイブを使用すると、[GZIP](/compression/gz/)、[BZIP2](/compression/bz2/) などのさまざまな圧縮スキームを使用して、アーカイブ内の個々のファイルを個別に圧縮/エンコードできます。

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### ヒープ

圧縮された toc の直後にヒープが開始されます。これは、TOC によって参照される構造化されていないデータのヒープです。 TOC にリストされている Offset 値は、ヒープの先頭から始まります。 toc 内の長さの値は、ヒープに格納された実際のバイト数 (圧縮されているかどうかに関係なく) を示します。一方、サイズの値は、アイテムの抽出されたサイズ (必要に応じて解凍した後) を示します。

## 参考文献

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - ウィキペディア](https://en.wikipedia.org/wiki/Xar_(archiver))

