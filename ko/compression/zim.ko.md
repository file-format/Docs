{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM 파일 형식 - OpenZIM 아카이브 파일",
  "description":"ZIM 파일 형식과 ZIM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## .ZIM 파일이란? ##

확장자가 .zim인 파일은 Wiki 콘텐츠를 오프라인으로 저장하기 위해 생성된 아카이브입니다. Wikipedia를 USB에 저장하는 데 가장 적합한 개방형 파일 형식으로 간주됩니다. 사이트 콘텐츠를 컴팩트한 형식으로 저장합니다. 그 이름은 이전 Zeno 파일 형식인 "Zeno IMproved"에서 따왔습니다. ZIM은 Wikimedia CH에서 후원하고 Wikimedia Foundation에서 지원하는 [openZIM ](https://openzim.org/)project에서 관리합니다. ZIM 파일은 Kiwix 및 ZIMReader와 같은 응용 프로그램에서 열 수 있습니다. OpenZIM 프로젝트는 OpenSource 커뮤니티의 기여를 위해 [Github](https://github.com/openzim)에서 ZIM 파일 형식 구현을 호스팅했습니다.

## ZIM 파일 형식 사양

ZIM 파일 형식은 [Zeno 파일 형식](https://openzim.org/wiki/Zeno_file_format)을 기반으로 개발되었으며 이전 버전과 호환되지 않습니다. ZIM 파일 형식의 형식 사양은 개발자 참조용으로 openZIM의 [온라인에서 사용 가능](https://openzim.org/wiki/ZIM_file_format)입니다. OpenZIM은 ZIM 파일을 읽고 쓸 수 있도록 C++ 오픈 소스 구현인 [LibZim](https://openzim.org/wiki/Zimlib)을 제공했습니다.

ZIM 파일 형식은 LZMA2 압축을 사용하여 콘텐츠를 압축합니다.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM 파일 형식" >}}


### ZIM 헤더

ZIM 파일은 오프셋 0에 있는 헤더로 시작합니다. 모든 구성 요소는 리틀 엔디안을 기반으로 하며 모든 정수는 부호 없는 정수(예: uint_16, uint_32, uint_64)입니다.

|필드 이름 |유형| 오프셋| 길이| 설명|
---|---|---|---|---|
|매직넘버| 정수| 0| 4| 파일 형식을 인식하는 매직 넘버는 72173914(0x44D495A)|
|주 버전| 정수| 4| 2| ZIM 파일 형식의 주요 버전(5 또는 6)|
|마이너 버전| 정수| 6| 2| ZIM 파일 형식의 부 버전|
|uuid| 정수| 8| 16| 이 zim 파일의 고유 ID|
|기사 수| 정수| 24| 4| 총 기사 수|
|클러스터 수| 정수| 28| 4| 총 클러스터 수|
|urlPtrPos| 정수| 32| 8| URL로 정렬된 디렉토리 포인터 목록의 위치|
|제목PtrPos| 정수| 40| 8| Title|에 의해 정렬된 디렉토리 포인터 목록의 위치
|클러스터 PtrPos| 정수| 48| 8| 클러스터 포인터 목록의 위치|
|mimeListPos| 정수| 56| 8| MIME 유형 목록의 위치(헤더 크기도 포함)|
|메인페이지| 정수| 64| 4| 메인 페이지 또는 메인 페이지가 없으면 0xffffffff|
|레이아웃 페이지| 정수| 68| 4| 레이아웃 페이지 또는 레이아웃 페이지가 없는 경우 0xffffffffff|
|체크섬포스| 정수| 72| 8| 체크섬 자체가 없는 이 파일의 md5checksum에 대한 포인터입니다. 이것은 항상 파일 끝 16바이트를 가리킵니다.|

## 참조 ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

