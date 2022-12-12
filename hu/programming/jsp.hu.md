{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages File Format",
  "description":"Tudjon meg többet a JSP fájlformátumról JSP-példával és olyan API-kkal, amelyek JSP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Mi az a JSP fájl?
A JSP-fájlok dinamikus, adatvezérelt oldalakként valósulnak meg a Java webalkalmazásokhoz. A JSP jelentése Java Server Pages; megvalósítható a Servlet kiterjesztéseként, mert több funkcionalitást tesz lehetővé, mint a servlet, mint például a kifejezési nyelv. A JSP és a Servlet ugyanazt a munkát végzi el a régebbi Java webalkalmazásokban. Programozási szempontból a legegyértelműbb különbség köztük az, hogy a servletekkel Java programot írunk, majd statikus jelölést (például HTML-t) ágyazunk be ebbe a kódba, míg a JSP a kliensoldali szkripttel vagy jelöléssel kezdődik, majd a JSP címkéket beágyazja a kódba. csatlakoztassa oldalát a Java háttérrendszerhez.

## JSP fájlformátum
A **jsp fájlkiterjesztéssel** mentett fájl a következő szakaszokat tartalmazza a felsorolás sorrendjében:

1. Megjegyzések megnyitása
2. JSP-oldal direktíva(i)
3. Opcionális címkekönyvtár-irányelv(ek)
4. Opcionális JSP-deklaráció(k)
5. HTML és JSP kód

### Nyitó megjegyzések
A JSP-fájl vagy töredékfájl egy szerveroldali stílusú megjegyzéssel kezdődik:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
A fenti megjegyzés csak a szerver oldalon jelenik meg, mert az oldal böngészőben történő megjelenítése közben eltávolítják. A megjegyzés tartalmazhatja a szerző(k)re vonatkozó információkat, a dátumot és a revízió szerzői jogi megjegyzését, egy azonosítót és egy leírást a fejlesztői JSP-oldalról. A "@(#)" karakterek kombinálását bizonyos programok egy azonosító kezdetének jelzéseként ismerik fel.

### JSP-oldal irányelv(ek)
A JSP-oldal direktíva határozza meg a JSPF-oldalhoz kapcsolódó attribútumokat a fordítási időben. A JSP specifikáció nem szab megkötést arra vonatkozóan, hogy hány JSP-oldal direktíva írható egyetlen oldalra. Lásd a következő példát:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Ha egy oldalirányelv meghaladja a JSP-oldal normál szélességét, az utasítás több sorra oszlik:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Választható címkekönyvtárra vonatkozó irányelv(ek)
A JSP oldalon egy címkekönyvtár direktíva deklarál egyéni címkekönyvtárakat. Egy rövid direktíva egyetlen sorban deklarálható. A több címkekönyvtár direktívája a JSP-oldal törzsén belül ugyanazon a helyen van egymás mellett:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Választható JSP-deklaráció(k)
  


A JSPF-fájlban deklarált metódusoknak és változóknak létezniük kell a JSP-deklarációkban. Ezek a metódusok és változók hasonlóak a Java programozási nyelv deklarációihoz, ezért érdemes követni a vonatkozó kódkonvenciókat. A nyilatkozatokat általában egyetlen < %-ban írják! ... %> JSP deklarációs blokk a deklarációk központosítására a JSP oldal törzsének egy területén. nézze meg a következő példákat:

#### Eltérő deklarációs blokkok:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Preferált deklarációs blokk:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML és JSP kód
A JSP-oldal ezen része tartalmazza a JSP-oldal HTML-törzsét és a JSPF-kódot, például JSP-kifejezéseket, szkriptleteket és JavaBeans-utasításokat.

## A JSP-oldal életciklusa

A fázis szerinti JSP oldalfolyamat itt látható:

- A JSP oldal fordítása
- JSP oldal összeállítása
- Osztálybetöltés (az osztálybetöltő betölti az osztályfájlt)
- Példányosítás (a generált szervlet objektuma létrejön).
- Inicializálás (a tároló meghívja a jspInit() metódust).
- Kérjen feldolgozást (a tároló a _jspService() metódust hívja meg).
- Destroy (a tároló meghívja a jspDestroy() metódust).

{{< figure src="../jsp.jpg" alt="JSP fájlformátum" >}}

## JSP példa

A JSP-technológiák megismerése manapság nagyon egyszerű, mivel sok JSP-oktatóanyag érhető el az interneten. A következő JSP-példa a rendelés feldolgozására szolgál, az adatbázis megfelelő rekordjainak frissítésével.
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


 


## Hivatkozások

* [A JavaServer-oldalak kódegyezményei](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP oktatóanyag](https://www.javatpoint.com/jsp-tutorial)

