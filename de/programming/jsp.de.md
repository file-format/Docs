{
  "date" : "2021-04-21",
  "keywords": [ "Was ist eine JSP-Datei", "Tutorials zu JSP", "JSP bedeutet", "JSP", "JSP-Dateien", "Erweiterung", "Format", "JSP-Tutorial", ".jsp" , "jsp-Beispiel", "jsp-Dateierweiterung", "wie man eine jsp-Datei öffnet"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Server Pages-Dateiformat",
  "description":"Erfahren Sie mehr über das JSP-Dateiformat mit JSP-Beispiel und APIs, die JSP-Dateien erstellen und öffnen können.",
  "linktitle" :"JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Was ist eine JSP-Datei?
Die JSP-Dateien werden als dynamische, datengesteuerte Seiten für Ihre Java-Webanwendungen realisiert. Die JSP bedeutet Java Server Pages; kann als Erweiterung von Servlets realisiert werden, da es mehr Funktionalität als Servlets ermöglicht, wie z. B. Ausdruckssprache. Die JSP und das Servlet erledigen in älteren Java-Webanwendungen zusammen dieselbe Aufgabe. Aus Programmierperspektive besteht der deutlichste Unterschied zwischen ihnen darin, dass Sie bei Servlets ein Java-Programm schreiben und dann statisches Markup (wie HTML) in diesen Code einbetten, während JSP mit dem clientseitigen Skript oder Markup beginnt und dann JSP-Tags einbettet Verbinden Sie Ihre Seite mit dem Java-Backend.

## JSP-Dateiformat
Eine mit **jsp-Dateierweiterung** gespeicherte Datei enthält die folgenden Abschnitte in der Reihenfolge, in der sie aufgelistet sind:

1. Kommentare öffnen
2. JSP-Seitendirektive(n)
3. Optionale Tag-Bibliothek-Anweisung(en)
4. Optionale JSP-Deklaration(en)
5. HTML- und JSP-Code

### Eröffnungskommentare
Eine JSP-Datei oder Fragmentdatei beginnt mit einem serverseitigen Stilkommentar:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Der obige Kommentar wird nur serverseitig angezeigt, da er beim Rendern der Seite im Browser entfernt wird. Der Kommentar kann Informationen über den/die Autor(en), das Datum und den Urheberrechtsvermerk der Überarbeitung, eine Kennung und eine Beschreibung der JSP-Seite für Entwickler enthalten. Die Kombination der Zeichen " @(#)" wird von bestimmten Programmen als Beginn einer Kennung erkannt.

### JSP-Seitenrichtlinie(n)
Eine JSP-Seitendirektive definiert Attribute, die der JSPF-Seite zur Übersetzungszeit zugeordnet sind. Die JSP-Spezifikation legt keine Einschränkung fest, wie viele JSP-Seitendirektiven auf einer einzelnen Seite geschrieben werden können. Siehe folgendes Beispiel:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Wenn eine Seitendirektive die normale Breite einer JSP-Seite überschreitet, wird die Direktive in mehrere Zeilen aufgeteilt:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Optionale Tag-Bibliothek-Richtlinie(n)
Auf der JSP-Seite deklariert eine Tag-Bibliotheksanweisung benutzerdefinierte Tag-Bibliotheken. Eine kurze Direktive kann in einer einzigen Zeile deklariert werden. Mehrere Tag-Bibliotheksanweisungen werden an derselben Stelle im Hauptteil der JSP-Seite gestapelt:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Optionale JSP-Deklaration(en)
  


Die in einer JSPF-Datei deklarierten Methoden und Variablen sollten in JSP-Deklarationen vorhanden sein. Diese Methoden und Variablen ähneln Deklarationen in der Programmiersprache Java, weshalb die entsprechenden Codekonventionen eingehalten werden sollten. Deklarationen werden normalerweise in einem einzigen < % geschrieben! ... %> JSP-Deklarationsblock, um Deklarationen innerhalb eines Bereichs des Hauptteils der JSP-Seite zu zentralisieren. sehen Sie sich die folgenden Beispiele an:

#### Unterschiedliche Deklarationsblöcke:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bevorzugter Deklarationsblock:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML- und JSP-Code
Dieser Abschnitt einer JSP-Seite enthält den HTML-Hauptteil der JSP-Seite und den JSPF-Code, z. B. JSP-Ausdrücke, Skriptlets und JavaBeans-Anweisungen.

## Lebenszyklus einer JSP-Seite

Der phasenweise JSP-Seitenfluss ist hier angegeben:

- Übersetzung der JSP-Seite
- Zusammenstellung der JSP-Seite
- Classloading (der Classloader lädt die Klassendatei)
- Instanziierung (Objekt des generierten Servlets wird erstellt).
- Initialisierung (der Container ruft die Methode jspInit() auf).
- Anforderungsverarbeitung (der Container ruft die Methode _jspService() auf).
- Destroy (der Container ruft die Methode jspDestroy() auf).

{{< figure src="../jsp.jpg" alt="JSP-Dateiformat" >}}

## JSP-Beispiel

Das Erlernen der JSP-Technologien ist heutzutage sehr einfach, da viele JSP-Tutorials über das Internet verfügbar sind. Das folgende JSP-Beispiel dient zum Verarbeiten der Bestellung durch Aktualisieren der entsprechenden Datensätze in der Datenbank.
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


 


## Verweise

* [Code-Konventionen für die JavaServer-Seiten](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP-Tutorial](https://www.javatpoint.com/jsp-tutorial)

