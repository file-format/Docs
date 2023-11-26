{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM 파일 - 관리 템플릿 파일 형식",
  "description":"ADM 파일 형식과 ADM 파일을 여는 방법에 대해 알아보세요.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADM 파일이란?

ADM 파일은 Microsoft 그룹 정책 소프트웨어에서 레지스트리 파일의 레지스트리 기반 정책 설정 위치를 지정하는 데 사용되는 템플릿 파일입니다. 이는 시스템 관리자가 그룹에 속한 컴퓨터 그룹을 관리하기 위한 정책을 정의하는 데 사용됩니다. 이 정보는 그룹 관리를 위해 생성된 GPO(그룹 정책 개체)의 일부가 됩니다.

Microsoft 그룹 정책 개체 편집기를 사용하여 ADM 파일을 열 수 있습니다.

## ADM 파일 형식 - 추가 정보

ADM 파일은 유니코드 형식의 텍스트 파일로 저장됩니다. 이는 주로 Windows Vista 및 Windows 7 레지스트리에서 레지스트리 기반 정책 설정의 위치를 설명하는 데 사용되었습니다.

ADM 파일은 더 이상 지원되지 않으며 [ADMX](/ko/system/admx/) 파일로 대체되었습니다. GPA는 Microsoft Windows Vista 서비스 팩 1 이상을 실행하는 컴퓨터에서 다음 기본 ADM 파일을 무시합니다.

* 시스템.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## 참고자료

* [관리 템플릿 파일 - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 관리 템플릿 파일 관리](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

