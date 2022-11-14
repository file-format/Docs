{
  "date" : "2021-08-13",
  "keywords" :[ "sdi 파일", "sdi 파일 형식", "sdi 파일이란", "파일", "sdi 예제", "sdi 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"SDI 파일을 만들고 열 수 있는 SDI 파일 형식과 API에 대해 알아보세요.",
  "title" :"SDI - Windows 시스템 배포 이미지 파일",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## .SDI 파일이란?
확장자가 .sdi인 파일에는 로드 blob, 부트 blob 및 부분 blob이 포함됩니다. 일반적으로 Windows Embedded Studio에서 Windows 로드 및 설치를 위한 RAM 디스크 또는 부팅 디스크를 만드는 데 사용합니다. SDI는 시스템 배포 이미지의 약어입니다. Windows Embedded Studio는 Windows용 디스크 이미지를 만드는 데 사용되는 프로그램입니다. 실제로 이 프로그램에는 SDI 파일 관리자 프로그램과 **sdimgr.exe**라는 명령줄 도구가 포함되어 있으며 둘 다 SDI 이미지를 적용, 생성 및 편집하는 데 사용할 수 있습니다.

## SDI 파일 형식
SDI 파일 형식은 시스템 부팅을 위한 가상 디스크 사용을 가능하게 하는 데 널리 사용됩니다. 일부 Microsoft Windows 버전은 **RAM 부팅**을 활성화합니다. 이는 SDI 파일을 메모리에 로드한 다음 부팅하는 데 중요합니다. SDI 파일 형식은 PXE(Preboot Execution Environment)를 사용하여 네트워크 부팅도 가능합니다. 또한 하드 디스크 이미징에도 사용됩니다.
### SDI 파일 섹션
SDI 파일 자체는 다음 섹션으로 나눌 수 있습니다.
- **Boot BLOB**: 실제 부팅 프로그램인 STARTROM.COM이 포함되어 있습니다. 이것은 하드 디스크의 부트 섹터와 유사합니다.
- **Load BLOB**: 일반적으로 NTLDR을 포함하며 부팅 BLOB에 의해 시작됩니다.
- **파트 BLOB**: 여기에는 실제 부팅 런타임이 포함됩니다. 또한 런타임의 루트 디렉토리에 있어야 하는 boot.ini 및 ntdetect.com 파일도 포함합니다.
- **디스크 BLOB**: MBR로 시작하는 플랫 HDD 이미지입니다. 부팅 대신 하드 드라이브 이미징에 사용됩니다. 또한 디스크 BLOB만 Microsoft 유틸리티로 탑재할 수 있습니다.


## 참고문헌

* [시스템 배포 이미지 - Wikipedia 제공](https://en.wikipedia.org/wiki/System_Deployment_Image)


