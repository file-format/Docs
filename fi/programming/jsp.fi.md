{
  "date": "2021-04-21",
  "keywords": [
"mikä on jsp-tiedosto",
"jsp:n opetusohjelmat",
"jsp tarkoittaa",
"jsp",
"jsp-tiedostoja",
"laajennus",
"muoto",
"jsp opetusohjelma",
".jsp",
"jsp esimerkki",
"jsp tiedostopääte",
"kuinka avata jsp-tiedosto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP - Java Server Pages -tiedostomuoto",
  "description": "Opi JSP-tiedostomuodosta JSP-esimerkillä ja API-liittymillä, jotka voivat luoda ja avata JSP-tiedostoja.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-fip"
}
},
  "lastmod": "2021-05-07"
}

## Mikä on JSP-tiedosto?
JSP-tiedostot toteutetaan Java-verkkosovellustesi dynaamisina, tietopohjaisina sivuina. JSP tarkoittaa Java-palvelinsivuja; voidaan toteuttaa Servletin laajennuksena, koska se mahdollistaa enemmän toimintoja kuin servlet, kuten lausekekieli. JSP ja Servlet tekevät saman työn yhdessä vanhemmissa Java-verkkosovelluksissa. Ohjelmoinnin näkökulmasta selkein ero niiden välillä on se, että servlettien avulla kirjoitat Java-ohjelman ja upotat sitten staattiset merkinnät (kuten HTML) kyseiseen koodiin, kun taas JSP alkaa asiakaspuolen komentosarjalla tai merkinnöillä ja upottaa sitten JSP-tunnisteet yhdistä sivusi Java-taustajärjestelmään.

## JSP-tiedostomuoto
Tiedosto, joka on tallennettu **jsp-tiedostotunnisteella**, sisältää seuraavat osat siinä järjestyksessä kuin ne on lueteltu:

1. Kommenttien avaaminen
2. JSP-sivudirektiivi(t)
3. Valinnaiset tunnistekirjaston käskyt
4. Valinnaiset JSP-ilmoitukset
5. HTML- ja JSP-koodi

### Kommenttien avaus
JSP-tiedosto tai fragmenttitiedosto alkaa palvelinpuolen tyylikommentilla:

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

### JSP-sivudirektiivi(t)
JSP-sivudirektiivi määrittelee JSPF-sivuun käännöshetkellä liittyvät attribuutit. JSP-määritys ei aseta rajoituksia sille, kuinka monta JSP-sivudirektiiviä voidaan kirjoittaa yhdelle sivulle. Katso seuraava esimerkki:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Jos sivuohje ylittää JSP-sivun normaalin leveyden, käsky jaetaan useille riveille:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Valinnaiset tunnistekirjastodirektiivit
JSP-sivulla tunnistekirjastodirektiivi määrittelee mukautetut tunnistekirjastot. Lyhyt ohje voidaan ilmoittaa yhdellä rivillä. Useita tunnistekirjastokäskyjä on pinottu samaan paikkaan JSP-sivun rungossa:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Valinnaiset JSP-ilmoitukset

JSPF-tiedostossa ilmoitettujen menetelmien ja muuttujien tulee olla olemassa JSP-ilmoituksissa. Nämä menetelmät ja muuttujat ovat samanlaisia kuin Java-ohjelmointikielen ilmoitukset, ja siksi asiaankuuluvia koodikäytäntöjä tulee noudattaa. Ilmoitukset kirjoitetaan yleensä yhdellä < %! ... %> JSP-ilmoituslohko, joka keskittää ilmoitukset yhdelle JSP-sivun rungon alueelle. katso seuraavat esimerkit:

#### Erilaiset ilmoituslohkot:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Ensisijainen ilmoituslohko:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML- ja JSP-koodi
Tämä JSP-sivun osa sisältää JSP-sivun HTML-tekstin ja JSPF-koodin, kuten JSP-lausekkeet, komentosarjat ja JavaBeans-ohjeet.

## JSP-sivun elinkaari

Vaihekohtainen JSP-sivun kulku on annettu tässä:

- JSP-sivun käännös
- JSP-sivun kokoaminen
- Classloading (luokanlataaja lataa luokkatiedoston)
- Instantiation (luodun servletin objekti luodaan).
- Alustus (säilö kutsuu jspInit()-menetelmän).
- Pyynnön käsittely (säilö kutsuu \_jspService()-menetelmän).
- Destroy (säilö kutsuu jspDestroy()-menetelmän).

{{< figure src="../jsp.jpg" alt="JSP-tiedostomuoto" >}}

## JSP esimerkki

JSP-tekniikoista oppiminen on nykyään erittäin helppoa, koska Internetin kautta on saatavilla paljon JSP-opetusohjelmia. Seuraava JSP-esimerkki on tilauksen käsittelyä varten päivittämällä tietokannan asianmukaiset tietueet.
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
## Viitteet

 * [JavaServer-sivujen koodikäytännöt](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

