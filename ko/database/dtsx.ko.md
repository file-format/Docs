{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX 파일 형식 및 DTSX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"DTSX 파일 형식 - SQL Server DTS 설정 파일",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .DTSX 파일이란?

.dtsx(Data Transformation Services Package XML) 확장자를 가진 파일은 한 데이터베이스에서 다른 데이터베이스로 데이터를 전송하기 위한 데이터 마이그레이션 단계/규칙을 참조하기 위해 Microsoft SQL에서 사용하는 데이터 변환 서비스(DTS) 파일입니다. 여기에는 원본 지점과 대상 지점 간의 데이터 전송 중에 필요할 수 있는 변환 및 선택적 처리 단계가 포함됩니다. Microsoft SQL Server의 구성 요소인 SSIS(SQL Server Integration Services)는 DTSX 파일을 사용하여 데이터베이스 서버 간의 데이터 처리 단계를 식별합니다. DTSX 파일은 Microsoft SQL Server 2019로 열 수 있습니다.

## DTSX 파일 형식

데이터베이스 서버 간의 데이터 이동에는 이 작업 동안 데이터 무결성을 보장하기 위한 규칙과 처리 단계가 필요합니다. SSIS는 기업의 다양한 소스에서 데이터를 이동하고 일치시키기 위한 이러한 모든 활동이 편리하게 수행되도록 합니다. SSIS에서 이러한 단계를 따라 데이터를 처리할 수 있는 단계를 설정하는 데 사용할 구조를 정의하는 DTSX가 여기에 있습니다.

DTSX에서 설명하는 데이터 흐름은 다음 이미지와 같습니다.

{{< figure src="../DataFlowDTSX.png" alt="데이터 흐름 DTSX" >}}

DTSX는 [XML](/ko/web/xml/) 기반이며 [MS-DTSX]https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd) 에 문서화되어 있습니다. DTSX XML의 향상된 리팩토링은 구조에 대한 새 속성, 명명된 속성을 상위 XML 속성으로 대체, 대부분의 속성 값에 대한 기본값 지정, 상위 요소 내부에 반복되는 요소 배치를 포함하는 DTSX 2.0입니다. DTSX 구조는 이러한 [XML 스키마](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1)를 사용하여 설명되며 구조 형식은 다음과 같습니다. 셀러 텍스트 XML.

## 참고문헌

* [DTSX 형식 - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2 형식 - Microsoft 제공](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

