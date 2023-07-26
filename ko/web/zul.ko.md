{
  "date" : "2021-05-24",
  "keywords" :["zul", "파일", "확장자", "파일 형식", "파일 확장자", "열기"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK 사용자 인터페이스 파일",
  "description":"ZUL 파일 형식과 ZUL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## .ZUL 파일이란?

확장자가 .zul인 파일은 ZUML(사용자 인터페이스 마크업 언어)로 만든 웹 파일이며 사용자 인터페이스 요소에 대한 정의를 포함합니다. Ajax 및 Java 클래스는 서버 측 파일 개발을 위해 [XML](/ko/web/xml/) 기반 ZUML 사용을 지원합니다. ZUL 파일 형식은 JavaScript 또는 AJAX에 대한 지식 없이도 웹 및 모바일 응용 프로그램을 빌드할 수 있는 UI 프레임워크인 ZK에서 개발했습니다.

## ZUL 파일 형식

ZUL 파일은 사용자 인터페이스를 구성하는 다양한 요소로 구성된 XML 기반입니다. ZK 로더는 각 XML 요소를 사용하여 구성 요소를 만듭니다. 페이지 제목, 설명 등 페이지 요소의 전반적인 처리는 ZUML의 각 XML 처리 명령에 의해 설명됩니다.

### ZUL 예

다음 ZUML 코드 예제에서 첫 번째 줄은 페이지 제목을 지정하고, 두 번째 줄은 제목과 테두리가 있는 루트 구성 요소를 만들고, 세 번째 줄은 레이블과 이벤트 리스너가 있는 버튼을 만듭니다.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL 스키마는 https://www.zkoss.org/2005/zul/zul.xsd에서 다운로드할 수 있습니다.
## 참고문헌

* [ZUL - ZK 작성](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL 스키마](https://www.zkoss.org/2005/zul/zul.xsd)

