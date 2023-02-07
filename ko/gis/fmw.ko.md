{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FMW 파일 - FME 워크벤치 파일 형식",
  "description":"FMW 파일을 만들고 열 수 있는 FMW 파일 형식 및 API에 대해 알아봅니다.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## .FMW 파일이란?

FMW 파일은 공간 데이터 변환에 사용되는 FME Workbench 소프트웨어(FME Desktop 제품군의 일부로 제공)로 생성된 프로젝트 파일입니다. 여기에는 입력 데이터 세트, 변환 속성, 프로젝션 및 출력 설정과 같은 공간 데이터 조작에 사용되는 사용자 정의 설정이 포함됩니다. 공간 데이터 조작 설정은 시각적 레이아웃으로 저장되며 쉽게 편집하고 다시 저장할 수 있습니다.

[Safe Software FME Desktop](https://www.safe.com/fme/fme-desktop/)을 사용하여 FMW 파일을 열 수 있습니다.

## FMW 파일 형식 - 추가 정보

FMW 파일은 바이너리 파일로 디스크에 저장되며 FME 데스크톱 소프트웨어를 통해서만 읽을 수 있습니다. 이 소프트웨어는 또한 여러 관계형 데이터베이스 형식에서 데이터를 읽을 수 있으며 다양한 데이터 형식도 지원합니다.

### FMW 요약 정보

|사실|가치|
---|---|
|리더/라이터|리더|
|라이선스 수준|기본|
|종속성|없음|
|데이터세트 유형|파일|
|기능 유형|고정|
|일반적인 파일 확장자|.fmw|
|자동 번역 지원|예|
|사용자 정의 속성|아니오|
|좌표계 지원|아니요|
|일반 색상 지원|아니요|
|공간 인덱스|아니요|
|스키마 필요|아니요|
|거래 지원|아니오|
|도형 유형 속성|없음|
|인코딩 지원|아니오|

### FMW 지오메트리 지원

|형상|지원?|
---|---|
|집계|아니|
|서클|아니오|
|원호|아니|
|도넛 폴리곤|아니|
|타원호|아니|
|타원|아니오|
|라인|아니|
|없음|예|
|점|아니|
|다각형|아니|
|래스터|아니오|
|고체|아니|
|표면|아니|
|문자|아니오|
|z 값|아니오|


## 참조

* [안전 소프트웨어 FME 데스크톱](https://www.safe.com/fme/fme-desktop/)
* [FMW 요약 정보](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)

