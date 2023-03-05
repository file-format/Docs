{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Format de fichier des pages du serveur Java",
  "description":"En savoir plus sur le format de fichier JSP avec un exemple JSP et des API qui peuvent créer et ouvrir des fichiers JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Qu'est-ce qu'un fichier JSP ?
Les fichiers JSP sont réalisés en tant que pages dynamiques basées sur les données pour vos applications Web Java. Le JSP signifie Java Server Pages ; peut être réalisé comme une extension de Servlet car il permet plus de fonctionnalités que les servlets telles que le langage d'expression. Le JSP et le servlet font le même travail ensemble dans les anciennes applications Web Java. Du point de vue de la programmation, la différence la plus claire entre eux est qu'avec les servlets, vous écrivez un programme Java, puis intégrez un balisage statique (comme HTML) dans ce code, alors que JSP commence par le script ou le balisage côté client, puis intégrez des balises JSP à connectez votre page au backend Java.

## Format de fichier JSP
Un fichier enregistré avec l'**extension de fichier jsp** contient les sections suivantes dans l'ordre dans lequel elles sont répertoriées :

1. Commentaires d'ouverture
2. Directive(s) de page JSP
3. Directive(s) facultative(s) sur la bibliothèque de balises
4. Déclaration(s) JSP facultative(s)
5. Code HTML et JSP

### Commentaires d'ouverture
Un fichier JSP ou un fichier fragment commence par un commentaire de style côté serveur :

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Le commentaire ci-dessus n'apparaît que côté serveur car il est supprimé lors de l'affichage de la page dans le navigateur. Le commentaire peut contenir des informations sur le ou les auteurs, la date et l'avis de copyright de la révision, un identifiant et une description de la page JSP pour les développeurs. La combinaison des caractères " @(#)" est reconnue par certains programmes comme indiquant le début d'un identifiant.

### Directive(s) de page JSP
Une directive de page JSP définit les attributs associés à la page JSPF au moment de la traduction. La spécification JSP n'impose pas de contrainte sur le nombre de directives de page JSP pouvant être écrites dans une seule page. Voir l'exemple suivant :

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Si une directive de page dépasse la largeur normale d'une page JSP, la directive est divisée en plusieurs lignes :

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Directive(s) facultative(s) sur la bibliothèque de balises
Dans la page JSP, une directive de bibliothèque de balises déclare des bibliothèques de balises personnalisées. Une directive courte peut être déclarée sur une seule ligne. Plusieurs directives de bibliothèque de balises sont empilées au même emplacement dans le corps de la page JSP :

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Déclaration(s) JSP facultative(s)
  


Les méthodes et les variables déclarées dans un fichier JSPF doivent exister dans les déclarations JSP. Ces méthodes et variables sont similaires aux déclarations du langage de programmation Java, et c'est pourquoi les conventions de code pertinentes doivent être suivies. Les déclarations sont généralement écrites en un seul < % ! ... %> Bloc de déclaration JSP, pour centraliser les déclarations dans une zone du corps de la page JSP. regardez les exemples suivants :

#### Blocs de déclaration disparates :

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bloc de déclaration préféré :
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Code HTML et JSP
Cette section d'une page JSP contient le corps HTML de la page JSP et le code JSPF, tels que les expressions JSP, les scriptlets et les instructions JavaBeans.

## Cycle de vie d'une page JSP

Le flux de page JSP par phase est donné ici :

- Traduction de la page JSP
- Compilation de la page JSP
- Classloading (le chargeur de classe charge le fichier de classe)
- Instanciation (l'objet de la servlet générée est créé).
- Initialisation (le conteneur invoque la méthode jspInit()).
- Traitement des requêtes (le conteneur invoque la méthode _jspService()).
- Destroy (le conteneur invoque la méthode jspDestroy()).

{{< figure src="../jsp.jpg" alt="Format de fichier JSP" >}}

## Exemple JSP

L'apprentissage des technologies JSP est très facile de nos jours, car de nombreux didacticiels JSP sont disponibles sur Internet. L'exemple JSP suivant concerne le traitement de la commande, en mettant à jour les enregistrements appropriés dans la base de données.
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


 


## Références

* [Conventions de code pour les pages JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutoriel JSP](https://www.javatpoint.com/jsp-tutorial)

