{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "ABCDDB 파일이란?", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ABCDDB 파일을 만들고 열 수 있는 ABCDDB 파일 형식 및 API에 대해 알아봅니다.",
  "title" :"ABCDDB 파일 형식 - Apple 주소록 연락처 목록 데이터베이스 파일",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## .ABCDDB 파일이란?

확장자가 **.ABCDDB**인 파일은 Apple 주소록 연락처 목록 데이터베이스를 나타냅니다. 일반적으로 **연락처**라고도 하는 **주소록** 응용 프로그램에 속합니다. 내장형 애플리케이션이며 iOS 및 macOS 운영 체제에 포함되어 있습니다. 연락처 응용 프로그램을 사용하면 개인, 기업 및 조직을 포함하여 연락처와 관련된 정보를 저장하고 구성할 수 있습니다. 이 앱을 통해 사용자는 이름, 주소, 전화번호 및 이메일 주소와 같은 세부 정보를 추적하고 연락처를 그룹으로 분류할 수 있습니다.

## SQLite와의 관계 및 일반적인 경로

Apple의 주소록(연락처라고도 함)은 연락처 정보를 메타데이터 폴더에 vCard로 저장합니다. **파일 _ABCDDB_는 실제로 _SQLite 3 datafile_**입니다.

SQLite는 가볍고 독립형으로 설계된 널리 사용되는 데이터베이스 관리 시스템입니다. 다양한 유형의 소프트웨어 및 장치에서 사용됩니다. SQLite는 RDBMS의 한 유형으로 키를 통해 서로 관련된 테이블에 데이터를 저장합니다. 정수, 부동 소수점 숫자, 문자열 및 이진 데이터를 포함한 다양한 데이터 유형을 처리할 수 있습니다. 또한 SQLite는 사용자가 단일 작업 단위로 여러 데이터베이스 작업을 함께 수행할 수 있는 트랜잭션을 지원합니다.

확장자가 ABCDDB인 파일은 일반적으로 여기에 저장됩니다.

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## 손상된 연락처 데이터베이스 수정

이 작업을 시도하기 전에 먼저 백업을 수행하십시오. 그런 다음 다음으로 이동하십시오.

`~/라이브러리/응용 프로그램 지원/주소록`

해당 디렉토리에서 확장자가 .abcddb인 파일을 포함하여 세 개의 파일을 찾을 수 있습니다.

- `주소록-v22.abcddb`
- `주소록-v22.abcddb-wal`
- `주소록-v22.abcddb-shm`

이 파일을 모두 삭제하고 연락처를 다시 열면 다시 작동합니다.

## 백업에서 주소록 데이터베이스 복원

주소록 데이터베이스 연락처가 `addressbook-v22.abcddb`에 저장되어 있다고 가정합니다.

- 먼저 주소록 데이터를 백업하고 모든 응용 프로그램을 종료하십시오.
- 데이터베이스 파일을 `~/Library/Application Support/AddressBook` 하위 디렉토리로 이동합니다.
- **주소록.앱**을 실행합니다.

## ABCDDB 파일 데이터를 Microsoft Access로 내보내기

파일은 SQLite 3 데이터 파일이므로 ODBC 커넥터를 사용하여 abcddb 파일 내의 데이터를 Microsoft Access로 내보낼 수 있습니다.

SQLite ODBC 커넥터는 ODBC 인터페이스를 지원하는 응용 프로그램이 SQLite 데이터베이스에 연결할 수 있도록 하는 소프트웨어 라이브러리 및 드라이버입니다. 여기에는 ODBC 인터페이스를 정의하는 라이브러리와 이 인터페이스를 SQLite API에 대한 호출로 변환하는 드라이버가 포함됩니다. SQLite ODBC 커넥터를 사용하려면 먼저 설치한 다음 컴퓨터에 ODBC 데이터 소스를 설정해야 합니다. 이 단계를 완료한 후 ODBC 지원 기능이 있는 모든 응용 프로그램은 데이터 원본에 연결하고 SQLite 데이터베이스에서 데이터를 검색할 수 있습니다.

## 참조
* [손상된 연락처 데이터베이스 수정](https://discussions.apple.com/docs/DOC-10581)
* [Mac용 연락처 데이터베이스](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [Windows 7 Excel에서 abcddb 파일을 열거나 내보내려면 어떻게 해야 합니까?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file- in-windows-7-엑셀)

