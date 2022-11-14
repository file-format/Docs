{
  "date" : "2019-10-11",
  "keywords" :[ "wmf 파일", "wmf 파일 형식", "wmf 파일이란", "파일", "wmf 예제", "wmf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows 메타파일 형식",
  "description":"WMF 파일을 만들고 열 수 있는 WMF 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .WMF 파일이란?

WMF 확장자를 가진 파일은 벡터 및 비트맵 형식 이미지 데이터를 저장하기 위한 Microsoft WMF(Windows 메타파일)를 나타냅니다. 더 정확하게 말하면 WMF는 장치 독립적인 그래픽 파일 형식의 벡터 파일 형식 범주에 속합니다. Windows GDI(그래픽 장치 인터페이스)는 WMF 파일에 저장된 기능을 사용하여 화면에 이미지를 표시합니다. EMF(Enhanced Meta Files)라고 하는 보다 향상된 WMF 버전이 나중에 게시되어 형식이 더욱 풍부해졌습니다. 실제로 WMF는 SVG와 유사합니다.

## WMF 파일 형식 사양 ##

WMF 파일은 Windows 3.0과 함께 출시될 당시 16비트 파일 형식을 나타냅니다. 파일 형식은 그래픽 그리기 명령, 개체 정의 및 속성이 포함된 일련의 가변 길이 레코드로 구성됩니다. WMF 파일은 이미지를 그리기 위해 GDI에 렌더링된 명령을 기반으로 하므로 해당 이미지를 재생하기 위해 재생할 수 있는 이미지의 디지털 기록이라고도 합니다. WMF의 전체 파일 형식 사양은 온라인에서 사용할 수 있으며 WMF 파일과 함께 작동하는 응용 프로그램 개발에 참조해야 합니다. WMF 파일은 다음으로 구성됩니다.

* WMF 헤더 레코드
* WMF 기록(들)
* WMF 파일 끝 기록

### WMF 헤더 레코드 ###

**META_HEADER 레코드**는 다음을 포함하여 메타파일의 특성을 정의하는 정보를 포함합니다.

* 메타파일의 종류
* 메타파일의 버전
* 메타파일의 크기
* 메타파일에 정의된 개체의 수
* 메타파일에서 가장 큰 단일 레코드의 크기

### WMF 배치 가능 헤더 레코드 ###

**META_PLACEABLE 레코드**에는 다음을 포함하여 이미지와 관련된 확장 정보가 포함되어 있습니다.

* 경계 사각형
* 확장을 위한 논리적 단위 크기
* 유효성 검사를 위한 체크섬

### WMF 기록 ###

WMF 레코드에는 사양 문서에 지정된 일반 형식이 있습니다. 모든 WMF 레코드에는 다음 정보가 포함됩니다.

* 레코드 크기
* 녹음 기능
* 기록 기능에 대한 매개변수(있는 경우)

## 참조 ##

* [[MS-WMF]: Windows 메타파일 형식](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [윈도우 메타파일 - 위키피디아](https://en.wikipedia.org/wiki/Windows_Metafile)

