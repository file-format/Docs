{
  "date" : "2019-10-11",
  "keywords" :[ "vssx 파일", "vssx 파일 형식", "vssx 파일이란", "파일", "vssx 예제", "vssx 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Visio 스텐실 파일 형식",
  "description":"VSSX 파일 형식과 VSSX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## .VSX 파일이란?

확장자가 .vssx인 파일은 [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 이상으로 만든 드로잉 스텐실입니다. VSSX 파일 형식은 Visio 2013 이상에서 열 수 있습니다. Visio 파일은 모양, 커넥터, 순서도, 네트워크 레이아웃, UML 다이어그램, 소프트웨어 다이어그램, 데이터베이스 모델, 개체 매핑 및 기타 유사한 정보 모음과 같은 다양한 그리기 요소를 나타내는 것으로 알려져 있습니다. Microsoft Visio는 Visio 파일을 [PNG](/ko/image/png/), [BMP](/ko/image/bmp/), [PDF](/ko/pdf/) 등과 같은 다른 파일 형식으로 변환하는 기능도 제공합니다. Windows 및 Mac OS 모두에서 사용할 수 있습니다.

## VSSX 파일 형식

VSSX 파일 형식은 2007년부터 Microsoft에서 채택한 OpenOffice 형식을 기반으로 합니다. XML 파일 형식 사양을 기반으로 전체 파일 형식을 나타내는 [ZIP](/ko/compression/zip/) 아카이브를 기반으로 합니다. VSSX에 해당하는 이진 파일 형식은 Visio 2007까지 지원되었던 VSS였습니다. VSSX 파일 형식의 내용은 확장자를 .ZIP으로 바꾸고 WinZIP과 같은 보관 파일 형식으로 열어 볼 수 있습니다.

VSDX 파일은 Open Packaging Conventions 및 XML을 기반으로 하며 개발자는 프로그래밍 방식으로 이러한 파일을 사용하는 방법을 학습하여 이 형식의 이점을 얻을 수 있습니다. 형식은 Visio XML 드로잉 파일 형식(.vdx)에서 해당 부분과 동일한 XML 구조를 많이 상속합니다. 타사 소프트웨어가 파일 형식 수준에서 Visio 파일을 조작할 수 있으므로 Visio 파일과의 상호 운용성이 크게 향상됩니다.

Visio 2013 파일 형식을 구성하는 다른 특정 파일 형식은 다음과 같습니다.

* .vsdm(Visio 매크로 사용 드로잉)
* .vssx(Visio 스텐실)
* .vssm(Visio 매크로 사용 스텐실)
* .vstx(Visio 템플릿)
* .vstm(Visio 매크로 사용 템플릿)

각 Visio 파일은 다른 파일이나 부분을 포함하는 패키지라고 합니다. 패키지 부분은 XML 파일, 이미지 또는 VBA 솔루션일 수 있습니다. 패키지 내의 부분은 "문서" 및 "관계" 부분으로 나눌 수 있습니다.

## 참조 ##

* [Visio 파일 형식 소개](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [스키마 맵 - Visio XML](https://learn.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)

