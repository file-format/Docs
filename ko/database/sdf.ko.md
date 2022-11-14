{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf 파일","sdf 파일이란","sdf 파일을 여는 방법", "확장자", "파일", "sdf 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식 ", "데이터베이스 파일"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SDF 파일 형식과 SDF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"SDF - SQL Server Compact 데이터베이스 파일",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## .SDF 파일이란?
확장자가 .sdf인 파일에는 컴팩트 관계형 데이터베이스라고도 하는 Microsoft SQL Server Compact(SQL CE) 데이터베이스가 포함되어 있습니다. 모바일 장치 및 데스크톱용으로 만든 응용 프로그램을 위해 Microsoft에서 제작했습니다. 32비트 및 64비트 운영 체제를 모두 지원하며 데이터베이스의 전체 내용이 단일 SDF 파일에 포함되며 4GB 이상의 디스크 공간을 차지할 수 있습니다. 보안을 위해 .sdf 파일을 128비트 암호화로 암호화할 수 있습니다. SQL CE 런타임은 .sdf 파일에 대한 병렬 다중 사용자 액세스를 설정합니다. SDF 파일은 **QuickOnce**를 통해 복사하거나 단순히 시스템 배포를 위해 대상으로 복사할 수 있습니다.

## SDF 파일 형식
SDF 파일에는 일반적으로 컴팩트 관계형 데이터베이스라고 하는 데이터베이스가 포함되어 있습니다. SDF 파일에는 모든 데이터베이스 관련 정보가 포함되어 있으며 SQL Server Compact는 .sdf 파일을 관리하는 데 사용되는 경량의 무료 데이터베이스 엔진입니다. .sdf 파일 크기는 4GB 크기 제한을 초과해서는 안 됩니다. SDF 파일은 저장 프로시저, 트리거 또는 보기에 대한 정보를 저장하지 않습니다. SQL CE 데이터베이스를 사용하는 응용 프로그램은 ADO.NET 연결 문자열에서 SDF 파일에 대한 경로를 지정할 필요가 없습니다. 대신 |DataDirectory|\database_name.sdf로 언급되어 응용 프로그램의 어셈블리 매니페스트에 정의되는 데이터 디렉터리를 정의할 수 있습니다.
.sdf 명명 규칙은 선택 사항이며 모든 확장자를 사용하여 파일을 저장할 수 있습니다. 데이터베이스 파일에 대한 암호 설정은 선택적 단계입니다. 데이터베이스를 압축하거나 복구하려면 **compacted/repaired database** 옵션으로 파일을 저장해야 합니다.

## 참고문헌

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [ASP.NET 웹 응용 프로그램에 SQL Server Compact 사용](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


