{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP – файлов формат на страници на Java сървър",
  "description":"Научете за JSP файловия формат с JSP пример и API, които могат да създават и отварят JSP файлове.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Какво е JSP файл?
JSP файловете се реализират като динамични, управлявани от данни страници за вашите Java уеб приложения. JSP означава Java Server Pages; може да се реализира като разширение на Servlet, тъй като позволява повече функционалност от сървлета, като например език за изразяване. JSP и Servlet вършат една и съща работа заедно в по-стари Java уеб приложения. От гледна точка на програмирането, най-ясната разлика между тях е, че със сървлетите пишете програма на Java и след това вграждате статично маркиране (като HTML) в този код, докато JSP започва със скрипта или маркирането от страна на клиента, след което вграждате JSP тагове в свържете страницата си към бекенда на Java.

## JSP файлов формат
Файл, записан с **файлово разширение jsp**, съдържа следните секции в реда, в който са изброени:

1. Начални коментари
2. Директива(и) за JSP страница
3. Директива(и) за библиотека с етикети по избор
4. Незадължителна JSP декларация(и)
5. HTML и JSP код

### Начални коментари
JSP файл или фрагментен файл започва с коментар в стила на сървъра:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Коментарът по-горе се появява само от страна на сървъра, тъй като се премахва при изобразяване на страницата в браузъра. Коментарът може да съдържа информация за автора(ите), датата и известието за авторски права на редакцията, идентификатор и описание на JSP страницата за разработчици. Комбинирането на знаците " @(#)" се разпознава от определени програми като указващо началото на идентификатор.

### Директива(и) за JSP страница
Директива за JSP страница дефинира атрибути, свързани с JSPF страницата по време на превод. JSP спецификацията не налага ограничение за това колко JSP директиви за страница могат да бъдат записани в една страница. Вижте следния пример:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Ако директива за страница надвишава нормалната ширина на JSP страница, директивата се разделя на няколко реда:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Директива(и) за библиотека с етикети по избор
В JSP страницата директива за библиотека с етикети декларира персонализирани библиотеки с етикети. Кратка директива може да бъде декларирана в един ред. Множество директиви на библиотека с етикети са подредени заедно на едно и също място в тялото на JSP страницата:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Незадължителна JSP декларация(и)
  


Методите и променливите, декларирани в JSPF файл, трябва да съществуват в JSP декларации. Тези методи и променливи са подобни на декларациите в езика за програмиране Java и затова трябва да се следват съответните конвенции в кода. Декларациите обикновено се пишат в единичен < %! ... %> JSP декларационен блок, за централизиране на декларации в една област от тялото на JSP страницата. вижте следните примери:

#### Различни декларационни блокове:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Предпочитан декларационен блок:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML и JSP код
Този раздел на JSP страница съдържа HTML тялото на JSP страницата и JSPF кода, като JSP изрази, скриптове и инструкции на JavaBeans.

## Жизнен цикъл на JSP страница

Потокът на JSP страницата по фазите е даден тук:

- Превод на JSP страница
- Компилация на JSP страница
- Classloading (зареждането на класове зарежда файла на класа)
- Инстанциране (Създава се обект на генерирания сървлет).
- Инициализация (контейнерът извиква jspInit() метод).
- Обработка на заявка (контейнерът извиква метода _jspService()).
- Унищожаване (контейнерът извиква jspDestroy() метод).

{{< figure src="../jsp.jpg" alt="JSP файлов формат" >}}

## Пример за JSP

Научаването за JSP технологиите е много лесно в днешно време, защото много JSP уроци са достъпни в интернет. Следният JSP пример е за обработка на поръчката чрез актуализиране на съответните записи в базата данни.
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


 


## Препратки

* [Конвенции за кода за страниците на JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP урок](https://www.javatpoint.com/jsp-tutorial)

