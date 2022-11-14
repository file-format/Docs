{
  "date" : "2021-07-28",
  "keywords" :[ "ntf 파일", "ntf 파일 형식", "ntf 파일이란", "파일", "ntf 예제", "ntf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - 국가 전송 형식 파일",
  "description":"NTF 파일 형식과 NTF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## .NTF 파일이란?
확장자가 .ntf인 파일을 **NTF(National Transfer Format)** 파일이라고 합니다. UK Ordnance Survey(OS)에서 주로 사용합니다. 특히 지리 공간 데이터 전송을 위해. 영국 표준 기관에서 관리합니다. Ordnance Survey 디지털 데이터의 표준 전송 형식이 되었습니다. Transverse Mercator의 한 유형인 영국의 National Grid 투영법은 NTF 파일에 대한 모든 지리 참조 정보를 보유하고 있습니다.

## NTF 파일 형식
NTF 파일 형식은 영국의 Ordnance Survey가 소유합니다. 가져오기를 위해 GDB 라이브러리에서 지원합니다. NTF 파일 형식의 현재 버전은 2.0입니다. 이 파일 형식은 구조당 속성 필드가 하나만 있는 **PCIDSK** 벡터 세그먼트의 제한 사항을 해결하기 위해 도입되었지만 벡터 데이터로 추출할 수 있는 속성은 다양합니다. NTF 파일 형식을 우회하려면 두 개의 세그먼트가 있는 것으로 구성됩니다. 각 세그먼트는 동일한 벡터로 구성되지만 속성은 다릅니다. NTF 벡터 파일의 첫 번째 세그먼트에는 특성 코드 번호가 있는 벡터가 포함됩니다. 두 번째 세그먼트에는 값이 속성인 벡터가 포함됩니다.

### 좌표 참조 시스템
GDB 라이브러리는 적절한 TM 투영 특성을 가진 래스터 및 벡터 데이터를 나타냅니다.

- 기준 경도: 49.0
- 기준 위도: 2.0
- False Easting: 400000
- 거짓 북향: -100000
- 규모: 0.9996012717
- 타원체: 에어리 1830(E009)
NTF 파일을 업데이트하거나 쓰기 위한 지원이 제공되지 않으며 DTM 파일을 연결할 수도 없습니다.

### 오그리포 예시
다음 예에서는 NTF 파일에서 **ogrinfo**를 사용하여 레이어 번호를 검색합니다.
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## 참고문헌

* [영국 NTF(National Transfer Format)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [웹 매핑 - Tyler Mitchell 그림](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

