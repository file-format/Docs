{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ADE 파일 형식과 ADE 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"ADE - 액세스 프로젝트 확장 파일",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## .ADE 파일이란?

확장명이 .ade인 파일은 Microsoft Access ADP 프로젝트 파일에 포함된 정보의 컴파일된 출력을 포함하는 Microsoft Access 프로젝트 파일입니다. VBA(Visual Basic for Applications) 이외의 Access 프로젝트 파일에 있는 정보는 ADE 파일에서 컴파일된 형식으로 사용할 수 있습니다. 데이터는 이러한 파일에 압축된 형식으로 저장되어 파일 크기를 줄이고 Access의 성능을 향상시킵니다. ADE는 Access 프로젝트 파일의 컴파일된 출력이므로 프로젝트의 일부인 VBA 소스 코드는 출력의 일부가 되지 않도록 하여 보호된 상태로 유지됩니다. ADE 파일은 Microsoft Access 365에서 열 수 있습니다.

## ADE 파일 형식 - 추가 정보

ADE는 이진 파일로 디스크에 저장되는 컴파일된 액세스 데이터베이스 파일입니다. 이러한 파일의 내부 파일 구조는 알려져 있지 않습니다.

ADE 파일은 이러한 파일을 만드는 데 사용된 Microsoft Access 버전을 기반으로 열 때 문제를 일으킬 수 있습니다. 64비트 버전의 Microsoft Access 2010을 사용하고 MDE, [ACCDE](/ko/database/accde/) 또는 ADE 파일로 컴파일된 Access 데이터베이스는 Microsoft Access 2021 서비스 팩 1(SP1)에서 다음을 위해 다시 컴파일해야 합니다. Access 2010 SP1에서 제대로 작동합니다. 이 문제는 Access 2010 SP1이 최신 버전의 VBE7.dll 파일(버전 7.00.1619)을 사용하기 때문에 발생합니다.

## 참고문헌

* [Access ADE 파일 관련 문제](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [사용할 액세스 파일 형식](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

