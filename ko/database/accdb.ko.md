{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDB 파일 형식과 ACCDB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"ACCDB 파일 형식 - Microsoft Access 2007 데이터베이스 파일",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## .ACCDB 파일이란?

확장자가 .accdb인 파일은 사용자 데이터를 테이블에 저장하는 Microsoft Access 2007 데이터베이스 파일입니다. 수납 대응
사용자 정의 양식, SQL 쿼리 및 기타 데이터. ACCDB 파일은 Microsoft가 XML 기반 파일 구조로 전환한 후 [MDB](/ko/database/mdb/) 파일을 대체했습니다. ACCDB 파일은 여전히 이전 호환성을 가진 MDB로 변환할 수 있습니다. 그러나 ACCDB는 현재 널리 사용되는 Access 데이터베이스 파일 형식입니다. Microsoft는 또한 첨부 파일 저장 가능성, 이진 데이터 및 다중 값 필드 지원과 같은 ACCDB 형식의 추가 기능을 지원했습니다.

## ACCDB 파일 형식

MDB와 마찬가지로 ACCDB 파일 형식에 사용할 수 있는 공개 사양이 없습니다. Microsoft는 ODBC(Open Database Connectivity) 표준 및 VBA(Visual Basic for Applications)를 통해 프로그래밍 방식으로 이러한 파일에 액세스하는 것을 지원합니다.

### 통찰력

간단한 ACCDB 파일의 16진 덤프는 이전 MDB 형식 제품군의 최신 버전과 구조가 일반적으로 유사함을 나타냅니다. 두 파일 형식 모두 4096바이트의 고정 페이지 크기를 사용합니다. ACCDB와 MDB의 또 다른 유사점은 ACCDB에 대한 "Standard ACE DB" 문자열을 포함하는 매직 넘버 형식입니다. 버전 또는 호환성 코드는 두 형식 모두에서 동일한 위치에 있습니다. mdbtools | HACKING 파일은 "Offset 0x14에는 이 데이터베이스의 Jet 버전이 포함되어 있습니다"라고 명시되어 있으며 비공식 MDB 가이드도 동의합니다. [Microsoft Jet 데이터베이스 엔진](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)에 대한 Wikipedia 항목과 결합된 이러한 소스의 정보는 0x02 값이 ACE 12(Access 2007)를 나타내고 0x03 값이 ACE를 나타냄을 시사합니다. 14(액세스 2010). 그러나 Access 2010에서 만든 최소 데이터베이스와 Access 2016에서 만든 유사한 데이터베이스 모두 이 위치에 0x02가 있습니다. Access 2016에서 생성되었지만 새로 도입된 "큰 정수" 데이터 형식으로 열을 정의하는 최소 데이터베이스의 값은 0x05입니다. ACCDB 파일에서 이 표시기는 파일을 만드는 데 사용된 ACE 엔진 버전이 아니라 파일의 호환성을 반영하는 것으로 보입니다.

## 참고문헌

* [액세스 2016 사양](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [마이크로소프트 젯 데이터베이스 엔진](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [어떤 Access 파일 형식을 사용해야 하나요?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
