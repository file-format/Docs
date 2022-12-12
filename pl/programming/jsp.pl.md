{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP — format pliku stron serwera Java",
  "description":"Poznaj format pliku JSP na przykładzie JSP i interfejsach API, które mogą tworzyć i otwierać pliki JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Czym jest plik JSP?
Pliki JSP są realizowane jako dynamiczne, oparte na danych strony dla aplikacji internetowych Java. JSP oznacza Strony Serwera Java; może być zrealizowany jako rozszerzenie serwletu, ponieważ zapewnia większą funkcjonalność niż serwlet, na przykład język wyrażeń. JSP i Servlet wykonują razem to samo zadanie w starszych aplikacjach internetowych Java. Z perspektywy programowania najbardziej wyraźną różnicą między nimi jest to, że w przypadku serwletów piszesz program w Javie, a następnie osadzasz w nim statyczne znaczniki (takie jak HTML), podczas gdy JSP zaczyna się od skryptu lub znaczników po stronie klienta, a następnie osadza znaczniki JSP w połącz swoją stronę z zapleczem Java.

## Format pliku JSP
Plik zapisany z **rozszerzeniem pliku jsp** zawiera następujące sekcje w podanej kolejności:

1. Otwieranie komentarzy
2. Dyrektywy strony JSP
3. Opcjonalne dyrektywy biblioteki znaczników
4. Opcjonalne deklaracje JSP
5. Kod HTML i JSP

### Otwieranie komentarzy
Plik JSP lub plik fragmentów zaczyna się od komentarza w stylu po stronie serwera:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Powyższy komentarz pojawia się tylko po stronie serwera, ponieważ jest usuwany podczas renderowania strony w przeglądarce. Komentarz może zawierać informacje o autorze (autorach), datę i informację o prawach autorskich rewizji, identyfikator i opis strony JSP dla programistów. Połączenie znaków „@(#)” jest rozpoznawane przez niektóre programy jako wskazujące początek identyfikatora.

### Dyrektywy strony JSP
Dyrektywa strony JSP definiuje atrybuty powiązane ze stroną JSPF w czasie tłumaczenia. Specyfikacja JSP nie nakłada ograniczeń co do liczby dyrektyw strony JSP, które można zapisać na jednej stronie. Zobacz następujący przykład:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Jeśli dyrektywa strony przekracza normalną szerokość strony JSP, dyrektywa jest dzielona na kilka wierszy:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Opcjonalne dyrektywy biblioteki znaczników
Na stronie JSP dyrektywa biblioteki znaczników deklaruje niestandardowe biblioteki znaczników. Krótka dyrektywa może być zadeklarowana w jednym wierszu. Wiele dyrektyw bibliotek znaczników jest ułożonych razem w tym samym miejscu w treści strony JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Opcjonalne deklaracje JSP
  


Metody i zmienne zadeklarowane w pliku JSPF powinny istnieć w deklaracjach JSP. Te metody i zmienne są podobne do deklaracji w języku programowania Java, dlatego należy przestrzegać odpowiednich konwencji kodowych. Deklaracje są zwykle zapisywane w jednym <%! ... %> Blok deklaracji JSP, aby scentralizować deklaracje w jednym obszarze treści strony JSP. spójrz na następujące przykłady:

#### Różne bloki deklaracji:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Preferowany blok deklaracji:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Kod HTML i JSP
Ta sekcja strony JSP zawiera treść HTML strony JSP i kod JSPF, takie jak wyrażenia JSP, skryptlety i instrukcje JavaBeans.

## Cykl życia strony JSP

Fazowy przepływ strony JSP jest podany tutaj:

- Tłumaczenie strony JSP
- Kompilacja strony JSP
- Ładowanie klas (program ładujący klasy ładuje plik klasy)
- Tworzenie instancji (jest tworzony obiekt wygenerowanego serwletu).
- Inicjalizacja (kontener wywołuje metodę jspInit()).
- Przetwarzanie żądania (kontener wywołuje metodę _jspService()).
- Destroy (kontener wywołuje metodę jspDestroy()).

{{< figure src="../jsp.jpg" alt="Format pliku JSP" >}}

## Przykład JSP

Nauka o technologiach JSP jest obecnie bardzo łatwa, ponieważ wiele samouczków JSP jest dostępnych w Internecie. Poniższy przykład JSP dotyczy przetwarzania zamówienia poprzez aktualizację odpowiednich rekordów w bazie danych.
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


 


## Bibliografia

* [Konwencje kodu dla stron JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Samouczek JSP](https://www.javatpoint.com/jsp-tutorial)

