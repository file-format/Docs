{
  "date": "2021-04-21",
  "keywords": [
"Cad is comhad jsp ann",
"Teagaisc ar jsp",
"ciallaíonn jsp",
"jsp",
"comhaid jsp",
"síneadh",
"formáid",
"Teagaisc jsp",
".jsp",
"jsp shampla",
"síneadh comhad jsp",
"Conas comhad jsp a oscailt"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP - Formáid Chomhaid Leathanaigh Freastalaí Java",
  "description": "Foghlaim faoi fhormáid comhaid JSP le sampla JSP agus APIanna ar féidir leo comhaid JSP a chruthú agus a oscailt.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-gap"
}
},
  "lastmod": "2021-05-07"
}

## Cad is comhad JSP ann?
Baintear amach na comhaid JSP mar leathanaigh dhinimiciúla, sonraí-tiomáinte do d'fheidhmchláir ghréasáin Java. Ciallaíonn an JSP Leathanaigh Freastalaí Java; Is féidir é a bhaint amach mar shíneadh ar Servlet toisc go gcumasaíonn sé níos mó feidhmiúlachta ná servlet cosúil le teanga slonn. Déanann an JSP agus Servlet an jab céanna le chéile i bhfeidhmchláir ghréasáin Java níos sine. Ó thaobh ríomhchláraithe de, is é an difríocht is soiléire eatarthu ná go scríobhann tú clár Java le servlets agus go neadaíonn tú marcáil statach (cosúil le HTML) sa chód sin, ach go dtosaíonn JSP le script nó marcáil taobh an chliaint, agus ansin neadaíonn tú clibeanna JSP chuig ceangail do leathanach leis an inneall Java.

## Formáid Chomhaid JSP
Tá na hailt seo a leanas san ord ina bhfuil siad liostaithe i gcomhad a shábháiltear le **iarmhír comhaid jsp**:

1. Tráchtanna a oscailt
2. Treoir(eanna) leathanach JSP
3. Treoir(eanna) roghnacha leabharlainne clibeanna
4. Dearbhú/dearbhuithe roghnacha JSP
5. Cód HTML agus JSP

### Tuairimí Oscailte
Tosaíonn comhad JSP nó comhad blúirí le trácht ar stíl an fhreastalaí:

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

### Treoir(eanna) Leathanach JSP
Sainmhíníonn treoir leathanach JSP tréithe a bhaineann leis an leathanach JSPF tráth an aistriúcháin. Ní chuireann an tsonraíocht JSP srian ar cé mhéad treoir leathanach JSP is féidir a scríobh ar aon leathanach amháin. Féach ar an sampla seo a leanas:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Má sháraíonn treoir leathanaigh ghnáthleithead leathanach JSP, roinntear an treoir ina roinnt línte:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Treoir(eanna) Roghnacha Leabharlainne Clibeanna
I leathanach JSP, dearbhaíonn treoir leabharlainne clibeanna leabharlanna clibeanna saincheaptha. Is féidir treoir ghearr a dhearbhú i líne amháin. Cuirtear treoracha ilchlibeanna leabharlainne le chéile san áit chéanna laistigh de chorp an leathanaigh JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Dearbhú/dearbhuithe roghnacha JSP

Ba cheart na modhanna agus na hathróga a dhearbhaítear i gcomhad JSPF a bheith ann i ndearbhuithe JSP. Tá na modhanna agus na hathróga seo cosúil le dearbhuithe i dteanga ríomhchlárúcháin Java, agus sin an fáth gur chóir na coinbhinsiúin cód ábhartha a leanúint. De ghnáth scríobhtar dearbhuithe i < % amháin! ... %> Bloc dearbhaithe JSP, chun dearbhuithe a lárú laistigh de réimse amháin de chomhlacht leathanaigh an JSP. féach ar na samplaí seo a leanas:

#### Bloic dearbhaithe éagsúla:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bloc dearbhaithe is fearr leat:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Cód HTML agus JSP
Coinníonn an chuid seo de leathanach JSP corp HTML an leathanaigh JSP agus an cód JSPF, na habairtí JSP sin, scriptlets, agus treoracha JavaBeans.

## Saolré leathanach JSP

Tugtar sreabhadh na leathanach JSP céim-chliste anseo:

- Aistriúchán ar Leathanach JSP
- Leathanach JSP a thiomsú
- Luchtú ranga (luchtaíonn an t-ualach ranga comhad ranga)
- Instantiation (Cruthaítear Cuspóir an Servlet Ginte).
- Tionscnamh (baineann an coimeádán modh jspInit()).
- Próiseáil iarratais (baineann an coimeádán modh \_jspService()).
- Scrios (baineann an coimeádán modh jspDestroy()).

{{< figure src="../jsp.jpg" alt="Formáid Chomhaid JSP" >}}

## Sampla JSP

Tá sé an-éasca anois foghlaim faoi theicneolaíochtaí JSP mar go bhfuil go leor ranganna teagaisc JSP ar fáil ar an idirlíon. Is é an sampla JSP seo a leanas chun an t-ordú a phróiseáil, trí na taifid chuí sa bhunachar sonraí a nuashonrú.
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
## Tagairtí

 * [Coinbhinsiúin an Chóid do na Leathanaigh JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [Teagasc JSP](https://www.javatpoint.com/jsp-tutorial)

