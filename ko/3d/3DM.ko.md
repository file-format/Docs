{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"3DM 파일 형식과 3DM 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## .3DM 파일이란?

확장자가 .3dm인 파일은 3D 그래픽 소프트웨어에 사용되는 오픈 소스 파일 형식입니다. 여기에는 표면, 점 및 곡선 정보와 같은 종속 요소와 함께 3D 모델이 포함됩니다. 3DM 파일 형식은 응용 프로그램 간에 3D 지오메트리를 정확하게 전송하기 위해 [openNURBS](https://github.com/mcneel/opennurbs) 이니셔티브에 의해 개발되었습니다. 3DM 파일은 Rhinoceros, SAP VEViewer, Moment of Inspiration 및 Right Hemisphere Deep View와 같은 응용 프로그램으로 열고 변환할 수 있습니다.

## 3DM 파일 형식

오픈 소스 툴킷인 [openNURBS](https://github.com/mcneel/opennurbs)에는 파일 형식을 읽고 쓰기 위한 3DM 파일 형식 사양, 문서, C++ 소스 코드 라이브러리 및 .NET 2.0 어셈블리가 포함되어 있습니다.

### 3DM 예제 파일

일부 예제 3DM 파일은 openNURBS [예제](https://github.com/mcneel/opennurbs/tree/7.x/example_files) 섹션에서 다운로드할 수 있습니다. openNURBS 툴킷을 사용하여 로드하고 표시할 수 있습니다.

## 3DM 파일을 읽거나 쓰는 방법은 무엇입니까?

[openNURBS](https://github.com/mcneel/opennurbs) 라이브러리를 사용하면 Rhino 없이 누구나 3DM 파일 형식을 읽고 쓸 수 있습니다. openNURBS 파일 형식을 사용하여 3D 모델을 읽고 쓰는 라이브러리용 C++ 소스 코드를 제공합니다. 이 툴킷은 또한 NURBS 평가 도구와 기본 기하학적 및 3D 보기 조작 도구를 제공할 뿐만 아니라 여러 예제 프로그램에 대한 소스 코드를 포함합니다. [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) 지원 포럼은 3DM 커뮤니티가 직면한 문제를 공유하고 솔루션을 얻을 수 있는 풍부한 콘텐츠 및 토론 공간입니다.

## 참조 ##

* [코뿔소](https://www.rhino3d.com/download/openNURBS)
* [코뿔소 - 위키백과](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [깃허브의 openNURBS](https://github.com/mcneel/opennurbs)

