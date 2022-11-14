{
  "date" : "2021-08-11",
  "keywords" :[ "wim 파일", "wim 파일 형식", "wim 파일이란", "파일", "wim 예", "wim 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"WIM 파일을 만들고 열 수 있는 WIM 파일 형식 및 API에 대해 알아보세요.",
  "title" :"WIM - Windows 이미징 형식 파일",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## .WIM 파일이란?
.wim 확장자를 가진 파일은 Windows Vista에서 처음으로 나타났습니다. WIM은 일반적으로 Microsoft Windows Vista에 도입된 파일 기반 이미징 형식에 속합니다. 단일 디스크 이미지를 다양한 컴퓨터 플랫폼에 배포할 수 있습니다. WIM 파일은 운영 체제 이미지를 다시 부팅하지 않고 업데이트, 드라이버 및 구성 요소와 같은 파일을 관리하는 데 사용됩니다. AQ WIM 파일에는 다른 디스크 파일 형식과 매우 유사한 파일 및 관련 메타데이터 세트가 포함되어 있습니다.

## WIM 파일 형식
WIM 파일 형식은 VHD 또는 IS와 같은 섹터 기반 형식과 달리 WIM의 기본 정보 단위가 파일이라는 사실을 의미하는 파일 기반입니다. 파일 기반의 기본적인 이점은 파일 시스템 트리에서 여러 번 참조되는 파일의 단일 인스턴스 저장소와 하드웨어 독립성입니다. 파일이 단일 WIM 내부에 저장되기 때문에 다양한 파일을 개별적으로 열고 닫는 오버헤드를 줄입니다. 파일. WIM 파일은 고유한 이름이나 숫자 인덱스로 참조되는 여러 디스크 이미지를 저장할 수 있습니다.
### 압축 알고리즘 지원
WIM은 내림차순 속도 및 오름차순 비율로 다음 압축 알고리즘 제품군을 지원합니다.
- XPRESS
- LZX
- LZMS
- 고체 압축.
처음 세 제품군은 LZ77 기반이며 Solid-compression은 WIMGAPI Windows 8 및 DISM Windows 8.1에서 LZMS와 함께 도입되었습니다.
### WIM 파일 형식용 도구
다음 도구는 일반적으로 WIM 파일 형식을 지원합니다.

- **ImageX**: Windows 이미징 형식으로 Windows 디스크 이미지를 편집, 생성 및 배포하는 데 사용되는 명령줄 도구입니다. 관련 WIMGAPI와 함께 무료 Windows 자동 설치 키트의 일부로 배포됩니다. Windows Vista부터 Windows 설치 프로그램은 WAIK API를 사용하여 Windows를 설치합니다.
- **DISM**: Windows 설치 이미지에 대해 서비스 관련 작업을 수행할 수 있는 Windows 7 및 Windows Server 2008 R2에 도입된 도구(온라인 이미지 또는 폴더 또는 WIM 파일 내의 오프라인 이미지). 이 도구는 이미지를 마운트 및 마운트 해제하고, 오프라인 이미지에 장치 드라이버를 추가하고, 오프라인 이미지에 설치된 장치 드라이버를 쿼리할 수 있었습니다.
 




## 참고문헌


* [Windows 이미징 형식 - Wikipedia 제공](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


