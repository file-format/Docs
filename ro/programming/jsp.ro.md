{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Formatul fișierului paginilor serverului Java",
  "description":"Aflați despre formatul de fișier JSP cu exemplu JSP și API-uri care pot crea și deschide fișiere JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Ce este un fișier JSP?
Fișierele JSP sunt realizate ca pagini dinamice, bazate pe date pentru aplicațiile dvs. web Java. JSP înseamnă Java Server Pages; poate fi realizată ca o extensie a servlet-ului, deoarece permite mai multe funcționalități decât servlet-ul, cum ar fi limbajul de expresie. JSP și Servlet fac aceeași treabă împreună în aplicațiile web Java mai vechi. Din punct de vedere al programării, diferența cea mai clară dintre ele este că, cu servlet-uri, scrieți program Java și apoi încorporați marcaj static (cum ar fi HTML) în acel cod, în timp ce, JSP începe cu script-ul sau marcajul pe partea client, apoi încorporați etichete JSP în conectați-vă pagina la backend-ul Java.

## Format de fișier JSP
Un fișier salvat cu **extensia de fișier jsp** conține următoarele secțiuni în ordinea în care sunt listate:

1. Comentarii de deschidere
2. Directivele de pagină JSP
3. Directive opționale de bibliotecă de etichete
4. Declarații JSP opționale
5. Cod HTML și JSP

### Comentarii de deschidere
Un fișier JSP sau un fișier fragment începe cu un comentariu de stil pe partea serverului:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Comentariul de mai sus apare doar pe partea serverului, deoarece este eliminat în timpul redării paginii în browser. Comentariul poate conține informații despre autor(i), data și notificarea privind drepturile de autor a revizuirii, un identificator și o descriere despre pagina JSP pentru dezvoltatori. Combinarea caracterelor „ @(#)” este recunoscută de anumite programe ca indicând începutul unui identificator.

### Directive privind pagina JSP
O directivă de pagină JSP definește atributele asociate cu pagina JSPF în momentul traducerii. Specificația JSP nu impune o constrângere asupra câte directive de pagină JSP pot fi scrise într-o singură pagină. Vezi următorul exemplu:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Dacă o directivă de pagină depășește lățimea normală a unei pagini JSP, directiva este împărțită în mai multe rânduri:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Directive opționale pentru bibliotecă de etichete
În pagina JSP, o directivă de bibliotecă de etichete declară biblioteci de etichete personalizate. O directivă scurtă poate fi declarată într-o singură linie. Mai multe directive de bibliotecă de etichete sunt stivuite împreună în aceeași locație în corpul paginii JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Declarații JSP opționale
  


Metodele și variabilele declarate într-un fișier JSPF ar trebui să existe în declarațiile JSP. Aceste metode și variabile sunt similare cu declarațiile din limbajul de programare Java și de aceea trebuie respectate convențiile de cod relevante. Declarațiile sunt de obicei scrise într-un singur < %! ... %> Bloc de declarații JSP, pentru a centraliza declarațiile într-o zonă a corpului paginii JSP. uitați-vă la următoarele exemple:

#### Blocuri de declarații diferite:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bloc de declarare preferat:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Cod HTML și JSP
Această secțiune a unei pagini JSP conține corpul HTML al paginii JSP și codul JSPF, astfel de expresii JSP, scriptlet-uri și instrucțiuni JavaBeans.

## Ciclul de viață al unei pagini JSP

Fluxul paginii JSP pe fază este prezentat aici:

- Traducerea paginii JSP
- Compilarea paginii JSP
- Classloading (încărcătorul de clasă încarcă fișierul de clasă)
- Instanțierea (este creat obiectul Servlet-ului generat).
- Inițializare (containerul invocă metoda jspInit()).
- Procesarea cererii (containerul invocă metoda _jspService()).
- Distruge (containerul invocă metoda jspDestroy()).

{{< figure src="../jsp.jpg" alt="Format de fișier JSP" >}}

## Exemplu JSP

Învățarea despre tehnologiile JSP este foarte ușoară în prezent, deoarece o mulțime de tutoriale JSP sunt disponibile pe internet. Următorul exemplu JSP este pentru procesarea comenzii, prin actualizarea înregistrărilor corespunzătoare din baza de date.
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


 


## Referințe

* [Convenții de cod pentru paginile JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutorial JSP](https://www.javatpoint.com/jsp-tutorial)

