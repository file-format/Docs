{
  "date" : "2019-10-11",
  "keywords" :[ "x3d 파일", "x3d 파일 형식", "x3d 파일이란", "파일", "x3d 예제", "x3d 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D 이미지 파일",
  "description":"X3D 파일 형식과 X3D 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .X3D 파일이란?
X3D는 3D 정보 표현을 위한 [XML](/ko/web/xml/) 기반의 3D 그래픽 파일 형식입니다. 이는 모듈식 표준이며 여러 ISO 사양을 통해 정의됩니다. 이 형식은 벡터 및 래스터 그래픽, 투명도, 조명 효과 및 회전, 페이드 및 스윙을 포함한 애니메이션 설정을 지원합니다. 2001년 [VRML](/ko/3d/vrml/) 파일 형식의 후속이 되었습니다. X3D는 색상에 모델을 인쇄할 때 사용되는 [STL](/ko/cad/stl/)과 달리 색상 정보를 인코딩할 수 있는 장점이 있습니다. 3D 프린터. 이 형식은 VRML에 대한 확장 기능을 제공하여 XML 구문과 Open Inventor와 유사한 VRML97 구문 또는 이진 형식을 사용하여 장면을 인코딩할 수 있는 기능을 제공합니다.

X3D(ISO/IEC 19775)에 대한 추상 사양은 2004년 ISO에서 처음 승인되었습니다. X3D(ISO/IEC 19776)에 대한 XML 및 ClassicVRML 인코딩은 2005년에 처음 승인되었습니다.

## X3D 파일 형식

X3D 장면 파일에는 다음과 같은 공통 파일 구조가 있습니다.

* 파일 헤더(XML, ClassicVRML 또는 압축 바이너리)
* 버전 및 프로필 속성을 포함한 X3D 루트 노드의 시작
* Component 및 Meta 문이 있는 헤드 섹션(둘 다 선택 사항)
* X3D 장면 그래프와 그 자식 노드
* X3D 루트 노드의 끝

## X3D 파일 형식 예

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## 참조 ##

* [X3D - 위키피디아 작성](https://en.wikipedia.org/wiki/X3D)
* [Web3D 컨소시엄 공식 홈페이지](http://www.web3d.org/)
* [X3D 공식 홈페이지](http://www.web3d.org/x3d/what-x3d)

