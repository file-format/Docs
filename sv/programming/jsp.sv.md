{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages File Format",
  "description":"Lär dig mer om JSP-filformat med JSP-exempel och API:er som kan skapa och öppna JSP-filer.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Vad är JSP fil?
JSP-filerna realiseras som de dynamiska, datadrivna sidorna för dina Java-webbapplikationer. JSP betyder Java Server Pages; kan realiseras som en tillägg till Servlet eftersom det möjliggör mer funktionalitet än servlet som uttrycksspråk. JSP och Servlet gör samma jobb tillsammans i äldre Java-webbapplikationer. Ur ett programmeringsperspektiv är den tydligaste skillnaden mellan dem att med servlets skriver du Java-program och sedan bäddar in statisk uppmärkning (som HTML) i den koden, medan JSP börjar med klientsidans skript eller markering, och bäddar sedan in JSP-taggar för att anslut din sida till Java-backend.

## JSP filformat
En fil sparad med **jsp filtillägg** innehåller följande avsnitt i den ordning de är listade:

1. Öppningskommentarer
2. JSP-sidedirektiv(er)
3. Valfria direktiv(er) om taggbibliotek
4. Valfri JSP-deklaration(er)
5. HTML- och JSP-kod

### Öppningskommentarer
En JSP-fil eller fragmentfil börjar med en stilkommentar på serversidan:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Ovanstående kommentar visas endast på serversidan eftersom den tas bort när sidan renderas i webbläsaren. Kommentaren kan innehålla information om författaren/författarna, datumet och copyrightmeddelandet för revisionen, en identifierare och en beskrivning av JSP-sidan för utvecklare. Att kombinera tecknen " @(#)" känns igen av vissa program som indikerar början på en identifierare.

### JSP Siddirektiv(er)
Ett JSP-sidedirektiv definierar attribut som är associerade med JSPF-sidan vid översättningstidpunkten. JSP-specifikationen sätter ingen begränsning på hur många JSP-sidedirektiv som kan skrivas på en enda sida. Se följande exempel:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Om ett siddirektiv överskrider den normala bredden på en JSP-sida, delas direktivet upp i flera rader:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Valfria direktiv(er) om taggbibliotek
På JSP-sidan deklarerar ett taggbiblioteksdirektiv anpassade taggbibliotek. Ett kort direktiv kan deklareras på en enda rad. Flera taggbiblioteksdirektiv staplas ihop på samma plats i JSP-sidans kropp:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Valfri JSP-deklaration(er)
  


De metoder och variabler som deklareras i en JSPF-fil bör finnas i JSP-deklarationer. Dessa metoder och variabler liknar deklarationer i programmeringsspråket Java, och det är därför de relevanta kodkonventionerna bör följas. Deklarationer skrivs vanligtvis i en enda < %! ... %> JSP-deklarationsblock, för att centralisera deklarationer inom ett område av JSP-sidans kropp. titta på följande exempel:

#### Disparata deklarationsblock:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Föredraget deklarationsblock:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML och JSP-kod
Den här delen av en JSP-sida innehåller HTML-kroppen för JSP-sidan och JSPF-koden, sådana JSP-uttryck, scriptlets och JavaBeans-instruktioner.

## Livscykeln för en JSP-sida

Det fasmässiga JSP-sidflödet ges här:

- Översättning av JSP-sidan
- Sammanställning av JSP-sida
- Klassladdning (klassladdaren laddar klassfil)
- Instantiering (objektet för den genererade servleten skapas).
- Initialisering (behållaren anropar jspInit()-metoden).
- Bearbetning av begäran (behållaren anropar metoden _jspService()).
- Destroy (behållaren anropar metoden jspDestroy()).

{{< figure src="../jsp.jpg" alt="JSP filformat" >}}

## JSP-exempel

Att lära sig om JSP-teknikerna är väldigt enkelt nu för tiden eftersom många JSP-handledningar finns tillgängliga över internet. Följande JSP-exempel är för att bearbeta beställningen genom att uppdatera lämpliga poster i databasen.
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


 


## Referenser

* [Kodkonventioner för JavaServer-sidorna](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

