{
  "date" : "2021-07-29",
  "keywords" :[ "pes 파일", "pes 파일 형식", "pes 파일이란", "file", "pes example", "pes 파일 확장자","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES 파일 형식 - Brother PE 자수 형식",
  "description":"PES 파일 형식과 PES 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## PES 자수 파일이란?

PES 자수 파일은 자수/재봉틀에 대한 지침이 포함된 디자인 파일입니다. 이것은 Brother Industries에서 자수 기계용으로 개발했지만 나중에 일반 파일 형식으로 공식화되었습니다. PES 파일은 재봉틀에서 천에 패턴을 재봉하기 위한 지침을 읽는 데 사용됩니다. 이 파일은 두 가지 용도로 사용됩니다. 먼저 브라더 인더스트리에서 개발한 PE-Design 애플리케이션에 대한 디자인 정보를 제공하고, 두 번째로 디자인명, 색상, "stop", "jump", "trim"과 같은 자수 기계 코드를 제공합니다.

## PES 파일 형식 - 추가 정보

PES 파일은 바이너리 파일 형식으로 디스크에 저장됩니다. 미리 정의된 방법을 사용하여 저장된 재봉 정보가 있는 여러 섹션이 포함되어 있습니다. PES 파일 형식은 다음과 같습니다.

* 버전 데이터 - 버전 정보를 제공하며 값은 `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`일 수 있습니다.
* PEC Seek Value - 버전 데이터 바로 뒤에 오는 4바이트 리틀 엔디안 정수로 설계 세부 정보를 포함하는 PEC 섹션의 탐색 값을 나타냅니다.
* PSE 섹션 - Brother PE-Design과 관련된 디자인 정보가 포함되어 있으며 다른 재봉 응용 프로그램일 수 있습니다.
* PCE 섹션 - PSE 파일의 모든 위치에 있을 수 있지만 PEC 검색 값에 의해 참조됩니다.

## PES 파일을 사용하는 재봉틀의 종류

PES 파일은 주로 Brother 재봉틀과 함께 사용되는 PE-Design 소프트웨어에 의해 생성됩니다. PES 파일을 지원할 수 있는 다른 기계로는 Babylock 및 Bernina 가정용 자수 기계가 있습니다.

## PSE 파일을 변환하는 방법?

PE-Design 소프트웨어 응용 프로그램은 [PSE 파일 변환](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file)을 .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd 또는 .xxx와 같은 다른 형식으로 변환합니다. 파일을 열고 변환 형식을 선택하여 PE-Design 응용 프로그램을 사용하여 수행할 수 있습니다.

## 참고문헌

* [PE 디자인 - 사용 설명서](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

