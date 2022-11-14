{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Formato file pagine server Java",
  "description":"Scopri il formato di file JSP con l'esempio JSP e le API che possono creare e aprire file JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Che cos'è un file JSP?
I file JSP sono realizzati come pagine dinamiche basate sui dati per le tue applicazioni web Java. JSP significa Java Server Pages; può essere realizzato come un'estensione di Servlet perché abilita più funzionalità rispetto a servlet come il linguaggio delle espressioni. JSP e Servlet svolgono lo stesso lavoro insieme nelle vecchie applicazioni Web Java. Dal punto di vista della programmazione, la differenza più chiara tra loro è che con i servlet si scrive un programma Java e quindi si incorpora il markup statico (come HTML) in quel codice, mentre JSP inizia con lo script o il markup lato client, quindi incorpora i tag JSP in collega la tua pagina al backend Java.

## Formato file JSP
Un file salvato con **estensione file jsp** contiene le seguenti sezioni nell'ordine in cui sono elencate:

1. Commenti di apertura
2. Direttive della pagina JSP
3. Direttive opzionali della libreria di tag
4. Dichiarazioni JSP facoltative
5. Codice HTML e JSP

### Commenti di apertura
Un file JSP o un file frammento inizia con un commento di stile lato server:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Il commento sopra è apparso solo sul lato server perché viene rimosso durante il rendering della pagina nel browser. Il commento può contenere le informazioni sugli autori, la data e l'avviso di copyright della revisione, un identificatore e una descrizione della pagina JSP per gli sviluppatori. La combinazione dei caratteri " @(#)" viene riconosciuta da alcuni programmi come un'indicazione dell'inizio di un identificatore.

### Direttiva/e di pagina JSP
Una direttiva di pagina JSP definisce gli attributi associati alla pagina JSPF al momento della traduzione. La specifica JSP non impone un vincolo sul numero di direttive di pagina JSP che possono essere scritte in una singola pagina. Vedere il seguente esempio:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Se una direttiva di pagina supera la larghezza normale di una pagina JSP, la direttiva viene suddivisa in più righe:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Direttive opzionali della libreria di tag
Nella pagina JSP, una direttiva della libreria di tag dichiara le librerie di tag personalizzate. Una breve direttiva può essere dichiarata in una singola riga. Più direttive della libreria di tag sono impilate insieme nella stessa posizione all'interno del corpo della pagina JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Dichiarazioni JSP facoltative
  


I metodi e le variabili dichiarati in un file JSPF dovrebbero essere presenti nelle dichiarazioni JSP. Questi metodi e variabili sono simili alle dichiarazioni nel linguaggio di programmazione Java, ed è per questo che dovrebbero essere seguite le convenzioni di codice pertinenti. Le dichiarazioni sono generalmente scritte in un unico < %! ... %> Blocco dichiarazione JSP, per centralizzare le dichiarazioni all'interno di un'area del corpo della pagina JSP. guarda i seguenti esempi:

#### Blocchi di dichiarazione diversi:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Blocco di dichiarazione preferito:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Codice HTML e JSP
Questa sezione di una pagina JSP contiene il corpo HTML della pagina JSP e il codice JSPF, tali espressioni JSP, scriptlet e istruzioni JavaBeans.

## Ciclo di vita di una pagina JSP

Il flusso di pagine JSP per fasi è riportato qui:

- Traduzione della pagina JSP
- Compilazione della pagina JSP
- Classloading (il classloader carica il file di classe)
- Istanziazione (viene creato l'oggetto del servlet generato).
- Inizializzazione (il contenitore richiama il metodo jspInit()).
- Elaborazione della richiesta (il contenitore richiama il metodo _jspService()).
- Distruggi (il contenitore richiama il metodo jspDestroy()).

{{< figure src="../jsp.jpg" alt="Formato file JSP" >}}

## Esempio JSP

L'apprendimento delle tecnologie JSP è molto facile oggigiorno perché molti tutorial JSP sono disponibili su Internet. Il seguente esempio JSP serve per elaborare l'ordine, aggiornando i record appropriati nel database.
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


 


## Riferimenti

* [Convenzioni sul codice per le pagine JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutorial JSP](https://www.javatpoint.com/jsp-tutorial)

