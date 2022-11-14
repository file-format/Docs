{
  "date" : "2021-01-20",
  "keywords" :["xslt", "파일", "확장자", "파일 형식", "파일 확장자", "확장 가능한 스타일시트 언어"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT 파일 형식",
  "description":"XSLT 파일 형식과 XSLT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## .XSLT 파일이란?

확장자가 .xslt인 파일은 XSL 명령을 사용하여 XML 파일을 변환하고 스타일을 지정하는 데 사용되는 Extensible Stylesheet Language Transformation 파일입니다. 형식은 XML 문서를 텍스트 문서 또는 .html 웹 페이지와 같은 표준 출력 형식으로 변환하는 데 사용됩니다. 이 변환은 기존 XML 문서의 내용을 기반으로 새 문서를 만듭니다. XSLT는 이론적으로 임의의 계산이 가능하도록 합니다.

## XSLT 파일 형식

XLST 파일 형식에는 모든 텍스트 편집기에서 볼 수 있는 일반 텍스트 형식의 변환 지침이 포함되어 있습니다. 언어가 세 번 수정되었습니다.

* `XSLT 1.0` - XSLT 1.0은 1999년 11월 W3C 권장 사항으로 게시되었습니다.
* `XSLT 2.0` - 정규식을 사용한 문자열 조작, 날짜, 시간 및 기간을 조작하기 위한 함수 및 연산자, 다중 출력 문서, 그룹화, 더 풍부한 유형 시스템 및 강력한 유형 검사와 같은 수정 사항이 포함됩니다.
* `XSLT 3.0` - 2017년 6월 8일 W3C 권장 사항의 일부가 되었으며 주요 새 기능에는 스트리밍 변환, 대형 스타일시트의 모듈성을 개선하기 위한 패키지, 예를 들어 xsl:try 명령을 사용하여 동적 오류 처리 개선, XSLT가 XML은 물론 JSON도 처리할 수 있도록 지도와 배열을 지원합니다.

### XSLT 예

다음 예제는 [w3schools](https://www.w3schools.com/xml/xsl_intro.asp)에서 가져온 것입니다.
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## 참조 ##

* [XSLT - 위키피디아 작성](https://en.wikipedia.org/wiki/XSLT)
* [XSLT 요소](https://en.wikipedia.org/wiki/XSLT_elements)

