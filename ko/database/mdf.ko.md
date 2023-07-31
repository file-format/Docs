{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MDF 파일을 만들고 열 수 있는 MDF 파일 형식과 API에 대해 알아보세요.",
  "title" :"MDF 파일 형식 - SQL Server 마스터 데이터베이스 파일",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .MDF 파일이란?

확장자가 .mdf인 파일은 [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server)에서 사용자 데이터를 저장하는 데 사용하는 마스터 데이터베이스 파일입니다. 모든 데이터가 이 파일에 저장되기 때문에 가장 중요합니다. MDF 파일은 열, 행, 필드, 인덱스, 보기 및 테이블 형식으로 관계형 데이터베이스에 사용자 데이터를 저장합니다. SQL Server에서는 데이터베이스 성능에 긍정적인 영향을 미치도록 자동 증가 및 자동 축소 설정을 지정할 수 있습니다. MDF 파일은 Microsoft SQL Server를 사용하여 데이터베이스에 로드하고 첨부할 수 있습니다. MDF 파일에는 응용 프로그램/옥텟 스트림 MIME 유형이 있습니다.

## MDF 파일 형식

SQL Server에서 데이터 저장의 기본 단위는 페이지입니다. 데이터베이스 할당 스토리지 페이지는 0에서 n까지 번호가 매겨진 논리 페이지로 나뉩니다. 단일 페이지는 페이지 ID, 페이지가 속한 구조 유형, 페이지의 레코드 수, 이전 및 다음 페이지에 대한 포인터로 구성된 96바이트 헤더로 시작합니다.

### 파일 구조

MDF 파일의 데이터 구조는 다음과 같습니다.

* 페이지 0: 헤더
* 1페이지: 첫 번째 PFS
* 2페이지: 첫 번째 GAM
* 3페이지: 첫 번째 SGAM
* 4페이지: 미사용
* 5페이지: 미사용
* 6페이지: 첫 번째 DCM
* 7페이지: 첫 번째 BCM

#### 파일 헤더

모든 파일의 페이지 번호 0에는 파일에 대한 메타데이터를 저장하는 헤더가 있습니다.

#### 페이지 여유 공간(PFS)
PFS는 할당 상태를 식별하고 여유 공간의 양을 결정합니다.

* Bit 1: 페이지 할당 여부를 나타냅니다.
* 비트 2: 페이지가 혼합 익스텐트에서 온 것인지 여부를 나타냅니다.
* 비트 3: 이 페이지가 IAM 페이지임을 나타냅니다.
* 비트 4: 이 페이지에 고스트 레코드가 포함되어 있음을 나타냅니다.
* 비트 5 ~ 7: 다음과 같이 페이지 충만도를 나타내는 결합된 3비트 값:
* 0: 페이지가 비어 있습니다.
* 1: 페이지가 1~50% 찼습니다.
* 2: 페이지가 51~80% 찼습니다.
* 3: 페이지가 81~95% 찼습니다.
* 4: 페이지가 96~100% 찼습니다.

## 참고문헌

* [데이터베이스 파일 및 파일 그룹](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [데이터베이스 분리 및 연결 - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [SQL Server 데이터 파일 분석 분석](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

