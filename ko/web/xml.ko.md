{
  "date" : "2019-10-11",
  "keywords" :["xml", "파일", "확장자", "파일 형식", "파일 확장자", "확장 가능한 마크업 언어"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML 파일 형식",
  "description":"XML 파일 형식과 XML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## XML 파일이란?

XML은 **[HTML](/ko/web/html/)**과 비슷하지만 태그를 사용하여 객체를 정의한다는 점에서 다른 Extensible Markup Language의 약자입니다. XML 파일 형식 생성의 배경은 소프트웨어나 하드웨어 도구에 의존하지 않고 데이터를 저장하고 전송하는 것이었습니다. 그 인기는 사람과 기계가 읽을 수 있기 때문입니다. 이를 통해 WWW(월드 와이드 웹)와 같은 네트워크를 통해 저장 및 공유할 개체 형태의 공통 데이터 프로토콜을 만들 수 있습니다. XML의 "X"는 확장 가능하므로 사용자 요구 사항에 따라 언어를 원하는 수의 기호로 확장할 수 있습니다. Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/ko/web/xhtml/)** 및 **[SVG](/ko/page-description-language)와 같은 많은 표준 파일 형식에서 이러한 기능을 사용합니다. /svg/)**.

## XML 파일 형식

XML 파일 형식은 HTML 및 XML 문서용 프로그래밍 API인 XML DOM(문서 개체 모델)을 기반으로 합니다. XML DOM은 XML 문서 요소에 액세스하고 조작하는 표준 방법을 정의합니다. DOM 트리를 통해 모든 요소에 액세스하는 데 사용할 수 있는 XML 문서의 트리 구조 보기를 만듭니다. 기존 요소를 수정/삭제할 수 있을 뿐만 아니라 XML 트리에서 새 요소를 생성할 수 있습니다. XML 문서의 각 요소를 노드라고 합니다. XML DOM은 다음 이미지와 같습니다.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### XML의 보편적인 접근

XML의 힘은 데이터 전송 및 플랫폼 변경을 단순화하여 네트워크를 통한 데이터 통신을 위한 범용 언어로 만듭니다. 또한 데이터를 일반 텍스트 형식으로 저장하여 호환되지 않는 시스템 간에 데이터를 교환할 수 있습니다. HTML은 웹을 통한 데이터 표현을 위한 반면 XML은 데이터 교환을 위한 것입니다. XML 내부에서 사용되는 마크업 태그 쌍은 애플리케이션을 읽는 데 사용할 구조의 핵심 요소를 정의합니다.

## XML 예제

다음은 각 레코드에 아티스트, 국가, 회사, 가격 및 생산 연도와 같은 CD에 대한 정보가 포함된 CD 카탈로그의 간단한 예입니다.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## 참고문헌

* [XML - 위키피디아 작성](https://en.wikipedia.org/wiki/XML)

