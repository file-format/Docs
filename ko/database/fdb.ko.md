{
  "date" : "2023-01-18",
  "keywords" :[ "FDB", "FDB 파일이란 무엇인가", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FDB 파일을 만들고 열 수 있는 FDB 파일 형식 및 API에 대해 알아봅니다.",
  "title" :"FDB 파일 형식 - Microsoft Dynamics NAV 데이터베이스 파일",
  "linktitle" : "FDB",
  "menu" : {
    "docs" : {
      "identifier":"database-fdb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-18"
}

## .FDB 파일이란?

.fdb 파일은 Microsoft Dynamics NAV의 데이터베이스 파일에 사용되는 파일 확장자입니다. .fdb 파일 확장자는 "Firebird Database File"의 약자이며 Microsoft Dynamics NAV에서 사용하는 기본 데이터베이스 엔진인 Firebird Database Management System에서 사용하는 파일 형식입니다. .fdb 파일에는 재무 데이터, 재고 데이터, 고객 데이터 등을 포함하여 NAV 시스템의 모든 데이터, 테이블 및 구조가 포함되어 있습니다. 데이터 무결성을 보장하고 문제 발생 시 데이터를 복구할 수 있도록 .fdb 파일의 백업을 유지하는 것이 중요합니다. .fdb 파일은 내보내고 가져올 수 있으며 복제에도 사용할 수 있습니다.

## Microsoft Dynamics NAV와의 관계

FDB 파일은 Microsoft Dynamics NAV의 데이터베이스 파일입니다. Microsoft Dynamics NAV는 Microsoft에서 개발한 ERP(Enterprise Resource Planning) 소프트웨어입니다. 중소기업용으로 설계되었으며 재무 관리, 공급망 관리, 제조, 프로젝트 관리 등을 포함한 광범위한 비즈니스 관리 기능을 제공합니다. Microsoft Dynamics 플랫폼을 기반으로 하며 Office 및 Outlook과 같은 다른 Microsoft 제품과 완벽하게 통합됩니다. Dynamics NAV는 Windows 클라이언트뿐만 아니라 웹 클라이언트를 통해 액세스할 수 있으며 C/AL이라는 자체 개발 환경을 사용하여 다른 시스템과 사용자 지정 및 통합할 수도 있습니다. 제조, 도매 유통 및 서비스 산업의 회사에서 일반적으로 사용합니다.

## .fdb 파일을 여는 방법?

FDB 파일은 일반적으로 Microsoft Dynamics NAV 개발 환경 또는 Microsoft Dynamics NAV 클라이언트를 사용하여 열고 관리합니다.

다음은 Microsoft Dynamics NAV에서 .fdb 파일을 여는 단계입니다.

1. Microsoft Dynamics NAV 개발 환경을 엽니다.
2. "파일" 메뉴를 클릭하고 "열기"를 선택하거나 "Ctrl+O"를 누릅니다.
3. .fdb 파일이 저장된 위치로 이동합니다.
4. .fdb 파일을 선택하고 "열기" 버튼을 클릭합니다.

NAV 클라이언트를 사용하여 데이터베이스에 연결하여 .fdb 파일을 열 수도 있습니다.

1. NAV 클라이언트를 엽니다.
2. "파일" 메뉴를 클릭하고 "연결"을 선택합니다.
3. "서버" 필드에 .fdb 파일이 있는 서버의 이름 또는 IP 주소를 입력합니다.
4. 적절한 "데이터베이스 이름" 및 "자격 증명"을 입력합니다.
5. "연결" 버튼을 클릭합니다.

Microsoft Dynamics NAV에서 사용하는 기본 데이터베이스 엔진인 Firebird 데이터베이스 관리 시스템 관리 소프트웨어로 .fdb 파일을 여는 것도 가능합니다.

## 참조
* [Microsoft Dynamics NAV](https://dynamics.microsoft.com/en-us/nav-erp/)
* [Dynamics NAV에서 새 데이터베이스 파일을 추가하는 방법](https://learn.microsoft.com/en-us/dynamics-nav/how-to--add-new-database-files)

