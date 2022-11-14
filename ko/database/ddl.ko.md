{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DDL 파일 형식과 DDL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"DDL 파일 형식 - 데이터 정의 언어 파일",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## .DDL 파일이란?

확장자가 .ddl인 파일은 데이터베이스의 스키마를 정의하는 데 사용되는 데이터 정의 언어 파일입니다. 여기에는 테이블, 열, 레코드 및 기타 필드와 같은 데이터베이스 구조 작업을 위한 명령문/명령이 포함됩니다. DDL 파일의 명령은 [SQL](/ko/database/sql/)로 작성되며 데이터베이스에 테이블 생성, 삭제 및 업데이트와 같은 작업을 수행할 수 있습니다. 데이터베이스 스키마는 생성된 스키마의 소유이며 모든 CRUD 작업을 수행할 수 있습니다. DDL 파일을 만들고 열 수 있는 인기 있는 응용 프로그램은 Windows Text Editor, Jetbrains Intellij Idea 및 EclipseLink입니다.

## DDL 명령

단일 DDL 파일에는 올바른 구문으로 인해 문자 집합 및 테이블 생성, 테이블 삭제, 테이블 이름 변경 및 변경과 같이 스키마를 변경하고 순서대로 실행하는 여러 명령이 포함될 수 있습니다. 다음 DDL 명령은 데이터베이스 스키마로 작업할 때 일반적으로 사용됩니다.

`CREATE` - 데이터베이스 또는 해당 객체(예: 테이블, 인덱스, 함수, 뷰, 저장 프로시저 및 트리거)를 생성하는 데 사용됩니다.

`DROP` – 데이터베이스에서 개체를 삭제하는 데 사용됩니다.

`ALTER` - 데이터베이스의 구조를 변경하는 데 사용됩니다.

`TRUNCATE` – 레코드에 할당된 모든 공간을 포함하여 테이블에서 모든 레코드를 제거하는 데 사용됩니다.

`COMMENT` – 데이터 사전에 주석을 추가합니다.

`RENAME` – 데이터베이스에 있는 기존 개체의 이름을 바꿉니다.

## DDL 예

다음 예는 테이블을 생성하고 해당 필드를 정의하는 CREATE 명령에 대한 DDL 문을 보여줍니다.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## 참조 ##

* [위키피디아의 DDL](https://en.wikipedia.org/wiki/Data_definition_language)

