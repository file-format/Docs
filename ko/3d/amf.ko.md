{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf 파일", "amf 파일 형식", "파일 형식", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AMF 파일 형식과 AMF 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "title" :"AMF - 적층 제조 파일",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .AMF 파일이란?
AMF 파일은 적층 제조 프로세스에서 사용하기 위한 개체 설명에 대한 지침으로 구성됩니다. 오프닝이 들어있습니다<amf> XML 태그로 끝납니다.</amf> 요소. 이것은 파일의 XML 버전과 인코딩을 지정하는 XML 선언 라인이 앞에 옵니다. 선언에는 측정 단위 정보가 포함될 수 있으며 이러한 정보가 없는 경우 밀리미터가 기본 단위로 사용됩니다.


## AMF 파일 형식

적층 제조 파일 형식(**AMF**)은 3D 프린팅과 같은 적층 제조 프로세스에서 활용하기 위해 개체 설명에 대한 개방형 표준을 정의합니다. CAD 프로그램은 객체의 형상, 색상 및 재질과 같은 정보를 사용하여 AMF 파일 형식을 사용합니다. AMF는 측면이 색상, 재료, 격자 및 별자리를 지원하지 않기 때문에 STL 형식과 다릅니다.

### AMF 파일의 요소

로 정의된 5개의 최상위 요소<AMF> 태그는 아래에 자세히 설명되어 있습니다. 완전한 기능의 AMF 파일을 위해서는 단일 개체 요소가 있어야 합니다.

`<object> ` - object 요소는 각각 인쇄를 위한 재료 ID와 연결된 재료의 볼륨을 정의합니다. 파일에 하나 이상의 개체 요소가 있어야 합니다. 추가 개체는 선택 사항입니다.

`<material> ` - 선택적 재료 요소는 연관된 재료 ID로 인쇄하기 위한 하나 이상의 재료를 정의합니다. 재료 요소가 포함되지 않은 경우 단일 기본 재료가 가정됩니다.

`<texture> ` - 선택적 텍스처 요소는 각각 연관된 텍스처 ID가 있는 색상 또는 텍스처 매핑을 위한 하나 이상의 이미지 또는 텍스처를 정의합니다.

`<constellation> ` - 선택적 constellation 요소는 객체와 다른 별자리를 인쇄를 위한 상대적 패턴으로 계층적으로 결합합니다.

`<metadata> ` - 선택적 메타데이터 요소는 파일에 포함된 개체 및 요소에 대한 추가 정보를 지정합니다.

## AMF 예

다음은 [텍스트](/ko/word-processing/txt/) 파일로 복사하여 압축된 [zip](/ko/compression/zip/) 파일로 저장하여 열 수 있는 AMF 파일의 예입니다.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## 참고문헌

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [ISO에 대한 AMF 사양](https://www.iso.org/standard/67472.html)

