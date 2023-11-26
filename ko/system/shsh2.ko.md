{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 파일 - iOS SHSH Blob 파일 형식",
  "description":"SHSH2 파일이 무엇인지 알아보세요.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## .SHSH2 파일이란?

SHSH blob 또는 ECID SHSH라고도 하는 SHSH2 파일은 Apple에서 iPhone, iPad, iPod과 같은 iOS 장치의 펌웨어 업데이트를 인증하고 확인하는 데 사용하는 디지털 서명입니다. 여기에는 ECID(Exclusive Chip ID)라고 하는 장치의 고유 식별자가 포함되어 있습니다. 또한 장치에 설치된 펌웨어 버전에 대한 정보도 포함되어 있습니다.

## SHSH2 파일 형식 - 추가 정보

SHSH2 파일은 바이너리 파일 형식으로 디스크에 저장되며 이 파일 형식의 내부 파일 구조 세부 정보는 공개적으로 사용할 수 없습니다.

iPhone, iPad 또는 Mac과 같은 Apple 장치에 새 버전의 iOS가 설치되면 SHSH2 파일이 생성됩니다. 이 SHSH2 파일은 이 디지털 서명 파일을 읽고 확인하는 Apple 서버로 전송됩니다. 서버는 이 정보를 기반으로 설치를 허용하거나 금지합니다.

업데이트를 요청할 때도 마찬가지입니다. 사용자가 iTunes 또는 다른 소프트웨어를 통해 장치의 업데이트 또는 복원을 요청하면 Apple 서버는 업데이트를 진행하기 전에 SHSH2 파일이 장치의 ECID 및 펌웨어 버전과 일치하는지 확인합니다.

## 참고자료

* [SHSH Blob - Wikipedia 작성](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS 세이버](https://tsssaver.1conan.com/v2/)

