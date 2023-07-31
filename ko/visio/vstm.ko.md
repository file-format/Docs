{
  "date" : "2019-10-11",
  "keywords" :[ "vstm 파일", "vstm 파일 형식", "vstm 파일이란", "파일", "vstm 예제", "vstm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio 템플릿 파일 형식",
  "description":"VSTM 파일 형식과 VSTM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## .VTM 파일이란?

VSTM 확장자를 가진 파일은 매크로를 지원하는 Microsoft Visio로 만든 템플릿 파일입니다. VSDX 파일과 달리 VSTM 템플릿에서 만든 파일은 VBA(Visual Basic for Applications) 코드로 개발된 매크로를 실행할 수 있습니다. 이러한 설정으로 추가 문서를 생성하는 데 사용할 수 있는 문서의 기본 설정을 제공하기 위해 템플릿 파일을 만들 수 있습니다. Visio 파일은 시각적 개체, 순서도, UML 다이어그램, 정보 흐름, 조직도, 소프트웨어 다이어그램, 네트워크 레이아웃, 데이터베이스 모델, 개체 매핑 및 기타 유사한 정보가 포함된 도면을 만드는 데 사용됩니다. Visio를 사용하여 생성된 파일은 PNG, BMP, PDF 등과 같은 다양한 파일 형식으로 내보낼 수도 있습니다.

## 파일 형식 ##

VSTM 파일은 Open Packaging Conventions 및 XML을 기반으로 하며 개발자는 이러한 파일을 프로그래밍 방식으로 사용하는 방법을 학습하여 이 형식의 이점을 얻을 수 있습니다. 형식은 Visio XML 드로잉 파일 형식(.vdx)에서 해당 부분과 동일한 XML 구조를 많이 상속합니다. 타사 소프트웨어가 파일 형식 수준에서 Visio 파일을 조작할 수 있으므로 Visio 파일과의 상호 운용성이 크게 향상됩니다.

각 Visio 파일은 다른 파일이나 부분을 포함하는 패키지라고 합니다. 패키지 부분은 XML 파일, 이미지 또는 VBA 솔루션일 수 있습니다. 패키지 내의 부분은 "문서" 및 "관계" 부분으로 나눌 수 있습니다.

### Document ###


The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes. Images and text files within the package are considered document parts.


### 관계 ###

Visio 파일의 관계 부분은 "_rels" 폴더에 저장되며 패키지 내의 각 부분이 어떻게 관련되는지 설명합니다. 또한 파일의 구조를 제공합니다. 독립 실행형 XML 문서는 요소의 상위/하위 관계를 사용하여 엔티티 간의 관계를 결정합니다. 유효한 Visio 2013 파일 형식에는 올바른 부품 집합이 포함되어 있으며 패키지에는 부품 간의 관계가 포함되어 있습니다.

관계 부분은 패키지 내 서로 다른 문서 부분 간의 관계를 설명하는 XML 문서입니다. 지정된 소스(관계 파일의 이름과 위치로 정의됨)와 지정된 대상 문서 부분이라는 두 항목 간의 연관을 정의합니다. 예를 들어, 관계 부분은 파일과 연결된 모양 마스터, 페이지가 파일 및 서로 관련되는 방식 또는 이미지와 개체가 특정 페이지와 관련되는 방식을 설명하는 데 사용됩니다.

## 참조 ##

* [Visio 파일 형식 소개](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

