{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - OpenStreetMap 파일 형식 변경",
  "description":"OSC 파일을 만들고 열 수 있는 OSC 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## .OSC 파일이란?

OSC 파일은 기존 .osm 거리 지도에 대한 수정된 거리 지도 데이터가 포함된 변경 파일 형식입니다. 여기에는 [OSM 파일](/ko/gis/osm/)에 발생할 변경 사항에 대한 정보가 포함되어 있습니다. OSC 파일은 OSM 데이터에 대해 `insert`, `modify` 또는 `delete`와 같은 세 가지 수정 작업 유형을 가질 수 있습니다. 이러한 변경 파일은 일반적으로 OSM 편집기에서 데이터를 내보내고 다른 편집기로 가져오는 데 사용됩니다.

Merkaartar 및 osmchange 소프트웨어로 OSC 파일을 열 수 있습니다.

## OSC 파일 형식

OSC 파일은 일반적으로 변경 사항이 태그로 표시되는 JOSM 파일 형식으로 저장됩니다. 파일의 시작을 나타내는 `osmChange` 태그로 시작합니다. 하위 태그는 OSM 파일의 해당 노드에서 수행할 삽입, 수정 또는 삭제 작업인지 지정합니다. 노드의 내용은 실제로 osm 태그의 내용을 포함합니다.

### OSC 파일 형식 예

다음은 노드에서 수정 작업의 예입니다. 각 요소에는 변경 집합 ID와 버전 번호가 있어야 합니다.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## 참조

* [JOSM 파일 형식](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

