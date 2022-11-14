{
  "date" : "2019-10-11",
  "keywords" :[ "ppsm 파일", "ppsm 파일 형식", "ppsm 파일이란", "파일", "ppsm 예제", "ppsm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - 매크로 사용 PowerPoint 프레젠테이션 파일",
  "description":"PPSM 파일 형식과 PPSM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .PPSM 파일이란?

확장자가 PPSM인 파일은 Microsoft PowerPoint 2007 이상에서 만든 매크로 사용 슬라이드 쇼 파일 형식을 나타냅니다. 또 다른 유사한 파일 형식은 [PPTM](/ko/presentation/pptm/)으로, 슬라이드 쇼로 실행하는 대신 편집 가능한 형식으로 Microsoft PowerPoint로 여는 것이 다릅니다. 슬라이드 쇼로 실행하면 PPSM 파일은 슬라이드 쇼의 내용이 그대로 유지되고 기본적으로 읽기 전용 모드에 있는 프레젠테이션 슬라이드를 표시합니다. PPSM 파일은 PowerPoint에서 열어 Microsoft PowerPoint에서 계속 편집할 수 있습니다.

## 파일 형식 ##

PPSM 파일 형식은 PowerPoint 2007과 함께 도입되었으며 XML과 [ZIP](/ko/compression/zip/)의 조합을 사용하여 내용을 저장하는 OpenXML 파일 형식을 기반으로 합니다. Office Open XML 파일 형식으로 생성된 파일은 모든 구성 파일 간의 링크를 제공하는 다른 파일과 함께 XML 파일의 모음입니다. 이 컬렉션은 실제로 콘텐츠를 보기 위해 추출할 수 있는 압축된 아카이브입니다. 이렇게 하려면 zip으로 PPSM 파일 확장자의 이름을 바꾸고 내용을 관찰하기 위해 압축을 풉니다.

다음 섹션에서는 이들 각각에 대해 설명합니다.

### [콘텐츠 유형].xml ###

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

및 다음 xml 파일:

* 프레젠테이션.xml
* preProps.xml
* tableStyles.xml
* viewProps.xml

## 참조 ##

* [OpenXML 프레젠테이션 파일 형식](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [오픈오피스 XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

