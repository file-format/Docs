{
  "date" : "2019-10-11",
  "keywords" :[ "pptm 파일", "pptm 파일 형식", "pptm 파일이란", "파일", "pptm 예제", "pptm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPTM - 매크로 사용 PowerPoint 프레젠테이션 파일 형식",
  "description":"PPTM 파일을 만들고 열 수 있는 PPTM 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "PPTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

PPTM 확장자를 가진 파일은 Microsoft PowerPoint 2007 이상 버전에서 만든 매크로 사용 프레젠테이션 파일입니다. [PPTX](/ko/presentation/pptx/) 파일과 유사하지만 매크로를 포함할 수는 있지만 측면에서는 매크로를 실행할 수 없다는 차이점이 있습니다. PPTM 파일은 Microsoft PowerPoint에서 열고 내용을 업데이트하여 편집할 수 있습니다. 또 다른 유사한 형식은 PPSM이지만 기본적으로 읽기 전용이며 열 때 슬라이드쇼를 시작합니다. PPTX와 마찬가지로 PPTM에는 텍스트, 이미지, 비디오, 그래프 및 기타 관련 자료와 같은 다양한 프레젠테이션 요소에 대한 슬라이드가 포함되어 있습니다.

## 간략한 역사 ##

PPTM 파일 형식은 2007년에 도입되었으며 2000년에 Microsoft에서 채택한 Open XML 표준을 사용합니다. 새로운 파일 형식은 작은 파일 크기, 적은 손상 변경 및 올바른 형식의 이미지 표현이라는 이점을 추가했습니다. Microsoft가 **Office Open XML** 표준을 수용하기 위해 변경하기로 결정한 것은 2000년 초였습니다. 2007년에 이 새로운 파일 형식은 Office 2007의 일부가 되었으며 새 버전의 Microsoft Office에서도 계속 사용됩니다.

## 파일 형식 사양 ##

Office Open XML 파일 형식으로 생성된 파일은 모든 구성 파일 간의 링크를 제공하는 다른 파일과 함께 XML 파일의 모음입니다. 이 컬렉션은 실제로 콘텐츠를 보기 위해 추출할 수 있는 압축된 아카이브입니다. 이렇게 하려면 PPTM 파일 확장자의 이름을 zip으로 바꾸고 내용을 관찰하기 위해 압축을 풉니다.

다음 섹션에서는 이들 각각에 대해 설명합니다.

### [콘텐츠_유형].xml ###

이것은 zip 압축을 풀 때 기본 수준에서 발견되는 유일한 파일입니다. 패키지 내 부품의 콘텐츠 유형을 나열합니다. 패키지에 포함된 XML 파일에 대한 모든 참조는 이 XML 파일에서 참조됩니다. 다음은 슬라이드 파트의 콘텐츠 유형입니다.
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
패키지에 새 부품을 추가해야 하는 경우 새 부품을 추가하고 .rels 파일 내의 모든 관계를 업데이트하면 됩니다. 이러한 변경을 위해서는 Content_Types.xml도 업데이트되어야 한다는 점을 염두에 두어야 합니다.

### \\rels(폴더) ###

패키지 외부의 다른 부분과 리소스 간의 관계는 관계 부분에 의해 유지됩니다. 관계 폴더에는 패키지 수준 관계를 저장하는 단일 XML 파일이 있습니다. 프레젠테이션 파일의 주요 부분에 대한 링크는 이 파일에 URI로 포함됩니다. 이러한 URI는 패키지에 대한 각 핵심 부분의 관계 유형을 식별합니다. 여기에는 ppt/presentation.xml에 있는 기본 사무실 문서와 핵심 및 확장 속성으로 docProps 내의 다른 부분과의 관계가 포함됩니다.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
하나 이상의 관계의 소스인 문서의 각 부분에는 해당 관계 부분이 해당 부분의 \_rels 하위 폴더 내에서 발견되고 이름에 '.rels'를 추가하여 이름이 지정되는 고유한 관계 부분이 있습니다. 부분. 주요 콘텐츠 부분(presentation.xml)에는 자체 관계 부분(presentation.xml.rels)이 있습니다. 여기에는 slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml과 같은 콘텐츠의 다른 부분과 외부 링크에 대한 URI와의 관계가 포함됩니다.

#### 명시적 관계 ####

명시적 관계의 경우 리소스는 다음의 Id 속성을 사용하여 참조됩니다.<Relationship> 요소. 즉, 소스의 Id는 대상에 대한 명시적 참조와 함께 관계 항목의 Id에 직접 매핑됩니다.

예를 들어 슬라이드에는 다음과 같은 하이퍼링크가 포함될 수 있습니다.
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2"는 슬라이드(slide1.xml.rels)의 관계 부분 내에서 다음 관계를 참조합니다.
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### 암시적 관계 ####

암시적 관계의 경우 `<Relationship> 아이디`. 대신 참조가 이해됩니다.

### ppt 폴더 ###

프레젠테이션 내용에 대한 모든 세부 정보가 들어 있는 기본 폴더입니다. 기본적으로 다음 폴더가 있습니다.

* \_rels
* 주제
* 슬라이드
* 슬라이드 레이아웃
* 슬라이드마스터

다음 xml 파일:

* 프레젠테이션.xml
* preProps.xml
* tableStyles.xml
* viewProps.xml

## 참조 ##

* [[MS-PPTX] - PPTX 파일 형식](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [오픈오피스 XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

