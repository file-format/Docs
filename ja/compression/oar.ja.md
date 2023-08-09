{
  "date" : "2021-04-08",
  "keywords" :[ "oar ファイル", "oar ファイル形式", "oar ファイルとは", "ファイル", "oar の例", "oar ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator アーカイブ ファイル形式",
  "description":"OAR ファイル形式と,OAR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## .OAR オプション番号

拡張子が .oar のファイルは、ネットワーク経由でマルチユーザーがアクセスできる仮想環境を作成するためのオープン ソース 3D アプリケーション サーバーである OpenSimulator アプリケーションによって使用されるアーカイブ ファイルです。 OAR ファイル形式は、地形、オブジェクト テクスチャ、およびインベントリを別のシステムに完全にロードするために必要なアセット データを提供します。 OpenSimulator には、ユーザーが Web 経由で他の OpenSimulator インストールにアクセスできるオプションのハイパーグリッドもあります。 OAR ファイルには、インターネット MIME タイプ application/oar があり、1 つ以上のアーカイブ ファイルが含まれています。


## OAR ファイル形式

OAR は、圧縮されたアーカイブ ファイル形式で保存されるバイナリ ファイルです。 OAR ファイル形式の最新バージョンは [バージョン 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) で、以前の [バージョン 0.8](http://opensimulator.org/wiki/OAR_Format_0.8) から大幅に変更されています。。最新バージョンは、1 つの OAR に複数のリージョンを格納することをサポートしており、0.7.5 より前のバージョンの OpenSimulator との下位互換性はありません。 OAR ファイルは、元の UNIX tar 形式 (USTAR ではない) の gzip された tar ファイル (tar.gz) です。

## OAR リージョンの例
AOR ファイルには、複数のリージョンを含めることができます。アーカイブの構造は次のとおりです (この例には 4 つのリージョンが含まれています)。

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

アーカイブ制御ファイルには、将来のフォーマット変更との互換性を定義するためのメジャー バージョン番号が含まれています。 OAR 形式のアセットの存在は、boolean 要素によって示されます<assets_included>.含まれる領域に関する情報は、制御ファイルにあるマニフェストに含まれています。 Archive.xml の例は次のとおりです。

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## 参考文献

* [OAR フォーマット v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

