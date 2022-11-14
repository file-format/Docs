{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "확장자", "udl 파일", "udl 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "udl 파일이란" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"UDL 파일 형식과 UDL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"UDL - Microsoft 범용 데이터 링크 파일",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## .UDL 파일이란?
확장자가 .udl인 파일을 Microsoft Universal Data Link 파일이라고 합니다. 연결 속성 지정; Windows 앱에서 데이터베이스와의 연결을 설정하는 데 사용합니다. UDL 파일에는 OLE DB 데이터 원본에 대한 연결 문자열이 포함되어 있습니다. 사용자 이름과 암호 및 필수 연결 문자열 속성을 사용합니다. 연결 문자열에서 직접 속성을 지정하는 것을 방지하기 위해 데이터 연결 속성 대화 상자를 사용하여 연결 정보를 .udl 파일에 저장할 수 있습니다.

## UDL 파일 형식
기본적으로 UDL(Universal Data Link) 파일은 특정 속성이나 속성이 있는 데이터베이스 연결 문자열로 구성된 간단한 텍스트 파일입니다. UDL 파일이 생성되면 SQL Server Management Studio를 사용하여 연결을 확인하여 테스트할 수 있습니다.

### 연결 문자열 속성
적절한 연결을 보장하기 위해 다음 속성을 UDL에 설정할 수 있습니다.

- **서버 이름**: 액세스하려는 데이터베이스가 있는 서버의 위치입니다.
- **인증 옵션**
- **Windows 인증**: 현재 로그인한 사용자의 Windows 계정 자격 증명을 사용하여 SQL Server에 인증합니다.
- **SQL Server 인증**: 로그인 아이디와 비밀번호를 이용한 인증입니다.
- **Active Directory - 통합**: Azure Active Directory ID를 사용한 통합 인증. SQL Server에 대한 Windows 인증에도 사용할 수 있습니다.
- **Active Directory - 암호**: Azure Active Directory ID를 사용한 사용자 ID 및 암호 인증입니다.
- **Active Directory - MFA 지원이 포함된 범용**: Azure Active Directory ID를 사용한 대화형 인증입니다.
- **Active Directory - 서비스 주체**: Azure Active Directory 서비스 주체를 사용한 인증입니다.
- **서버 SPN**: 신뢰할 수 있는 연결을 사용하는 경우 서버의 SPN(서비스 사용자 이름)을 지정할 수 있습니다.
- **사용자 이름**: 데이터 소스에 로그인할 때 인증에 사용할 사용자 ID를 입력합니다.
- **비밀번호**: 데이터 소스에 로그인할 때 인증에 사용할 비밀번호를 입력합니다.
- **Blank password**: 선택하면 지정된 공급자가 연결 문자열에서 빈 비밀번호를 사용할 수 있습니다.
- **비밀번호 저장 허용**: 연결 문자열과 함께 비밀번호 저장을 허용합니다.
- **데이터에 강력한 암호화 사용**: 연결을 통해 전달되는 데이터가 암호화됩니다.
- **신뢰 서버 인증서**: 서버의 인증서가 검증됩니다.
- **데이터베이스**: 접근하려는 데이터베이스 이름입니다.
- **데이터베이스 파일을 데이터베이스 이름으로 첨부**: 연결 가능한 데이터베이스의 기본 파일 이름을 지정합니다.

## 참조 ##

* [Microsoft 데이터 액세스 구성 요소](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [UDL(Universal Data Link) 구성](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

