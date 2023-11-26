{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR 파일 - ESRI BIL 헤더 파일 형식",
  "description":"HDR 파일이란 무엇인가요?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## .HDR 파일이란 무엇입니까?

HDR 파일은 밴드 인터리브 라인(.BIL) 파일에 대한 헤더 정보가 포함된 GIS 헤더 파일입니다. 이미지 데이터를 설명하며 이미지 파일의 이름과 동일합니다. HDR 파일은 일련의 항목으로 구성되며 각 항목은 이미지의 특정 속성을 설명합니다. HDR 파일은 별도의 지리 참조 파일과 함께 실제 좌표로 변환하기 위한 BIL 파일의 레이아웃과 형식을 설명합니다.

## HDR 파일 형식

HDR 파일은 ASCII 텍스트 파일 형식으로 저장됩니다. 여기에는 각 항목이 이미지의 특정 속성을 설명하는 항목 집합이 포함되어 있습니다. 각 HDR 파일의 형식은 다음과 같습니다.

```
<keyword> <value>
```

`<keyword> ` - 설정 중인 특정 속성을 나타냅니다.
`<value> ` - 속성이 설정되는 값입니다.

헤더 항목의 순서에는 제한이 없습니다. 그러나 각 항목은 HDR 판독기에서 사용하는 구문 분석 방법을 준수하기 위해 별도의 줄에 있어야 합니다.

## HDR 파일에 사용된 키워드 요약

|키워드 |허용되는 값 |기본값|
---|---|---|
|nrows |임의의 정수 > 0| 없음
|ncols |모든 정수 > 0| 없음
|nbands |임의의 정수 > 0| 1
|n비트 |1, 4, 8, 16, 32| 8
|바이트순| I = Intel;M = Motorola |호스트 시스템과 동일|
|레이아웃| 빌, 빕, bsq| 빌|
|건너뛰기| 임의의 정수 ≥ 0| 0
|ulxmap |모든 실수| 0|
|ulymap |모든 실수 |nrows - 1|
|xdim |임의의 실수| 1
|ydim |모든 실수| 1
|bandrowbytes |모든 정수 > 0| 가장 작은 정수 ≥ (ncols x nbits) / 8|
|totalrowbytes |모든 정수 > 0| bil의 경우: nbands x bandrowbytes; bip의 경우: 가장 작은 정수 ≥ (ncols x nbands x nbits) / 8|
|밴드갭바이트 |임의의 정수 ≥ 0| 0|

## 참고자료

* [HRD 파일 형식 - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

