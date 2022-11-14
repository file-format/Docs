{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","jhtml 파일", "jhtml 파일 형식", "jhtml 파일 형식", "파일", "유형", "jhtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - 자바 HTML 파일",
  "description":"JHTML 파일 형식과 JHTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## JHTML 파일이란?

확장자가 .jhtml인 파일은 클라이언트가 브라우저에서 이 페이지를 요청할 때 서버에서 실행되는 [Java](/ko/programming/java/) 코드가 있는 [HTML](/ko/web/html/) 파일입니다. 서버는 요청을 처리하고, 함수에 포함된 Java 기능을 실행하고, 클라이언트의 브라우저에 페이지를 반환합니다. JHTML 페이지에 포함된 Java 객체는 이 유형의 페이지에 대한 요청을 처리하기 위해 서버에서 실행됩니다. JHTML 파일은 JDBC(Java [Database](/ko/database/) 연결) 연결을 사용하여 데이터베이스의 정보에 액세스할 수도 있습니다. JHTML 파일은 모든 텍스트 편집기에서 열 수 있으며 Google Chrome, Firefox 및 Safari와 같은 웹 브라우저에서 볼 수 있습니다.

## JHTML 파일 형식

JHTML은 ATG의 독점 기술이며 ATG(Art Technology Group) Dynamo 문서 편집기를 사용하여 작성할 수 있습니다. JHTML 파일은 표준 HTML 및 Java 코드를 사용하여 일반 텍스트 파일 형식으로 작성됩니다. 여기에는 Java 개체를 참조하는 독점 태그 외에 표준 HTML 태그가 포함됩니다. 이러한 페이지가 사용자에 의해 요청되면 HTTP 서버는 요청을 Java 애플리케이션 서버로 전달합니다. JHTML 페이지는 먼저 .java 파일로 변환되고 서블릿으로 실행되는 [.class](/ko/programming/class/) 파일을 생성하도록 컴파일됩니다. 이것은 사용자에게 표시하기 위해 요청하는 브라우저로 다시 반환되는 표준 HTTP 및 HTML 데이터 스트림을 생성합니다. 이는 서버에서 데이터베이스 관련 쿼리를 실행하고 최종 누적 결과를 클라이언트의 브라우저에 반환하는 데 유용합니다.

## 참고문헌

* [HTML 문서의 글로벌 구조](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

