{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP 조각 파일 형식",
  "description":"JSPF 파일 형식과 JSPF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## .JSPF 파일이란?
확장자가 .jspf인 파일을 JSP 조각이라고 합니다. 다른 JSP 파일에 포함된 정적 파일. JSPF 파일은 자체적으로 컴파일되지 않지만 포함된 페이지와 함께 컴파일됩니다. 구문은 JSP(Java Server Pages) 코드와 유사합니다. 여기에는 JSP의 단편만 포함됩니다. 전체 JSP 문서를 모두 포함하지 않았습니다.

## JSPF 파일 형식
"JSP 조각"이라는 용어가 JSP 2.0 사양에서 오버로드되므로 "JSP 세그먼트"라는 용어가 대신 사용됩니다. JSP 조각은 .jsp 또는 .jspf 확장자를 사용할 수 있으며 **/WEB-INF/jspf** 또는 나머지 정적 파일과 함께 배치해야 합니다. 완전한 페이지가 아닌 JSP 조각은 .jspf 확장자를 사용해야 하며 **/WEB-INF/jspf**에 위치해야 합니다.

### JSP 또는 JSP 조각 파일 구성
JSP 파일에는 나열된 순서대로 다음 섹션이 포함되어 있습니다.

1. 댓글 열기
2. JSP 페이지 지시문
3. 선택적 태그 라이브러리 지시문
4. 선택적 JSP 선언
5. HTML과 JSP 코드

JSP 또는 JSPF 파일은 모두 **Opening Comment**라는 서버 측 스타일 주석으로 시작합니다.

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
이 주석은 JSP 페이지 렌더링 중에 제거되기 때문에 서버 측에서만 볼 수 있습니다.

## JSP Fragment 파일은 언제 사용합니까?
JSP 페이지에 다른 JSP 페이지에서도 재사용할 수 있는 특정하지만 복잡한 구조가 필요한 경우 이를 처리하는 한 가지 방법은 복합 보기 패턴(Java Blueprints의 패턴 섹션)을 사용하여 조각으로 나누는 것입니다. 예를 들어, JSP 페이지의 프레젠테이션 구조에 다음과 같은 논리적 레이아웃이 있는 경우가 있습니다.

{{< figure src="../jspf.png" alt="JSPF 파일 형식" >}}

이 상황에서 이 복합 JSP 페이지는 다양한 모듈로 변환될 수 있으며 각각은 별도의 JSP 조각이라고 합니다. 그런 다음 JSP 조각을 복합 JSP 페이지의 적절한 위치에 배치할 수 있습니다. 따라서 JSPF 파일은 자체적으로 호출되지 않는 페이지를 포함하기 위해 정적 포함 지시문이 사용될 때 사용되며, 확장자가 .jspf인 파일은 웹 애플리케이션 아카이브( 전쟁).

## JSPF 예제
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## 참고문헌

* [JavaServer 페이지에 대한 코드 규칙](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

