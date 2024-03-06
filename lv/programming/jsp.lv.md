{
  "date": "2021-04-21",
  "keywords": [
"kas ir jsp fails",
"pamācības par jsp",
"jsp nozīmē",
"jsp",
"jsp failus",
"pagarinājumu",
"formātā",
"jsp apmācība",
".jsp",
"jsp piemērs",
"jsp faila paplašinājums",
"kā atvērt jsp failu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP — Java servera lappušu faila formāts",
  "description": "Uzziniet par JSP faila formātu, izmantojot JSP piemēru un API, kas var izveidot un atvērt JSP failus.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-lvp"
}
},
  "lastmod": "2021-05-07"
}

## Kas ir JSP fails?
JSP faili tiek realizēti kā dinamiskas, uz datiem balstītas lapas jūsu Java tīmekļa lietojumprogrammām. JSP nozīmē Java servera lapas; var tikt realizēts kā Servlet paplašinājums, jo tas nodrošina vairāk funkcionalitātes nekā servlet, piemēram, izteiksmes valoda. JSP un Servlet veic vienu un to pašu darbu vecākās Java tīmekļa lietojumprogrammās. No programmēšanas viedokļa visskaidrākā atšķirība starp tām ir tā, ka, izmantojot servlets, jūs rakstāt Java programmu un pēc tam šajā kodā ieguljat statisku marķējumu (piemēram, HTML), turpretim JSP sākas ar klienta puses skriptu vai iezīmēšanu, pēc tam iegulsiet JSP tagus savienojiet savu lapu ar Java aizmugursistēmu.

## JSP faila formāts
Failā, kas saglabāts ar **jsp faila paplašinājumu**, ir šādas sadaļas tādā secībā, kādā tās ir norādītas:

1. Atverot komentārus
2. JSP lapas direktīva(s)
3. Izvēles tagu bibliotēkas direktīva(s)
4. Izvēles JSP deklarācija(-as)
5. HTML un JSP kods

### Atvēršanas komentāri
JSP fails vai fragmenta fails sākas ar servera puses stila komentāru:

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

### JSP lapas direktīva(s)
JSP lapas direktīva nosaka atribūtus, kas saistīti ar JSPF lapu tulkošanas laikā. JSP specifikācija nenosaka ierobežojumu, cik JSP lapas direktīvu var ierakstīt vienā lapā. Skatiet šādu piemēru:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Ja lapas direktīva pārsniedz parasto JSP lapas platumu, direktīva tiek sadalīta vairākās rindās:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Izvēles tagu bibliotēkas direktīva(s)
JSP lapā tagu bibliotēkas direktīva deklarē pielāgotas tagu bibliotēkas. Īsu direktīvu var deklarēt vienā rindā. Vairākas tagu bibliotēkas direktīvas ir sakrautas vienā un tajā pašā vietā JSP lapas pamattekstā:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Izvēles JSP deklarācija(-as)

JSPF failā deklarētajām metodēm un mainīgajiem ir jābūt JSP deklarācijās. Šīs metodes un mainīgie ir līdzīgi deklarācijām Java programmēšanas valodā, un tāpēc ir jāievēro attiecīgās koda konvencijas. Deklarācijas parasti raksta ar vienu < %! ... %> JSP deklarāciju bloks, lai centralizētu deklarācijas vienā JSP lapas pamatteksta apgabalā. apskatiet šādus piemērus:

#### Atšķirīgi deklarāciju bloki:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Vēlamais deklarācijas bloks:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML un JSP kods
Šajā JSP lapas sadaļā ir JSP lapas HTML pamatteksts un JSPF kods, piemēram, JSP izteiksmes, skripti un JavaBeans instrukcijas.

## JSP lapas dzīves cikls

Fāzei atbilstošā JSP lapas plūsma ir norādīta šeit:

- JSP lapas tulkojums
- JSP lapas kompilācija
- Classloading (klases ielādētājs ielādē klases failu)
- Instantiation (tiek izveidots ģenerētā servleta objekts).
- Inicializācija (konteiners izsauc jspInit() metodi).
- Pieprasījuma apstrāde (konteiners izsauc \_jspService() metodi).
- Iznīcināt (konteiners izsauc jspDestroy() metodi).

{{< figure src="../jsp.jpg" alt="JSP faila formāts" >}}

## JSP piemērs

Mācīšanās par JSP tehnoloģijām mūsdienās ir ļoti vienkārša, jo daudzas JSP apmācības ir pieejamas internetā. Šis JSP piemērs ir paredzēts pasūtījuma apstrādei, atjauninot atbilstošos ierakstus datu bāzē.
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
## Atsauces

 * [Koda konvencijas JavaServer lapām](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP apmācība](https://www.javatpoint.com/jsp-tutorial)

