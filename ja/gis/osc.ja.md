{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - OpenStreetMap ファイル形式の変更",
  "description":"OSC ファイル形式と,OSC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## .OSC オプション番号

OSC ファイルは、既存の .osm ストリート マップの変更されたストリート マップ データを含む変更ファイル形式です。 [OSMファイル](/ja/gis/osm/)に加えられる変更に関する情報が含まれています。 OSC ファイルには、OSM データに対する 3 つのタイプの変更操作、つまり「挿入」、「変更」、または「削除」を含めることができます。これらの変更ファイルは、OSM エディタからデータをエクスポートし、別のエディタにインポートするためによく使用されます。

OSC ファイルは、Merkaartar および osmchange ソフトウェアで開くことができます。

## OSC ファイル形式

OSC ファイルは通常、変更がタグで表される JOSM ファイル形式で保存されます。ファイルの先頭を示す`osmChange`タグから始まります。サブタグは、OSM ファイル内の対応するノードで実行される操作が挿入、変更、または削除であるかどうかを指定します。ノードのコンテンツには、実際には osm タグのコンテンツが含まれています。

### OSC ファイル形式の例

以下は、ノードでの変更操作の例です。各要素には変更セット ID とバージョン番号が必要です。

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## 参考文献

* [JOSMファイル形式](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

