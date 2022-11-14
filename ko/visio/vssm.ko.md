{
  "date" : "2019-10-11",
  "keywords" :[ "vssm 파일", "vssm 파일 형식", "vssm 파일이란", "파일", "vssm 예", "vssm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM - Microsoft Visio 매크로 사용 파일 형식",
  "description":"VSSM 파일을 만들고 열 수 있는 API 및 VSSM 파일 형식에 대해 알아보세요.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## .VSM 파일이란?

확장자가 .vssm인 파일은 매크로 지원을 지원하는 Microsoft Visio Stencil 파일입니다. VSSM 파일을 열면 매크로를 실행하여 다이어그램에서 원하는 형식과 모양을 배치할 수 있습니다. 일반적으로 Microsoft Visio는 다양한 모양의 사용자 정의 정보를 포함하고 나타낼 수 있는 파일을 만들 수 있는 그리기 소프트웨어입니다. 이들 중 가장 일반적인 것은 UML 다이어그램, 순서도, 시각적 개체, 정보 흐름, 조직도, 소프트웨어 다이어그램, 네트워크 레이아웃, 데이터베이스 모델, 개체 매핑 및 기타 유사한 정보를 포함하지만 이에 국한되지 않습니다. Visio를 사용하여 생성된 파일은 [PNG](/ko/Image/PNG/), [BMP](/ko/Image/BMP/), [PDF](/ko/pdf/) 등과 같은 다른 파일 형식으로 변환할 수도 있습니다.

## VSSM 파일 형식

VSSM 파일 형식은 OpenOffice XML 사양을 기반으로 하는 Microsoft Visio 2013에서 도입되었습니다. Visio 2013 파일 형식을 구성하는 다른 특정 파일 형식은 다음과 같습니다.

* .vsdm(Visio 매크로 사용 드로잉)
* .vssx(Visio 스텐실)
* .vssm(Visio 매크로 사용 스텐실)
* .vstx(Visio 템플릿)
* .vstm(Visio 매크로 사용 템플릿)

내부적으로 Visio 2013 파일 형식은 구조화된 수단을 사용하여 [ZIP](/ko/Compression/ZIP/)와 같은 아카이브에 관련 리소스와 함께 응용 프로그램 데이터를 저장합니다. ZIP 파일은 다른 유형의 파일도 포함하는 표준 추출 유틸리티를 사용하여 추출할 수 있습니다.

각 Visio 파일은 다른 파일이나 부분을 포함하는 패키지라고 합니다. 패키지 부분은 XML 파일, 이미지 또는 VBA 솔루션일 수 있습니다. 패키지 내의 부분은 "문서" 및 "관계" 부분으로 나눌 수 있습니다.

## 참조 ##

* [Visio 파일 형식 소개](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

