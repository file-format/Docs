{
  "date" : "2021-05-24",
  "keywords" :["xul", "파일", "확장자", "파일 형식", "파일 확장자", "XML 사용자 인터페이스 언어"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML 사용자 인터페이스 언어 파일",
  "description":"XUL 파일 형식과 XUL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .XUL 파일이란?

확장자가 .xul인 파일([XUL](https://wiki.mozilla.org/XUL:Home_Page)은 XML 사용자 인터페이스 언어를 나타냄)은 다음을 위한 [XML](/ko/web/xml/) 기반 마크업 언어 파일입니다. 사용자 인터페이스 생성. 개발자가 웹 페이지를 만드는 데 사용되는 다른 마크업 언어와 유사한 그래픽 사용자 인터페이스 요소를 만들기 위해 Mozilla에서 개발했습니다. XUL은 Mozilla 코드베이스를 사용한 Firefox 브라우저에서 Mozilla에서 널리 사용되었습니다. XUL 렌더링은 다음을 사용하여 수행됩니다.
[Gecko 엔진](https://en.wikipedia.org/wiki/Gecko_(소프트웨어)). Pale Moon, Basilisk 및 Waterfox와 같은 Firefox 포크는 XUL 추가 기능에 대한 지원을 유지합니다. XUL 파일은 MIME 유형: application/vnd.mozilla.xul+xml로 식별됩니다.

## XUL 파일 형식

XUL 파일은 XML 파일 형식을 기반으로 일반 텍스트로 작성되며 Gecko 엔진을 사용하여 렌더링됩니다. XUL 구조의 세 가지 주요 부분은 다음과 같습니다.

* `Content` - 여기에는 창의 선언과 그 안에 포함된 사용자 인터페이스 요소가 포함됩니다.
* '스킨' - 스타일 시트, 이미지 및 기타 테마 관련 파일을 포함합니다. 창의 모양은 스타일 시트에 설명되어 있습니다.
* `로케일` - 창에 표시되는 텍스트는 별도로 저장되며 여러 언어 파일 집합을 사용자가 사용할 수 있습니다.

### XUL 예제

다음 예제에서는 세로 방향으로 서로 위에 쌓인 세 개의 버튼을 만듭니다.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## 참고문헌

* [XUL - 위키피디아 작성](https://en.wikipedia.org/wiki/XUL)
* [XUL 아카이브 문서 - Mozilla 제공](https://wiki.mozilla.org/XUL:Home_Page)

