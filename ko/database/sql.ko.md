{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SQL 파일을 만들고 열 수 있는 SQL 파일 형식과 API에 대해 알아보세요.",
  "title" :"SQL 파일 형식 - 구조화된 쿼리 언어 데이터 파일",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## .SQL 파일이란?

확장자가 .sql인 파일은 관계형 데이터베이스에서 작동하는 코드가 포함된 SQL(Structured Query Language) 파일입니다. 데이터베이스에 대한 CRUD(Create, Read, Update 및 Delete) 작업에 대한 SQL 문을 작성하는 데 사용됩니다. SQL 파일은 데스크톱 및 웹 기반 데이터베이스에서 작업하는 동안 일반적입니다. JPQL(Java Persistence Query Language), LINQ, HTSQL, 4D QL 등과 같은 SQL에 대한 몇 가지 대안이 있습니다. SQL 파일은 Microsoft SQL Server의 쿼리 편집기, MySQL 및 Windows OS의 메모장과 같은 기타 일반 텍스트 편집기로 열 수 있습니다.

## 약력

* 1970년대 초 IBM의 Donal D. Chamberlin과 Raymond F. Boyce가 개발 및 도입
* IBM의 원래 준관계형 데이터베이스 관리 시스템인 System R에서 데이터를 저장하고 검색하는 데 사용
* 각각 1979년, 1981년, 1983년에 상용화된 System/38, SQL/DS, DB2를 포함한 System R 프로토타입을 기반으로 상용 제품에 사용하기 시작했습니다.
* ANSI 및 ISO 표준 그룹에서 1986년까지 관계형 데이터베이스 관리 시스템(RDBMS)을 위한 표준 "데이터베이스 언어 SQL"로 공식 채택

## SQL 파일 형식

SQL 파일은 일반 텍스트 형식이며 여러 언어 요소로 구성될 수 있습니다. 서로 의존하지 않고 실행이 가능하다면 하나의 SQL 파일에 여러 문장을 추가할 수 있다. 이러한 SQL 명령은 CRUD 작업을 수행하기 위해 쿼리 편집기에서 실행할 수 있습니다.

### SQL 언어 요소

SQL 언어 요소는 다음과 같습니다.

|요소|설명|
---|---|
|조항| 문장 및 쿼리의 구성 요소.|
|표현| 스칼라 값 또는 데이터의 열과 행으로 구성된 테이블을 생성할 수 있음|
|술어| SQL 3값 논리(3VL)(true/false/unknown) 또는 부울 진리값으로 평가할 수 있는 조건을 지정하고 명령문 및 쿼리의 효과를 제한하거나 프로그램 흐름을 변경하는 데 사용됩니다.|
|질의| 특정 기준에 따라 데이터를 검색합니다. 이것은 SQL의 중요한 요소입니다.|
|설명| 스키마 및 데이터에 지속적인 영향을 미치거나 트랜잭션, 프로그램 흐름, 연결, 세션 또는 진단을 제어할 수 있습니다.|

### SQL 예제
다음 SQL 문은 **DATA**라는 테이블을 만들고 이 테이블에 레코드를 삽입하기 위한 추가 `INSERT` 명령이 뒤따릅니다.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## 참조 ##

* [위키피디아의 SQL](https://en.wikipedia.org/wiki/SQL)
* [SQL 구문](https://en.wikipedia.org/wiki/SQL_syntax)

