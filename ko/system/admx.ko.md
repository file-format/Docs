{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX 파일 - 그룹 정책 관리 템플릿 파일 형식",
  "description":"ADMX 파일 형식과 ADMX 파일을 여는 방법에 대해 알아보세요.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADMX 파일이란?

ADMX 파일은 그룹의 컴퓨터 그룹을 관리하는 Microsoft Windows 그룹 정책 소프트웨어에서 사용하는 정책 구성 파일입니다. 이는 XML 기반 관리 템플릿 파일이며 Windows Vista 서비스 팩 1에서 도입되었습니다. ADMX 파일에는 사용자 계정, 운영 체제 구성 및 응용 프로그램에 대한 구성 설정이 포함되어 있습니다. ADMX 파일은 많은 컴퓨터 시스템의 중앙 집중식 관리를 위한 구성을 저장하고 배포하는 데 사용됩니다.

XML 호환, 텍스트 편집기 또는 Microsoft 그룹 정책 개체 편집기를 사용하여 ADMX 파일을 만들거나 편집할 수 있습니다.

## ADMX 파일 형식 - 추가 정보

ADMX 파일은 사람이 읽을 수 있는 범용 [XML](/ko/web/xml/) 파일 형식으로 저장됩니다. 이는 다국어 파일 형식으로, 다양한 언어를 사용하는 시스템 관리자가 동일한 ADMX 파일로 작업할 수 있도록 해줍니다. ADMX 파일은 유니코드 형식의 텍스트 파일 형식인 이전 [ADM](/ko/system/adm/) 파일 형식을 대체했습니다. ADMX 파일은 특정 그룹 정책 설정이 변경될 때 변경되는 레지스트리 키를 지정합니다.

### ADMX 파일로 무엇을 할 수 있나요?

ADMX 파일은 그룹에 속한 사용자 컴퓨터에 허용되는 작업을 정의합니다. 그룹 정책은 Active Directory 소프트웨어와 함께 설정된 규칙을 적용합니다. ADMX 파일은 도메인의 중앙 위치인 Windows OS의 중앙 저장소에서 관리됩니다.

작업 환경에 배포된 ADMX 파일을 통해 관리자는 다음과 같은 정책을 구현할 수 있습니다.

* 인터넷 사용 통제
* 특정 유형의 파일 다운로드
* 시스템에서 이동식 장치 사용

## 참고자료

* [관리 템플릿 파일 - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 관리 템플릿 파일 관리](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

