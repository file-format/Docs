{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"LDF 파일 형식과 LDF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"LDF - SQL Server 마스터 데이터베이스 파일 형식",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .LDF 파일이란?

확장자가 .ldf인 파일은 RDBMS(관계형 데이터베이스 관리 시스템)인 Microsoft SQL Server에서 유지 관리하는 로그 파일입니다. 기본 데이터베이스 파일([MDF](/ko/database/mdf/))에서 수행된 모든 트랜잭션(삽입, 업데이트, 삭제 등)은 LDF 파일에 기록됩니다. LDF 파일은 모든 데이터베이스의 중요한 구성 요소입니다. 시스템 장애가 발생한 경우 로그 파일을 사용하여 데이터베이스를 일관된 상태로 복원합니다. 트랜잭션이 완전히 커밋되지 않은 경우 트랜잭션 로그 파일의 크기가 커질 수 있습니다. LDF 파일은 Microsoft SQL Server 소프트웨어 응용 프로그램으로 열 수 있습니다.

## LDF 파일에 기록된 작업

SQL 로그 파일은 다음 작업을 기록합니다.

* 각 거래의 시작과 끝.

* 각 데이터 데이터 수정(삽입, 업데이트 또는 삭제). 여기에는 시스템 테이블을 포함한 모든 테이블에 대한 시스템 저장 프로시저 또는 DDL(데이터 정의 언어) 문에 의한 변경도 포함됩니다.

* 모든 익스텐트 및 페이지 할당 또는 할당 해제.

* 테이블 또는 인덱스 생성 또는 삭제.

## LDF 파일 형식

LDF 파일은 로그 레코드의 문자열로 정렬된 SQL Server 트랜잭션 레코드로 구성됩니다. 각 로그 레코드에는 이전 레코드의 LSN보다 높은 LSN(로그 시퀀스 번호)이 있습니다. 문자열은 파일에서 서로 연결됩니다. 최신 고속 컴퓨터로 인해 LSN1 이전의 로그 파일에서 LSN2가 존재하는 위치에 레코드를 삽입할 수 있습니다. 작업은 직렬로 기록되기 때문에 LSN2에서 설명한 변경은 로그 기록 LSN1 이후에 수행되었습니다. 특정 트랜잭션에 대한 레코드는 사용되는 포인터를 사용하여 역방향으로 연결되고 트랜잭션의 롤백 속도를 높입니다.
 

## 참고문헌

* [데이터베이스 파일 및 파일 그룹](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [트랜잭션 로그 아키텍처 및 관리 가이드](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- 서버-ver15)

