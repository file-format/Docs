{
  "date": "2021-04-21",
  "keywords": [
"kas yra jsp failas",
"jsp vadovėliai",
"jsp reiškia",
"jsp",
"jsp failus",
"pratęsimas",
"formatu",
"jsp pamoka",
".jsp",
"jsp pavyzdys",
"jsp failo plėtinys",
"kaip atidaryti jsp failą"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP – Java serverio puslapių failo formatas",
  "description": "Sužinokite apie JSP failo formatą naudodami JSP pavyzdį ir API, kurios gali kurti ir atidaryti JSP failus.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-ltp"
}
},
  "lastmod": "2021-05-07"
}

## Kas yra JSP failas?
JSP failai realizuojami kaip dinamiški, duomenimis pagrįsti puslapiai jūsų Java žiniatinklio programoms. JSP reiškia Java serverio puslapius; gali būti realizuotas kaip Servlet plėtinys, nes suteikia daugiau funkcijų nei servlet, pvz., išraiškos kalba. JSP ir Servlet atlieka tą patį darbą senesnėse Java žiniatinklio programose. Žvelgiant iš programavimo perspektyvos, aiškiausias skirtumas tarp jų yra tas, kad naudodami servletus rašote Java programą ir tada į šį kodą įdedate statinį žymėjimą (pvz., HTML), tuo tarpu JSP prasideda nuo kliento scenarijaus arba žymėjimo, tada įterpiate JSP žymas prijunkite savo puslapį prie Java sistemos.

## JSP failo formatas
Faile, išsaugotame su **jsp failo plėtiniu**, yra šios skiltys tokia tvarka, kokia jie yra:

1. Komentarų atidarymas
2. JSP puslapio direktyva (-os)
3. Pasirenkama (-os) žymų bibliotekos direktyva (-os)
4. Neprivaloma (-os) JSP deklaracija (-os)
5. HTML ir JSP kodas

### Komentarų atidarymas
JSP failas arba fragmento failas prasideda serverio pusės stiliaus komentaru:

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

### JSP puslapio direktyva (-os)
JSP puslapio direktyva apibrėžia atributus, susijusius su JSPF puslapiu vertimo metu. JSP specifikacija neriboja, kiek JSP puslapio direktyvų galima įrašyti viename puslapyje. Žiūrėkite šį pavyzdį:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Jei puslapio nurodymas viršija įprastą JSP puslapio plotį, direktyva suskaidoma į kelias eilutes:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Pasirenkamos žymų bibliotekos direktyva (-os)
JSP puslapyje žymų bibliotekos direktyva deklaruoja pasirinktines žymų bibliotekas. Trumpa direktyva gali būti paskelbta vienoje eilutėje. Kelios žymų bibliotekos direktyvos yra sukrautos toje pačioje vietoje JSP puslapio turinyje:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Neprivaloma (-os) JSP deklaracija (-os)

JSPF faile deklaruoti metodai ir kintamieji turi būti JSP deklaracijose. Šie metodai ir kintamieji yra panašūs į deklaracijas Java programavimo kalba, todėl reikia laikytis atitinkamų kodo taisyklių. Deklaracijos paprastai rašomos vienu < %! ... %> JSP deklaracijų blokas, skirtas centralizuoti deklaracijas vienoje JSP puslapio turinio srityje. pažvelkite į šiuos pavyzdžius:

#### Skirtingi deklaracijų blokai:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Pageidaujamas deklaracijos blokas:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML ir JSP kodas
Šioje JSP puslapio dalyje yra JSP puslapio HTML turinys ir JSPF kodas, tokios JSP išraiškos, scenarijus ir JavaBeans instrukcijos.

## JSP puslapio gyvavimo ciklas

Fazinis JSP puslapio srautas pateikiamas čia:

- JSP puslapio vertimas
- JSP puslapio sudarymas
- Klasės įkėlimas (klasių įkėlimo programa įkelia klasės failą)
- Inscenizacija (sukuriamas sugeneruoto serverio objektas).
- Inicijuoti (konteineris iškviečia jspInit() metodą).
- Užklausos apdorojimas (konteineris iškviečia \_jspService() metodą).
- Destroy (konteineris iškviečia jspDestroy() metodą).

{{< figure src="../jsp.jpg" alt="JSP failo formatas" >}}

## JSP pavyzdys

Mokymasis apie JSP technologijas dabar yra labai lengvas, nes daug JSP mokymo programų yra prieinama internete. Šis JSP pavyzdys skirtas užsakymo apdorojimui, atnaujinant atitinkamus įrašus duomenų bazėje.
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
## Nuorodos

 * [Kodo konvencijos, skirtos JavaServer puslapiams](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP mokymo programa](https://www.javatpoint.com/jsp-tutorial)

