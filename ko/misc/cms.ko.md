{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS 파일 형식 - 연결 관리자 서비스 프로필 파일",
  "description":"CMS 파일을 만들고 열 수 있는 CMS 파일 및 API에 대해 알아보세요.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## .CMS 파일이란?

CMS 파일은 Microsoft Windows 연결 관리자에서 사용하는 프로필 정보가 포함된 데이터 파일입니다. 원격 사용자가 이 프로필 정보를 사용하여 네트워크에 연결할 수 있습니다. CMS 파일 내부에 저장된 정보에는 원격 사용자와 네트워크 간의 연결을 설정하는 데 사용되는 사용자의 운영 체제 및 권한에 대한 데이터가 포함됩니다. CMS 관리자는 CMAK(연결 관리자 관리자 키트)를 사용하여 CMS 파일을 생성합니다.

## CMS 파일 형식 - 추가 정보

CMS 파일은 일반적으로 사용자 컴퓨터에서 찾을 수 없습니다. 이들은 원격 사용자가 네트워크에 접속할 수 있도록 특별히 사용되기 때문에 회사 네트워크나 특정 목적으로 구축된 사무실에 연결하는 데 사용되는 컴퓨터에서 찾을 수 있습니다. 대부분의 경우 회사 전용 VPN(가상 사설망)과 같은 조직 네트워크에 연결하는 데 사용됩니다. 네트워크 관리자는 원격 위치에서 회사 네트워크에 액세스할 수 있도록 연결 관리자를 사용하여 이러한 네트워크에 대한 액세스를 설정합니다.

### 인디 CMS가 무엇인가요?

CMS 프로필 파일은 연결 관리자를 사용하여 생성되며 원격 사용자에게 제공되기 전에 다른 구성 파일과 함께 패키징됩니다. 이러한 추가 파일에는 [EXE](/ko/executable/exe/) 파일과 함께 패키지되는 CMP 및 INF 파일이 포함될 수 있습니다. 이 완전한 패키지는 네트워크 연결을 위해 원격 사용자에게 제공됩니다.

## 참고문헌

* [Windows 연결 관리자 이해 및 구성](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

