{
  "date" : "2020-01-10",
  "keywords" :[ "otg 파일", "otg 파일 형식", "otg 파일이란", "파일", "otg 예제", "otg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument 도면 템플릿 파일 형식",
  "description":"OTG 파일을 만들고 열 수 있는 OTG 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## .OTG 파일이란?

OTG 파일은 OASIS Office Applications [1.0 사양](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf)을 따르는 OpenDocument 표준을 사용하여 생성된 도면 템플릿입니다. 파일 내용을 더욱 향상시키는 데 사용할 수 있는 벡터 이미지에 대한 그리기 요소의 기본 구성을 나타냅니다. OTF 파일은 문서의 내용을 나타내는 XML 형식을 기반으로 하는 다른 OpenDocument 형식 기반 파일과 같습니다. OTF 파일은 텍스트 또는 표준 XML 편집기에서 열어 볼 수 있습니다.

## OTG 파일 형식 사양 ##

OTG 파일 형식은 스키마가 잘 정립된 OpenDocument XML 형식을 기반으로 합니다. OpenDocument 형식의 각 구성 요소 구조는 연관된 속성이 있고 텍스트 문서, 스프레드시트 또는 도면 파일과 같은 모든 문서 유형에 공통적인 요소로 표시됩니다. 도면 템플릿인 OTG는 다음을 포함하는 그래픽 콘텐츠 사양을 광범위하게 활용합니다.

* 그래픽 애플리케이션을 위한 향상된 페이지 기능
* 도형 그리기
* 프레임
* 3D 모양
* 사용자 정의 모양
* 프레젠테이션 모양
* 프레젠테이션 애니메이션
* SMIL 프레젠테이션 애니메이션
* 프레젠테이션 이벤트
* 현재 텍스트 필드
* 프레젠테이션 문서 내용

### 그래픽 애플리케이션을 위한 향상된 페이지 기능 ###
#### 유인물 마스터 ####

유인물 마스터 요소는 이러한 페이지 인쇄를 지원하는 응용 프로그램의 유인물 페이지를 자동으로 생성하기 위한 템플릿입니다.
`<style:handout-master> ` 요소는 다음과 같습니다.

|레이아웃|속성|설명
---|---|---|
|프레젠테이션 페이지 레이아웃|프레젠테이션:presentation-page-layout-name|`에 대한 링크<style:presentation-page-layout> ` 속성
|페이지 레이아웃|`스타일:페이지 레이아웃 이름` | 유인물 마스터 페이지의 크기, 테두리 및 방향을 포함하는 페이지 레이아웃을 지정합니다.
|페이지 스타일|`draw:style-name`|드로잉 페이지 스타일을 지정하여 유인물 마스터 페이지에 추가 서식 속성을 지정합니다.|
|헤더 선언| `프레젠테이션:헤더 이름 사용`| 유인물 마스터 페이지에 표시되는 모든 헤더 필드에 사용되는 헤더 필드 선언의 이름을 지정합니다.
|바닥글 선언| Presentation:use-footer-name|유인물 마스터 페이지에 표시되는 모든 바닥글 필드에 사용되는 바닥글 필드 선언의 이름을 지정합니다.
|날짜 및 시간 선언|use-date-time-name|유인물 마스터 페이지에 표시되는 모든 날짜-시간 필드에 사용되는 날짜-시간 필드 선언의 이름을 지정합니다.

### 도형 그리기 ###
OpenDocument 형식은 모든 유형의 문서에서 사용할 수 있는 여러 그리기 모양을 지원합니다.

|모양|관련 속성| 집단
---|---|---|
직사각형 - `<draw:rect> `|위치, 크기, 스타일, 레이어, Z-색인, ID, 캡션 ID, 텍스트 앵커, 테이블 배경, 그리기 끝 위치, 둥근 모서리|제목, 긴 설명, 이벤트 리스너, 글루 포인트, 텍스트
라인 `<draw:line> `|스타일, 레이어, Z-색인, ID, 캡션 ID 및 변환, 텍스트 앵커, 테이블 배경, 끝 위치 그리기, 시작점, 끝점|제목, 자세한 설명, 이벤트 리스너, 글루 포인트, 텍스트
폴리라인 `<draw:polyline> `| 위치, 크기, 보기 상자, 스타일, 레이어, Z-색인, ID, 캡션 ID 및 변환, 텍스트 앵커, 테이블 배경, 그리기 끝 위치, Points| 제목, 긴 설명, 이벤트 리스너, 글루 포인트, 텍스트
다각형 `<draw:polygon> `|위치, 크기, 보기 상자, 스타일, 레이어, Z-색인, ID, 캡션 ID 및 변환, 텍스트 앵커, 테이블 배경, 그리기 끝 위치, 포인트|제목, 긴 설명, 이벤트 리스너, 글루 포인트, 텍스트
|정다각형 `<draw:regular-polygon> `|위치, 크기, 스타일, 레이어, Z-색인, ID, 캡션 ID 및 변환, 텍스트 앵커, 테이블 배경, 그리기 끝 위치, 오목, 모서리, 선명도|제목, 긴 설명, 이벤트 리스너, 글루 포인트, 텍스트
|파트`<draw:path> `|위치, 크기, 보기 상자, 스타일, 레이어, Z-색인, ID, 캡션 ID 및 변환, 텍스트 앵커, 테이블 배경, 그리기 끝 위치, 경로 데이터| 제목, 긴 설명, 이벤트 리스너, 글루 포인트, 텍스트

### 프레임 ###
도면 문서에서 프레임은 텍스트 상자, 이미지 또는 개체를 포함하는 직사각형 컨테이너입니다. 프레임은 등고선, 이미지 맵 및 하이퍼링크와 같은 추가 기능을 지원합니다. 프레임에는 이미지와 함께 개체가 포함될 수 있으므로 개체를 여러 번 표현할 수 있습니다. 응용 프로그램은 최상의 지원을 기반으로 각 요소를 렌더링합니다.

프레임에는 다음이 포함될 수 있습니다.
* 텍스트 상자
* OpenDocument 형식 또는 개체별 바이너리 형식으로 표현되는 개체
* 이미지
* 애플릿
* 플러그인
* 플로팅 프레임

문서에는 아래와 같이 프레임이 포함되어 있습니다.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## 참조 ##
* [오아시스 사무용 오픈 문서 형식](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 형식 - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

