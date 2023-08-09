{
  "date" : "2019-12-09",
  "keywords" :[ "3mf 파일", "3mf 파일 형식", "3mf 파일이란", "파일", "3mf 예", "3mf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"3MF 파일 형식과 3MF 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## 3MF 파일이란?

3MF(3D Manufacturing Format)는 응용 프로그램에서 3D 개체 모델을 다양한 다른 응용 프로그램, 플랫폼, 서비스 및 프린터에 렌더링하는 데 사용됩니다. 최신 버전의 3D 프린터에서 작업하기 위해 [STL](/ko/cad/stl/)과 같은 다른 3D 파일 형식의 제한 및 문제를 피하기 위해 제작되었습니다. 3MF는 3MF 컨소시엄에서 개발 및 발행한 비교적 새로운 파일 형식입니다. 3D 프린팅의 새로운 혁신을 지원하기 위해 확장 가능한 내부 정보, 색상 및 기타 특성을 유지하면서 모델을 완전히 설명할 수 있을 만큼 풍부합니다. 이 형식은 확장 가능하고 광범위하게 채택될 수 있으며 널리 사용되는 다른 파일 형식을 능가하는 문제가 없습니다.

## 3MF 파일 형식의 간략한 역사

STL 및 기타와 같은 사용 가능한 모델 설명 파일 형식의 기존 제한 사항으로 인해 주요 브랜드가 함께 모여 3D 인쇄를 위해 보다 확장 가능한 파일 형식을 공식화하게 되었습니다. 중요한 고려 사항은 응용 프로그램이 모델 데이터를 3D 프린터로 전달하는 방법이었습니다. 따라서 3MF 컨소시엄은 3D 인쇄의 요구 사항을 충족할 수 있을 만큼 충분히 확장할 수 있도록 하기 위해 3MF라는 새로운 3D 파일 형식을 지원하기 시작했습니다. Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP 등 여러 회사가 이 컨소시엄에 참여했습니다. Microsoft는 3MF 컨소시엄이 사양을 공동으로 추가 개발하기 위한 출발점으로 진행 중인 3D 파일 형식을 기증했습니다.

## 3MF 파일 형식 - 추가 정보

3MF는 사용자 정의 데이터에 대한 타사 확장성을 포함하여 3D 제조와 관련된 데이터에 대한 정의를 포함하는 XML 기반 데이터 형식(사람이 읽을 수 있는 압축 XML)입니다. 3MF 파일 형식은 다른 3D 파일 형식이 직면한 한계와 문제를 염두에 두고 설계되었습니다. 이것은 다음과 같은 3MF 파일 형식의 공식화로 이어집니다.

* **전체:** 필요한 모든 모델, 재료 및 속성 정보를 단일 아카이브에 포함
* **사람이 읽을 수 있음:** OPC, [ZIP](/ko/compression/zip/) 및 XML과 같은 일반적인 구조를 사용하여 개발 용이
* **단순:** 간단하고 명확한 사양으로 개발이 쉽고 검증이 빠릅니다.
* **확장 가능:** XML 네임스페이스를 활용하여 호환성을 유지하면서 공개 및 비공개 확장을 모두 허용합니다.
* **명확함:** 명확한 언어 및 적합성 테스트를 통해 파일이 디지털에서 실제 파일에 이르기까지 항상 일관성 있음을 보장합니다.
* **무료:** 3MF 사양에 대한 액세스 및 구현은 로열티, 특허 및 라이선스가 없으며 앞으로도 계속 무료입니다.

3MF 파일 형식에 대한 사양은 공개 액세스 및 지속적인 업데이트를 위해 [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md)에서 호스팅됩니다. 현재 게시된 버전은 하나 이상의 3D 모델의 내용과 모양을 설명하기 위해 XML 및 기타 널리 사용되는 기술을 사용하기 위한 일련의 규칙을 설명하는 1.2.3입니다. 3MF 파일 형식을 처리하기 위한 시스템을 구축하려는 개발자는 구현 목적으로 이러한 사양을 참조할 수 있습니다.

## 3MF 파일 형식 사양

3MF 파일 형식은 물리적 모델에 대해 ZIP 아카이브 형식의 개방형 패키징 사양을 사용합니다. 여기에는 문서의 특정 목적을 충족시키는 잘 정의된 부분 및 관계 세트가 포함됩니다. 이것은 또한 형식이 디지털 서명 및 축소판을 포함한 패키지 기능을 따르도록 합니다.

### 3MF 문서 - 개요

일반적인 3MF 문서는 다음과 같습니다.

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

페이로드에는 3D 모델 부품을 처리하는 데 필요한 전체 부품 세트가 포함됩니다. 3D 페이로드에 설명된 객체를 제조하는 데 사용되는 모든 콘텐츠는 3MF 문서에 포함되어야 합니다(MUST). 각 문서 부분에 대한 설명과 필수 또는 옵션의 상태는 다음 표와 같습니다.


|**이름**|**설명**|**관계 소스**|**필수/선택**
--- | --- | --- | ---
|3D 모델|제조를 위한 하나 이상의 3D 개체에 대한 설명을 포함합니다.|패키지|필수
|Core Properties|다양한 문서 속성을 포함하는 OPC 부분입니다.|Package|OPTIONAL
|디지털 서명 출처|패키지에서 디지털 서명의 루트인 OPC 부분입니다.|패키지|선택 사항
|디지털 서명|각각 디지털 서명을 포함하는 OPC 부분.|디지털 서명 출처|선택 사항
|디지털 서명 인증서|디지털 서명 인증서를 포함하는 OPC 부분.|디지털 서명|선택 사항
|PrintTicket|3D 모델 부분에서 3D 개체를 출력할 때 사용할 설정을 제공합니다.|3D 모델|선택 사항
|Thumbnail|패키지 또는 패키지 전체의 3D 개체를 나타내는 작은 JPEG 또는 PNG 이미지를 포함합니다.|패키지|선택 사항
|3D 텍스처|3D 모델 부품(확장에 사용 가능)에서 3D 개체에 색상을 적용하는 데 사용되는 텍스처를 포함합니다.|3D 모델|선택 사항
|사용자 지정 부품|메타데이터와 연결된 OPC 부품|패키지|선택 사항

[부품 및 관계](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D 모델](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [객체 리소스](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [자료 자원](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) 및 [패키지 기능](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) 사양 섹션 문서 3MF 문서에 대한 자세한 정보를 제공합니다.

## 참조 ##

* [3MF 파일 형식 사양](https://github.com/3MFConsortium/spec_core)
* [3MF - 위키피디아 작성](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

