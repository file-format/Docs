{
  "date": "2021-04-21",
  "keywords": [
"hvad er en jsp fil",
"tutorials på jsp",
"jsp betyder",
"jsp",
"jsp filer",
"udvidelse",
"format",
"jsp tutorial",
".jsp",
"jsp eksempel",
"jsp filtypenavn",
"hvordan man åbner en jsp fil"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP - Java Server Pages Filformat",
  "description": "Lær om JSP-filformat med JSP-eksempel og API'er, der kan oprette og åbne JSP-filer.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-dap"
}
},
  "lastmod": "2021-05-07"
}

## Hvad er en JSP fil?
JSP-filerne realiseres som de dynamiske, datadrevne sider til dine Java-webapplikationer. JSP betyder Java Server Pages; kan realiseres som en udvidelse til Servlet, fordi det muliggør mere funktionalitet end servlet såsom udtrykssprog. JSP'en og Servlet udfører det samme arbejde sammen i ældre Java-webapplikationer. Fra et programmeringsperspektiv er den mest klare forskel mellem dem, at du med servlets skriver Java-program og derefter indlejrer statisk markup (som HTML) i den kode, hvorimod JSP starter med klientsidescriptet eller markup, og derefter indlejrer JSP-tags for at tilslut din side til Java-backend.

## JSP filformat
En fil gemt med **jsp filtypenavn** indeholder følgende sektioner i den rækkefølge, de er anført:

1. Åbningskommentarer
2. JSP-sidedirektiv(er)
3. Valgfri tagbiblioteksdirektiv(er)
4. Valgfri JSP-erklæring(er)
5. HTML og JSP kode

### Åbningskommentarer
En JSP-fil eller fragmentfil begynder med en kommentar på serversiden:

```
<%--
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description:
  --%>
```
Above comment is appeared only on the server side because it is removed while rendering the page in browser. The comment may contain the information about the author(s), the date, and the copyright notice of the revision, an identifier and a description about the JSP page for developers. Combining the characters " @(#)" is recognized by certain programs as indicating the start of an identifier.

### JSP-sidedirektiv(er)
Et JSP-sidedirektiv definerer attributter knyttet til JSPF-siden på oversættelsestidspunktet. JSP-specifikationen pålægger ikke en begrænsning for, hvor mange JSP-sidedirektiver, der kan skrives på en enkelt side. Se følgende eksempel:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Hvis et sidedirektiv overstiger den normale bredde på en JSP-side, er direktivet opdelt i flere linjer:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Valgfri direktiv(er) om tagbibliotek
På JSP-siden erklærer et tagbiblioteksdirektiv brugerdefinerede tagbiblioteker. Et kort direktiv kan erklæres på en enkelt linje. Flere tag-biblioteksdirektiver er stablet sammen på den samme placering i JSP-sidens krop:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Valgfri JSP-erklæring(er)

De metoder og variabler, der er erklæret i en JSPF-fil, bør eksistere i JSP-erklæringer. Disse metoder og variabler ligner erklæringer i programmeringssproget Java, og det er derfor, de relevante kodekonventioner skal følges. Erklæringer skrives normalt i en enkelt < %! ... %> JSP-erklæringsblok, for at centralisere erklæringer inden for et område af JSP-sidens krop. se på følgende eksempler:

#### Uensartede erklæringsblokke:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Foretrukken erklæringsblok:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML og JSP-kode
Denne sektion af en JSP-side indeholder HTML-teksten på JSP-siden og JSPF-koden, såsom JSP-udtryk, scriptlets og JavaBeans-instruktioner.

## Livscyklus for en JSP-side

Det fasevise JSP-sideflow er givet her:

- Oversættelse af JSP-side
- Kompilering af JSP-side
- Klasseindlæsning (klasseindlæseren indlæser klassefil)
- Instantiering (objektet for den genererede servlet oprettes).
- Initialisering (beholderen kalder jspInit()-metoden).
- Anmodningsbehandling (beholderen kalder \_jspService()-metoden).
- Destroy (beholderen kalder jspDestroy()-metoden).

{{< figure src="../jsp.jpg" alt="JSP filformat" >}}

## JSP eksempel

At lære om JSP-teknologierne er meget let nu om dage, fordi en masse JSP-tutorials er tilgængelige over internettet. Følgende JSP-eksempel er til behandling af ordren ved at opdatere de relevante poster i databasen.
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
## Referencer

 * [Kodekonventioner for JavaServer-siderne](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

