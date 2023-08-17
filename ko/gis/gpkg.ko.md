{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg 파일", "gpkg 파일 형식", "gpkg 파일이란", "파일", "gpkg 예", "gpkg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage 형식 파일",
  "description":"GPKG 파일 형식과 GPKG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## .GPKG 파일이란?
확장자가 .gpkg인 파일은 일반적인 정의, 형식 제한, 무결성 주장 및 콘텐츠 제약 조건이 있는 데이터 및 메타데이터 테이블을 포함하는 SQLite 데이터베이스 컨테이너로 구현된 지리 정보 시스템으로 구성됩니다. 2014년에 출판되었습니다. 미군을 대신하여 OGC(Open Geospatial Consortium)에서 정의한 것입니다. 다양한 정부, 상업 및 오픈 소스 조직이 GeoPackage를 광범위하게 지원합니다.

## GPKG 파일 형식
GeoPackage는 확장된 SQLite 3 데이터베이스 파일로 구성됩니다. 표준은 다음에 대한 일련의 규칙(필수 규칙)을 정의합니다.
- 이미지의 타일 매트릭스 세트 저장
- 벡터 기능
- 다양한 축척의 래스터 맵
- 메타데이터 및 스키마

표준의 2.3절에 정의된 확장 규칙을 사용하여 GeoPackage를 확장할 수 있습니다. GeoPackage를 설계하는 목적은 가능한 한 가벼운 데이터베이스를 만들고 즉시 사용할 수 있는 단일 파일에 포함시키는 것이었습니다. 따라서 오프라인 모드의 모바일 애플리케이션과 클라우드 저장소 또는 USB 저장 장치 등에서의 빠른 공유에 이상적입니다.

### GPKG 콘텐츠
GeoPackages에는 다른 관계형 데이터베이스와 같이 여러 테이블이 포함되어 있습니다. 이러한 테이블은 사용자 정의 테이블이거나 메타데이터 테이블일 수 있습니다. GeoPackages는 두 개의 필수 메타데이터 테이블로 구성됩니다.

#### gpkg_contents
GeoPackage의 목차. 이 테이블의 필수 열은 다음과 같습니다.

- **table_name**: 사용자 정의 데이터 테이블의 실제 이름.
- **data_type**: 데이터 유형(예: 제목, 기능 및 속성)
- **식별자 및 설명**: 사람이 읽을 수 있는 텍스트 ;
- **last_change**: ISO 8601 형식의 마지막 변경 정보 날짜.
- **min_x, min_y, max_x, max_y**: 컨텐츠의 공간적 범위. ;
- **srs_id**: 공간 참조 시스템 .

#### gpkg_spatial_ref_sys
공간 참조 콘텐츠의 경우 타일 및 기능을 포함하되 이에 국한되지 않는 콘텐츠의 각 행은 좌표 참조 시스템을 참조해야 합니다. **gpkg_spatial_ref_sys** 테이블에 저장됩니다. 이 테이블의 필수 열은 다음과 같습니다.

- **srs_name, description**: 사람이 읽을 수 있는 SRS의 이름 및 설명
- **srs_id**: SRS의 고유 식별자. 또한 테이블의 기본 키입니다.
- **조직**: 정의 조직의 대소문자를 구분하지 않는 이름입니다.
- **organization_coordsys_id**: 조직에서 할당한 SRS의 숫자 ID입니다.
- **정의**: SRS의 잘 알려진 텍스트 정의입니다.


## 참고문헌

* [GeoPackage - 위키피디아 제공](https://en.wikipedia.org/wiki/GeoPackage)
* [GeoPackage 시작하기](http://www.geopackage.org/guidance/getting-started.html)

