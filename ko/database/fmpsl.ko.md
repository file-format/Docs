{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FMPSL 파일 형식과 FMPSL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"FMPSL 파일 형식 - FileMaker Pro 12 스냅샷 링크 파일",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## .FMPSL 파일이란?

FMPSL 파일은 FileMaker Pro 12로 생성된 데이터베이스의 스냅샷 파일입니다. 데이터베이스에서 쿼리한 결과를 시각적 레이아웃 및 가시적 정보와 같은 기타 정보와 함께 저장합니다. FMPSL 파일을 사용하여 FileMaker Pro 데이터베이스의 다른 인스턴스에서 이 모든 데이터를 복원할 수 있습니다. 이 파일 형식은 FileMaker Pro v 12 출시와 함께 도입되었습니다. 이 버전 이전에는 스냅샷 링크가 FileMaker Pro v 11에서 FPSL 파일 형식으로 도입되었습니다. FMPSL 파일은 FileMaker Pro Advanced 소프트웨어로 열 수 있습니다. FileMaker Pro에서 지원하는 다른 파일 형식에는 [FP5](/ko/database/fp5/), [FP7](/ko/database/fp7/) 및 [FMP12](/ko/database/fmp12/)가 있습니다.

## FMPSL 파일 형식

FMPSL 파일의 내부 파일 형식 세부 정보는 개발자 참조를 위해 공개적으로 사용할 수 없습니다.

### 레코드를 FMPSL 파일로 저장하는 방법은 무엇입니까?

FileMaker Pro 데이터베이스의 데이터는 다음 단계를 사용하여 스냅샷 링크 파일로 저장할 수 있습니다.

1. 데이터베이스에서 스냅샷 링크 파일로 저장해야 하는 레코드를 검색합니다.
1. 메뉴에서 Send Record As Snapshot Link 옵션을 사용하여 파일 이름을 입력하여 파일을 저장합니다.
1. 검색 중인 레코드를 사용하여 발견된 전체 레코드 세트를 저장합니다.

생성된 스냅샷 파일은 지정된 이름으로 디스크에 저장됩니다.

## 참고문헌

* [FileMaker Pro 파일 형식의 이전 버전을 FMP12 파일 형식으로 변환](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [기록을 스냅샷 링크 파일로 저장](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

