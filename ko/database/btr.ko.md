{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "Btrieve 데이터베이스" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BTR 파일 형식과 BTR 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"BTR - Btrieve 데이터베이스 파일",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## .BTR 파일이란?

확장자가 .btr인 파일은 [Btrieve](https://www.actian.com/) 트랜잭션 데이터베이스 응용 프로그램에서 만든 데이터베이스 파일입니다. RBMS(관계형 데이터베이스 관리 시스템)와 달리 Btrieve는 빠른 검색을 위해 데이터를 저장하는 방법인 ISAM(색인 순차 액세스 방법)을 기반으로 합니다. BTR 파일은 레코드 모음을 저장하고 요구 사항에 따라 보고서를 생성하는 데 사용됩니다. BTR 파일은 Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility 및 Legend Software BTRIEVE Viewer를 사용하여 열 수 있습니다.

## BTR 파일 구조 - 추가 정보

내부 데이터 구조 및 BTR 파일 구조의 각 바이트 정렬은 공개적으로 사용할 수 없습니다. 그러나 브리에브
BTR 파일에서 정보를 읽을 수 있는 [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)를 제공합니다. 다음 프로그래밍 언어 및 개발 환경과 호환됩니다.

* 엠바카데로 C/C++
* 엠바카데로 델파이
* GNU C/C++
* 마이크로 포커스 코볼
* 마이크로소프트 비주얼 베이직
* 마이크로소프트 비주얼 C++
* 왓콤 C/C++

BTR 파일에서 데이터를 검색하는 것은 관련된 DDF 파일에 따라 다릅니다. DDF가 없으면 그러한 파일에서 정보를 검색하기가 쉽지 않습니다.

## 참고문헌

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Btreive API 소개](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

