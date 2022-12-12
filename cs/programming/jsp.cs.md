{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages File Format",
  "description":"Další informace o formátu souboru JSP s příkladem JSP a rozhraními API, která mohou vytvářet a otevírat soubory JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Co je soubor JSP?
Soubory JSP jsou realizovány jako dynamické stránky založené na datech pro vaše webové aplikace Java. JSP znamená Java Server Pages; lze realizovat jako rozšíření servletu, protože umožňuje více funkcí než servlet, jako je výrazový jazyk. JSP a Servlet dělají stejnou práci společně ve starších Java webových aplikacích. Z hlediska programování je mezi nimi nejzřetelnější rozdíl v tom, že pomocí servletů napíšete program Java a poté do tohoto kódu vložíte statické označení (jako HTML), zatímco JSP začíná skriptem nebo označením na straně klienta a poté vložíte značky JSP do připojte svou stránku k backendu Java.

## Formát souboru JSP
Soubor uložený s **příponou souboru jsp** obsahuje následující sekce v pořadí, v jakém jsou uvedeny:

1. Otevírání komentářů
2. Direktivy stránky JSP
3. Volitelné direktivy knihovny značek
4. Nepovinné prohlášení JSP
5. HTML a JSP kód

### Úvodní komentáře
Soubor JSP nebo soubor fragmentu začíná komentářem stylu na straně serveru:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Výše uvedený komentář se zobrazuje pouze na straně serveru, protože je odstraněn při vykreslování stránky v prohlížeči. Komentář může obsahovat informace o autorovi (autorech), datum a upozornění na autorská práva revize, identifikátor a popis stránky JSP pro vývojáře. Kombinace znaků " @(#)" je některými programy rozpoznána jako označení začátku identifikátoru.

### Směrnice stránky JSP
Direktiva stránky JSP definuje atributy spojené se stránkou JSPF v době překladu. Specifikace JSP neklade žádné omezení na to, kolik direktiv stránky JSP lze zapsat na jednu stránku. Viz následující příklad:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Pokud direktiva stránky přesahuje běžnou šířku stránky JSP, je direktiva rozdělena do několika řádků:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Volitelné směrnice pro knihovnu značek
Na stránce JSP direktiva knihovny značek deklaruje vlastní knihovny značek. Krátkou direktivu lze deklarovat na jednom řádku. Více direktiv knihovny značek je naskládáno dohromady na stejném místě v těle stránky JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Nepovinná deklarace JSP
  


Metody a proměnné deklarované v souboru JSPF by měly existovat v deklaracích JSP. Tyto metody a proměnné jsou podobné jako deklarace v programovacím jazyce Java, a proto je třeba dodržovat příslušné konvence kódu. Prohlášení se obvykle píší v jediném < %! ... %> Blok deklarací JSP pro centralizaci deklarací do jedné oblasti těla stránky JSP. podívejte se na následující příklady:

#### Nesourodé deklarační bloky:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Preferovaný deklarační blok:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Kód HTML a JSP
Tato část stránky JSP obsahuje tělo HTML stránky JSP a kód JSPF, jako jsou výrazy JSP, skriptlety a instrukce JavaBeans.

## Životní cyklus stránky JSP

Fázový tok stránky JSP je uveden zde:

- Překlad stránky JSP
- Kompilace stránky JSP
- Classloading (classloader načte soubor třídy)
- Instanciace (vytvoří se objekt generovaného servletu).
- Inicializace (kontejner vyvolá metodu jspInit()).
- Zpracování požadavku (kontejner vyvolá metodu _jspService()).
- Destroy (kontejner vyvolá metodu jspDestroy()).

{{< figure src="../jsp.jpg" alt="Formát souboru JSP" >}}

## Příklad JSP

Učení se o technologiích JSP je v dnešní době velmi snadné, protože na internetu je k dispozici mnoho výukových programů JSP. Následující příklad JSP je pro zpracování objednávky aktualizací příslušných záznamů v databázi.
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


 


## Reference

* [Konvence kódu pro stránky JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Výukový program JSP](https://www.javatpoint.com/jsp-tutorial)

