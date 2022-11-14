{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK 파일 형식",
  "description":"NPK 파일 형식과 NPK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## .NPK 파일이란?

NPK 파일은 **MikroTik** 라우터에서 라우터 운영 체제 업그레이드를 위해 사용하는 소프트웨어 업그레이드 패키지 파일입니다. 소프트웨어 업데이트를 설치하기 위해 라우터에 로드되는 압축된 바이너리 아카이브로 제공됩니다. NPK 파일 내부에 포함된 정보에는 IP 주소 및 IP 서비스, 커넥터 정보(이더넷 인터페이스 및 직렬 포트), 이메일 설정, 브리지 구성 및 로컬 사용자 관리와 같은 네트워킹 정보가 포함됩니다.

## NPK 파일 형식

NPK 파일은 압축된 바이너리 아카이브로 저장됩니다. MikroTik 자체에서만 사용하는 닫힌 파일 형식입니다. 타사를 통해 RouterOS 추가 기능을 생성하기 위한 것이 아닙니다. NPK 파일은 MikroTik 자체에서 관리하며, 업그레이드 버전은 [MikroTik](https://mikrotik.com/download) 웹사이트의 다운로드 섹션에서 다운로드할 수 있습니다.

NPK 파일이 라우터에 업로드되면 라우터 OS는 재부팅하지 않는 한 적용되지 않습니다. 따라서 라우터 OS를 업그레이드하기 위해서는 재시작이 필요합니다.

## 참고문헌

* [MikroTik - 라우터 OS 업그레이드](https://mikrotik.com/download)
* [NPK 파일 생성 방법](https://forum.mikrotik.com/viewtopic.php?t=87126)

