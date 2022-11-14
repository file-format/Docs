{
  "date" : "2019-10-11",
  "keywords" :[ "xpm 파일", "xpm 파일 형식", "xpm 파일이란", "파일", "xpm 예제", "xpm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap 파일 형식",
  "description":"XPM 파일을 만들고 열 수 있는 XPM 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .XPM 파일이란?

확장자가 .xpm인 파일은 X Windows 시스템에서 사용되는 이미지 파일 형식입니다. 투명한 픽셀을 지원하며 일반적으로 아이콘 픽스맵을 만드는 대상입니다. 흑백, 그레이 스케일 및 컬러 픽스맵 데이터를 지원합니다. 이들은 손으로 편집할 수 있도록 설계되었으며 [C](/ko/programming/c/) 코드에 포함될 수 있습니다. 이를 위해 XPM 파일은 일반 텍스트 파일 형식이며 C 프로그래밍 언어 구문을 따릅니다. XPM 파일은 다음과 같은 다양한 이미지 보기 응용 프로그램으로 열 수 있습니다.
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView 및 Canvas X.

## XPM 파일 형식

XPM 파일 형식은 C 및 C++ 프로그램에 통합하기 위해 C 구문을 사용합니다. 다음 6가지 섹션으로 구성되어 있습니다.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

섹션은 실제로 다음과 같은 문자열 배열입니다.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
다음은 각 섹션의 세부 사항입니다.

`<Values> ` - 이 섹션은 10진법에 해당하는 4개 또는 6개의 정수를 포함하는 문자열입니다.

* 픽스맵 너비와 높이
* 색상 수
* 픽셀당 문자 수
* 선택적 핫스팟 좌표 및 XPMEXT 태그

`<Colors> ` - 이 섹션은 색상만큼 많은 문자열을 포함합니다. 각 문자열은 다음과 같습니다.

```
<chars>{<key><color> }+
```
`<Pixels> ` - 이 섹션은 다음으로 구성됩니다.<height> 문자열과<width> \*<chars_per_pixel> 문자. 모든<chars_per_pixel> 길이 문자열은 이전에 정의된 그룹 중 하나여야 합니다.<Colors> 부분.

`<Extension> ` - 확장 섹션이 비어 있지 않으면 레이블이 지정되어야 합니다.<Values> 부분. 그것은 여러 구성 될 수 있습니다<Extension> 다음 두 가지 유형이 될 수 있는 하위 섹션:

* 다음과 같이 구성된 하나의 독립 실행형 문자열: XPMEXT<extension-name><extension-data>
* 또는 여러 문자열로 구성된 블록:XPMEXT<extension-name><related extension-data composed of several strings>

## 참고문헌

* [XPM - 위키백과](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM 매뉴얼](http://www.xfree86.org/current/xpm.pdf)

