{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDB 파일 형식과 MDB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"MDB 파일 형식 - Microsoft Access 데이터베이스 파일",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## .MDB 파일이란?

확장자가 .mdb인 파일은 RDBMS(관계형 데이터베이스 관리 시스템)인 Microsoft Access 데이터베이스 파일입니다. 기본 및 외래 키를 통해 서로 연결된 데이터베이스 테이블에 데이터를 저장합니다. MDB 파일에는 데이터베이스 테이블, 쿼리, 저장 프로시저의 전체 구조가 포함되어 있습니다. MDB는 Microsoft Access 2003의 기본 파일 형식입니다. Microsoft Access의 측면 버전은 현재까지 최신 파일 형식인 [ACCDB](/ko/database/accdb/) 파일 형식을 사용합니다. MDB 파일은 Microsoft Access, MDB Viewer, MDBOpener와 같은 응용 프로그램으로 열 수 있으며 ACCDB, [CSV](/ko/spreadsheet/csv/), Excel 형식 등으로 변환할 수 있습니다.

## MDB 파일 형식

MDB 형식에 사용할 수 있는 공개 사양이 있으며 이는 Microsoft의 독점 파일 형식으로 유지됩니다. 그러나 Microsoft는 ODBC(Open Database Connectivity) 표준 및 VBA(Visual Basic for Applications)를 사용하여 MDB 파일에 대한 연결 액세스를 제공합니다. 비공식 MDB 가이드는 리버스 엔지니어링을 기반으로 MDB 형식에 대한 간략한 비공식 설명을 제공하며 사양에 대해 알기 위해 참조할 수 있습니다.

### 페이지

비공식 MDB 가이드에 따르면 MDB 파일은 고정 크기 페이지(Jeb DB3의 경우 2048바이트, Jet DB 4의 경우 4096바이트)로 구성됩니다. 첫 번째 바이트는 페이지 유형을 나타냅니다. 다음은 주요 페이지 유형입니다.

`첫 페이지:` 파일이 호환되는 Jet DB 버전의 식별도 포함하는 데이터베이스 헤더 정보를 포함합니다. 또한 파일 보안 정보와 페이지 사용 맵도 포함되어 있습니다.

`테이블 정의 페이지:` 테이블 정의 페이지는 열, 데이터 유형, 인덱스 및 기타 정보를 지정합니다. 필요한 경우 추가 페이지를 사용하고 이 테이블에 대한 행 데이터가 포함된 페이지 맵을 포함합니다.

`데이터 페이지:` 데이터 페이지는 데이터가 행별로 저장되는 실제 데이터 컨테이너입니다. 보조 페이지를 사용하여 긴 데이터 값을 저장합니다.

단일 Microsoft Access 데이터베이스는 파일 및 테이블 크기 제한을 초과할 수 있는 여러 파일로 구성될 수 있습니다. 이를 통해 사용자 데스크탑의 프론트 엔드 MDB 파일에 양식과 코드를 넣고 네트워크에 연결된 서버의 다른 백엔드 MDB 파일에 데이터를 넣을 수 있습니다.

## 참조 ##

* [액세스 사양](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
