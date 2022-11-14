{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - 자바 서버 페이지 파일 형식",
  "description":"JSP 파일을 생성하고 열 수 있는 JSP 예제와 API를 통해 JSP 파일 형식에 대해 알아보세요.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## .JSP 파일이란?
JSP 파일은 Java 웹 애플리케이션을 위한 동적 데이터 기반 페이지로 실현됩니다. JSP는 Java Server Pages를 의미합니다. 표현 언어와 같은 서블릿보다 더 많은 기능을 가능하게 하기 때문에 서블릿의 확장으로 구현될 수 있다. JSP와 Servlet은 이전 Java 웹 애플리케이션에서 동일한 작업을 함께 수행합니다. 프로그래밍 관점에서 둘 사이의 가장 분명한 차이점은 서블릿을 사용하면 Java 프로그램을 작성한 다음 해당 코드에 HTML과 같은 정적 마크업을 포함하는 반면, JSP는 클라이언트 측 스크립트 또는 마크업으로 시작한 다음 JSP 태그를 페이지를 Java 백엔드에 연결합니다.

## JSP 파일 형식
**jsp 파일 확장명**으로 저장된 파일에는 나열된 순서대로 다음 섹션이 포함되어 있습니다.

1. 댓글 열기
2. JSP 페이지 지시문
3. 선택적 태그 라이브러리 지시문
4. 선택적 JSP 선언
5. HTML과 JSP 코드

### 댓글 열기
JSP 파일 또는 조각 파일은 서버 측 스타일 주석으로 시작합니다.

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
위의 주석은 브라우저에서 페이지를 렌더링하는 동안 제거되기 때문에 서버 측에서만 나타납니다. 주석에는 작성자에 대한 정보, 날짜, 개정판의 저작권 표시, 개발자를 위한 JSP 페이지에 대한 식별자 및 설명이 포함될 수 있습니다. " @(#)" 문자 조합은 특정 프로그램에서 식별자의 시작을 나타내는 것으로 인식됩니다.

### JSP 페이지 지시문
JSP 페이지 지시문은 번역 시 JSPF 페이지와 연관된 속성을 정의합니다. JSP 사양은 단일 페이지에 작성할 수 있는 JSP 페이지 지시문 수에 대한 제약을 부과하지 않습니다. 다음 예를 참조하십시오.

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
페이지 지시문이 JSP 페이지의 일반 너비를 초과하면 지시문이 여러 줄로 나뉩니다.

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### 선택적 태그 라이브러리 지시문
JSP 페이지에서 태그 라이브러리 지시문은 사용자 정의 태그 라이브러리를 선언합니다. 짧은 지시문은 한 줄로 선언할 수 있습니다. 여러 태그 라이브러리 지시문은 JSP 페이지 본문 내 동일한 위치에 함께 쌓입니다.

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### 선택적 JSP 선언
  


JSPF 파일에 선언된 메소드와 변수는 JSP 선언에 존재해야 합니다. 이러한 메서드와 변수는 Java 프로그래밍 언어의 선언과 유사하므로 관련 코드 규칙을 따라야 합니다. 선언은 일반적으로 단일 < %! ... %> JSP 선언 블록, JSP 페이지 본문의 한 영역 내에서 선언을 중앙 집중화합니다. 다음 예를 보십시오.

#### 서로 다른 선언 블록:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### 기본 선언 블록:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML 및 JSP 코드
JSP 페이지의 이 섹션에는 JSP 페이지의 HTML 본문과 JSP 표현식, 스크립틀릿 및 JavaBeans 명령과 같은 JSPF 코드가 있습니다.

## JSP 페이지의 수명 주기

단계별 JSP 페이지 흐름은 다음과 같습니다.

- JSP 페이지 번역
- JSP 페이지 편집
- 클래스 로딩(클래스 로더가 클래스 파일을 로드함)
- 인스턴스화(생성된 서블릿의 객체가 생성됨).
- 초기화(컨테이너가 jspInit() 메서드를 호출함).
- 요청 처리(컨테이너가 _jspService() 메서드를 호출함).
- Destroy(컨테이너가 jspDestroy() 메서드를 호출함).

{{< figure src="../jsp.jpg" alt="JSP 파일 형식" >}}

## JSP 예제

JSP 기술에 대한 학습은 인터넷을 통해 많은 JSP 자습서를 사용할 수 있기 때문에 요즘은 매우 쉽습니다. 다음 JSP 예제는 데이터베이스에서 적절한 레코드를 업데이트하여 주문을 처리하기 위한 것입니다.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## 참고문헌

* [JavaServer 페이지에 대한 코드 규칙](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP 튜토리얼](https://www.javatpoint.com/jsp-tutorial)

