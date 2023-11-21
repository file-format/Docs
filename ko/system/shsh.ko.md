{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH 파일 - iPhone/iPod Touch SHSH Blob 파일 형식",
  "description":"SHSH 파일이 무엇인지 알아보세요.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## .SHSH 파일이란?

Signature HaSH라고도 알려진 SHSH 파일은 Apple이 iPhone, iPad, iPod과 같은 iOS 장치의 펌웨어 업데이트를 인증하고 확인하는 데 사용하는 디지털 서명입니다.

## SHSH와 SHSH2 파일 형식의 차이점

SHSH2 파일과 마찬가지로 SHSH 파일에는 "ECID"(독점 칩 ID)라는 장치의 고유 식별자와 장치에 설치된 펌웨어 버전에 대한 정보가 포함되어 있습니다. 그러나 SHSH 파일은 이전 버전의 iOS(iOS 10 이전)에서 사용되었으며 이후 SHSH2 파일로 대체되었습니다.

## SHSH 파일 형식 - 추가 정보

SHSH 파일은 바이너리 파일 형식으로 디스크에 저장됩니다. 이 파일 형식의 내부 파일 구조 세부정보는 공개적으로 제공되지 않습니다.

SHSH 파일은 장치의 펌웨어를 Apple에서 더 이상 서명하지 않는 이전 버전으로 다운그레이드하려는 사용자에게 중요합니다. Apple에서 아직 서명 중인 특정 펌웨어 버전에 대해 SHSH 파일을 저장하면 사용자는 나중에 이 파일을 사용하여 Apple의 서명 확인을 우회하고 해당 펌웨어 버전을 장치에 설치할 수 있습니다. 이 과정을 '탈옥'이라고도 합니다.

## 참고자료

* [SHSH Blob - Wikipedia 작성](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS 세이버](https://tsssaver.1conan.com/v2/)

