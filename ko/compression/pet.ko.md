{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET 파일 형식 - Puppy Linux 설치 패키지 파일",
  "description":"PET 파일 형식과 PET 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Linux PET 파일이란?

PET 파일은 Linux 운영 체제의 PuppyLinux 변형과 함께 생성되고 사용되는 응용 프로그램 설치 패키지 파일입니다. 압축된 아카이브의 파일 크기를 줄이는 압축된 [TGZ](/ko/compression/tgz/) 파일로 생성됩니다. PET 파일 형식의 무결성은 원격 끝에서 확인을 위해 파일 끝에 추가되는 md5sum 체크섬에 의해 보장됩니다. PET 파일은 표준 TGZ 파일 추출기와 WinRAR를 사용하여 추출할 수 있습니다. PET 파일은 이전 [PUP](/ko/compression/pup/) 패키지 설치 파일을 대체했습니다.

## PET 파일 형식

PET 파일은 바이너리 파일 형식의 압축 아카이브로 디스크에 저장됩니다. 그러나 PET 파일 형식의 내부 파일 형식 세부 정보는 알려져 있지 않습니다. [.exe](/ko/executable/exe/) 및 [.msi](/ko/executable/msi/) 패키지 설치 파일과 유사하게 PET 파일은 실행될 때 설치를 시작합니다.

## 참고문헌

* [퍼피리눅스](https://en.wikipedia.org/wiki/Puppy_Linux)
* [PuppyLinux PET 패키지 색인](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

