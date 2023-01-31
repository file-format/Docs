{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - OpenStreetMap 更改文件格式",
  "description":"了解可以创建和打开 OSC 文件的 OSC 文件格式和 API。",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## 什么是 .osc 文件？

OSC 文件是一种更改文件格式，其中包含现有 .osm 街道地图的修改后的街道地图数据。它包含有关对 [OSM 文件](/zh/gis/osm/) 进行更改的信息。 OSC 文件可以对 OSM 数据进行三种可能的修改操作，即“插入”、“修改”或“删除”。这些更改文件通常用于将数据从 OSM 编辑器中导出并导入到另一个编辑器中。

您可以使用 Merkaartar 和 osmchange 软件打开 OSC 文件。

## OSC 文件格式

OSC 文件通常以 JOSM 文件格式保存，其中更改由标签表示。它以指示文件开头的 osmChange 标记开头。子标签指定是否要对 OSM 文件中的相应节点执行插入、修改或删除操作。节点的内容实际上包含 osm 标签的内容。

### OSC 文件格式示例

以下是对节点进行修改操作的示例。每个元素都必须有一个变更集 ID 和一个版本号。

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## 参考

* [JOSM 文件格式](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

