{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion 마크업 언어 파일",
  "description" :"CFML 파일이 무엇이며 CFML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## .CFML 파일이란?

확장자가 .cfml인 파일은 웹 페이지를 생성하는 데 사용되는 ColdFusion 마크업 언어 파일입니다. 이것은 프로그래머가 ColdFusion 응용프로그램을 개발하는 방법을 정의하는 데 사용되는 일련의 규칙을 나타냅니다. ColdFusion은 [ASP](/ko/web/asp/), [PHP](/ko/web/php/) 등과 같은 다른 기술보다 적은 비용으로 서버 측 웹 응용 프로그램을 빠르게 생성하는 데 사용되는 프로그래밍 언어입니다. CML 파일을 열 수 있는 응용 프로그램에는 Adobe ColdFusion 2018, Adobe ColdFusion Builder 및 Adobe Dreamweaver가 있습니다.

## CFML 파일 형식 - 추가 정보

CFML 파일은 마크업 파일이며 태그 형태의 웹 요소를 포함합니다. 이것은 모든 텍스트 편집기에서 열고 편집할 수 있는 텍스트 파일입니다. CFML 파일은 [HTML](/ko/web/html/)과 유사한 여러 태그로 구성되며 일반적으로 여는 태그와 닫는 태그로 구성됩니다. 이러한 태그에는 하나 이상의 속성도 포함될 수 있습니다.

### 태그 구문

다음은 CFML 태그의 일반화된 구문입니다.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

대부분의 태그는 속성을 허용하며 다음과 같이 정의됩니다.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

이러한 태그 중 일부는 다음 구문을 사용하여 여러 속성도 허용합니다.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML 코드 예

다음은 실제 CFML 태그인 `cfoutput` 태그를 사용하는 예입니다.

```
<cfoutput>
  #firstname#
</cfoutput>
```

## 참고문헌

* [콜드퓨전](https://www.quackit.com/coldfusion/tutorial/)

