{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "DSN 파일이란 무엇입니까?", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DSN 파일을 만들고 열 수 있는 DSN 파일 형식 및 API에 대해 알아봅니다.",
  "title" :"DSN 파일 형식 - 데이터베이스 소스 이름 파일",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## .DSN 파일이란?

DSN은 "데이터 원본 이름"을 나타내며 데이터베이스 연결 정보를 저장하는 데 사용되는 파일 형식입니다. DSN 파일은 일반적으로 ODBC(개방형 데이터베이스 연결)와 함께 사용되며 서버 이름, 사용자 이름 및 암호와 같은 연결에 필요한 정보를 제공하여 특정 데이터베이스에 쉽게 액세스할 수 있도록 합니다. 파일은 일반적으로 일반 텍스트로 되어 있으며 텍스트 편집기를 사용하여 만들고 편집할 수 있습니다. Windows, Linux 및 Mac과 같은 다양한 운영 체제에서 사용할 수 있습니다.

## DSN 파일을 만드는 방법?

DSN 파일을 만드는 방법은 사용 가능한 운영 체제 및 도구에 따라 다를 수 있습니다. 다음 단계는 Windows 시스템에서 DSN 파일을 만드는 프로세스의 일반적인 개요를 제공합니다.

1. 시작 메뉴에서 "ODBC 데이터 원본"을 검색하여 ODBC 데이터 원본 관리자를 엽니다.
2. "시스템 DSN" 탭을 선택하고 "추가" 버튼을 클릭합니다.
3. 연결할 데이터베이스에 적합한 드라이버를 선택하고 "마침"을 클릭합니다.
4. 서버 이름, 사용자 이름 및 암호와 같이 데이터베이스에 연결하는 데 필요한 정보를 입력합니다.
5. "확인"을 클릭하여 DSN 파일을 저장합니다.

또는 확장자가 .dsn인 일반 텍스트 파일을 만들고 필요한 연결 정보를 다음 형식으로 입력하여 DSN 파일을 수동으로 만들 수 있습니다.

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

그런 다음 이 파일의 경로를 코드/스크립트의 DSN으로 사용하여 데이터베이스에 연결할 수 있습니다.

## DSN 파일을 여는 프로그램

DSN 파일은 서버 이름, 사용자 이름 및 암호와 같이 데이터베이스에 연결하는 데 사용되는 정보를 저장하는 일반 텍스트 파일입니다. 일반적으로 ODBC(Open Database Connectivity)와 함께 사용되어 특정 데이터베이스에 쉽게 액세스할 수 있습니다.

DSN 파일의 내용을 열고 보려면 메모장, Sublime Text, Atom 등과 같은 텍스트 편집기를 사용할 수 있습니다. 이러한 프로그램을 사용하면 DSN 파일을 열고 파일에 저장된 연결 정보를 볼 수 있습니다.

그러나 DSN 파일을 사용하여 데이터베이스에 연결하고 SELECT, INSERT, UPDATE, DELETE 등과 같은 작업을 실행하려면 Python, Java, C#과 같은 프로그래밍 언어 또는 Microsoft Access와 같은 데이터베이스 관리 도구와 같은 ODBC 지원 프로그램이 필요합니다. , SQL Server Management Studio가 필요합니다. 이러한 프로그램은 DSN 파일의 정보를 사용하여 데이터베이스에 연결하고 원하는 작업을 수행할 수 있습니다.

## 참조
* [DSN(데이터 원본 이름)이란 무엇입니까?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)
* [ODBC 가져오기의 데이터 소스로 사용할 파일 DSN을 어떻게 생성합니까?](https://www.ibm.com/support/pages/how-do-i-create-file-dsn-use-data- 소스-odbc-가져오기)

