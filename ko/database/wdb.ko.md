{
  "date" : "2021-08-24",
  "keywords" :[ "wdb 파일", "wdb 파일 형식", "wdb 파일이란", "파일", "wdb 예제", "wdb 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WDB 파일 형식과 WDB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"WDB - SQL Server 추적 파일",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## .WDB 파일이란?
확장자가 .wdb인 파일은 실제로 데이터베이스 관리 시스템과 같은 기능을 수행하는 데 사용되는 Microsoft Works에서 만든 데이터베이스 파일입니다. WDB 파일은 Access Database([MDB](/ko/database/mdb/)) 파일과 유사하지만 효율성이 떨어지고 제한 사항이 더 큽니다. Microsoft Access를 사용하여 WDB 파일을 열 수 없습니다. 그러나 Microsoft Works에서 WDB 파일을 연 다음 MDB 파일로 내보내면 MS Access에서 WDB 파일을 열 수 있습니다.

## WDB 파일 형식
Microsoft Works 데이터베이스는 Microsoft Works 오피스 제품군의 기본 데이터베이스 형식입니다. 형식의 독점 특성과 몇 가지 제한 사항 때문입니다. WDB 파일은 Microsoft Works 이외의 다른 소프트웨어에서 열 수 없습니다. 파일 형식에서 NULL 값으로 종료된 필드 값을 나타내는 각 ASCII 텍스트 문자열 앞에 반복되는 10바이트 헤더가 있습니다. 헤더는 일반적으로 **\x0f** 바이트와 NULL로 시작하고 4개의 데이터 바이트가 NULL로 번갈아 가며 이어집니다.

### 파일 구조

WDB 파일의 구조는 다음과 같습니다.
- **첫 번째 헤더**: 파일 시작 부분에서 \x25\x00\xf2로 끝나는 244 NULL 바이트
- **두 번째 헤더**: \xffT - 즉, \xff\x54로 시작하고 열/필드 이름 및 기타 항목을 포함하는 4096바이트로 확장되며 바이트 위치 6144에서 시작하는 것으로 보입니다.
- **필드**: 값에 10바이트 헤더가 있으며 형식은 {유형 바이트} {유형 바이트, 부분 2} {데이터 바이트 1} \x00 {db 2} \x00 {db 3} {db 3 , 파트 2} {db 4} \x00. 데이터 바이트 2는 필드 번호이고 데이터 바이트 3은 레코드 번호입니다(데이터 바이트 3 추가, 256개 레코드를 초과할 때 파트 2).


## 참조 ##

* [사용자:JesseW/wdb 형식](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

