{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages-bestandsindeling",
  "description":"Meer informatie over JSP-bestandsindeling met JSP-voorbeeld en API's die JSP-bestanden kunnen maken en openen.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Wat is een JSP-bestand?
De JSP-bestanden worden gerealiseerd als de dynamische, datagestuurde pagina's voor uw Java-webapplicaties. De JSP betekent Java Server Pages; kan worden gerealiseerd als een uitbreiding op Servlet omdat het meer functionaliteit mogelijk maakt dan servlet zoals expressietaal. De JSP en Servlet doen hetzelfde werk samen in oudere Java-webapplicaties. Vanuit een programmeerperspectief is het meest duidelijke verschil tussen beide dat je met servlets een Java-programma schrijft en vervolgens statische opmaak (zoals HTML) in die code insluit, terwijl JSP begint met het client-side script of opmaak en vervolgens JSP-tags insluit in verbind uw pagina met de Java-backend.

## JSP-bestandsindeling
Een bestand dat is opgeslagen met de **jsp-bestandsextensie** bevat de volgende secties in de volgorde waarin ze worden vermeld:

1. Opmerkingen openen
2. JSP-paginarichtlijn(en)
3. Optionele tagbibliotheekrichtlijn(en)
4. Optionele JSP-aangifte(n)
5. HTML- en JSP-code

### Openingsreacties
Een JSP-bestand of fragmentbestand begint met een opmerking in de stijl van de server:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Bovenstaande opmerking wordt alleen aan de serverzijde weergegeven omdat deze wordt verwijderd tijdens het weergeven van de pagina in de browser. De opmerking kan de informatie over de auteur(s), de datum en de copyrightmelding van de revisie, een identifier en een beschrijving over de JSP-pagina voor ontwikkelaars bevatten. Het combineren van de tekens " @(#)" wordt door bepaalde programma's herkend als het begin van een identifier.

### JSP-paginarichtlijn(en)
Een JSP-paginarichtlijn definieert attributen die bij vertaling aan de JSPF-pagina zijn gekoppeld. De JSP-specificatie legt geen beperking op aan het aantal JSP-paginarichtlijnen dat op één pagina kan worden geschreven. Zie het volgende voorbeeld:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Als een pagina-instructie de normale breedte van een JSP-pagina overschrijdt, wordt de richtlijn opgedeeld in verschillende regels:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Optionele tagbibliotheekrichtlijn(en)
Op de JSP-pagina declareert een tagbibliotheekrichtlijn aangepaste tagbibliotheken. Een korte richtlijn kan in een enkele regel worden gedeclareerd. Meerdere tagbibliotheekrichtlijnen worden op dezelfde locatie in de hoofdtekst van de JSP-pagina gestapeld:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Optionele JSP-aangifte(n)
  


De methoden en variabelen die in een JSPF-bestand worden gedeclareerd, moeten aanwezig zijn in JSP-declaraties. Deze methoden en variabelen zijn vergelijkbaar met declaraties in de programmeertaal Java, en daarom moeten de relevante codeconventies worden gevolgd. Declaraties worden meestal geschreven in een enkele <%! ... %> JSP-aangifteblok, om aangiften te centraliseren binnen één gebied van de hoofdtekst van de JSP-pagina. kijk naar de volgende voorbeelden:

#### Verschillende aangifteblokken:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Voorkeursaangifteblok:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML- en JSP-code
Dit gedeelte van een JSP-pagina bevat de HTML-body van de JSP-pagina en de JSPF-code, zoals JSP-expressies, scriptlets en JavaBeans-instructies.

## Levenscyclus van een JSP-pagina

De fasegewijze JSP-paginastroom wordt hier gegeven:

- Vertaling van JSP-pagina
- Compilatie van JSP-pagina
- Classloading (de classloader laadt het klassenbestand)
- Instantiatie (Object van de gegenereerde Servlet wordt gemaakt).
- Initialisatie (de container roept de jspInit()-methode aan).
- Verwerking van verzoeken (de container roept de _jspService()-methode aan).
- Vernietigen (de container roept de jspDestroy()-methode aan).

{{< figure src="../jsp.jpg" alt="JSP-bestandsindeling" >}}

## JSP-voorbeeld

Leren over de JSP-technologieën is tegenwoordig heel eenvoudig omdat er veel JSP-zelfstudies beschikbaar zijn via internet. Het volgende JSP-voorbeeld is voor het verwerken van de bestelling, door de juiste records in de database bij te werken.
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


 


## Referenties

* [Codeconventies voor de JavaServer-pagina's](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP-zelfstudie](https://www.javatpoint.com/jsp-tutorial)

