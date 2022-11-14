{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - 보고서 정의 언어 클라이언트 측",
  "keywords" :[ "rdlc", "보고서 정의 언어", "mkv 형식", "XSD", "보고서 정의 언어 클라이언트 측"],
  "description":"SQL Server Reporting Services 보고서 정의의 XML 표현인 RDLC 파일 형식에 대해 알아보세요.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## .RDLC 파일이란? ##

RDLC는 보고서 정의 언어 클라이언트 측을 나타냅니다. 실은 마이크로소프트 리포팅 기술을 이용하여 생성한 리포트 파일의 확장자입니다. 보고서 디자이너의 SQL Server 2005 버전은 이러한 파일을 만드는 데 사용됩니다. 클라이언트 측의 **ReportViewer** 컨트롤은 RDLC 보고서를 직접 실행할 수 있습니다.

## RDL 대 RDLC 파일
|.rdl 파일 |.rdlc 파일|
---|---|
|RDL 파일은 SQL Server 2005 버전의 보고서 디자이너에서 생성됩니다.|RDLC 파일은 Visual Studio 2005 버전의 보고서 디자이너에서 생성됩니다.|
|SQL Server Reporting Services에서 사용됨|Visual Studio에서 사용됨|
|리모트 리포트입니다|로컬 리포트입니다|
|실행하려면 Reporting Services 인스턴스가 필요합니다|Reporting Services 인스턴스가 필요하지 않습니다|

## 클라이언트 보고서 정의(.rdlc) 파일 생성
ReportViewer 컨트롤은 컨트롤의 기본 제공 처리 기능을 사용하여 클라이언트 보고서 정의(.rdlc) 파일을 실행하는 데 사용됩니다. 로컬 처리 모드에서 실행하는 클라이언트 보고서는 애플리케이션 프로젝트에서 쉽게 생성할 수 있습니다. 보고서 작성 방법은 다음과 같습니다.

- **보고서 마법사**를 사용하여 새 클라이언트 보고서 정의(.rdlc)를 만듭니다.

- Visual Studio를 사용하여 새 클라이언트 보고서 정의(.rdlc) 파일을 만듭니다.

- 프로그래밍 방식으로 보고서 정의를 생성합니다.


**ReportViewer** 컨트롤에서 실행해야만 보고서를 미리 볼 수 있습니다. 언제든지 보고서 정의를 열고 편집한 다음 응용 프로그램을 빌드하거나 배포하여 결과를 확인할 수 있습니다.

## 참조 ##

- [클라이언트 보고서 정의(.rdlc) 파일 생성](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

