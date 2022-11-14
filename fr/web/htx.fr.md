{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier HTX - Format de fichier d'extension HTML",
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier HTX et les API qui peuvent créer et ouvrir un fichier HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier HTX ?

Un fichier HTX est en fait un fichier HTML qui contient des variables de données pour afficher les résultats de la requête de base de données sous forme de page Web. Généralement créés avec le logiciel de développement Web Microsoft FrontPage, les fichiers HTX sont enregistrés pour être enregistrés dans le même dossier que le fichier Internet Database Connector (.IDC) correspondant.

Les fichiers HTX peuvent être ouverts avec des applications telles que Microsoft FrontPage et n'importe quel éditeur de texte tel que le Bloc-notes, TextEdit ou Atom.

## Format de fichier HTX

Les fichiers HTX sont enregistrés sous forme de fichier texte brut avec un code permettant de récupérer les données d'une base de données et d'enregistrer des variables pour l'affichage.


### Exemple de fichier HTX

Un exemple de fichier HTX est le suivant qui définit un en-tête de page pour afficher la restriction de requête et les documents affichés sur la page pour l'affichage à l'utilisateur.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

La sortie de cet exemple de code est la suivante.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Comme on peut le voir, le fichier HTX est un modèle qui formate la façon dont les résultats sont renvoyés et affichés aux utilisateurs finaux. Il est écrit au format HTML avec quelques extensions IIS et un service d'indexation. Ces extensions incluent des noms de variables et d'autres codes pour le traitement des résultats.

## Références

* [Formatage des résultats dans le fichier .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

