{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","fichier shtml", "format de fichier shtml", "type de fichier shtml", "fichier", "type", "qu'est-ce qu'un fichier shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Fichier HTML inclus côté serveur",
  "description":"En savoir plus sur le format de fichier SHTML et les API qui peuvent créer et ouvrir des fichiers SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Qu'est-ce qu'un fichier SHTML ?

Un fichier avec l'extension .shtml est une page Web écrite en [HTML](/fr/web/html/) et comprend des instructions de serveur. Il peut également contenir des inclusions côté serveur similaires aux fichiers ASP pour un chargement plus rapide. Les fichiers côté serveur peuvent également contenir du code exécutable qui peut ralentir le chargement du serveur. Les fichiers SHTML sont similaires au HTML mais ils permettent également l'utilisation de commandes serveur simples. Ces commandes serveur sont exécutées dans un langage de programmation informatique simple appelé Server Side Include (SSI). SHTML a été largement remplacé par d'autres langages de programmation côté serveur tels que [PHP](/fr/programming/php/).

## Format de fichier SHTML

Les fichiers SHTML sont écrits en texte brut et utilisent les [commandes SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) qui sont exécutées côté serveur. Ces commandes côté serveur peuvent même être utilisées pour se connecter à la base de données à l'aide des pilotes de base de données et récupérer les données des utilisateurs à partir des tables.

## Exemple SHTML

Les instructions côté serveur sont utilisées dans des applications telles que le compteur de visiteurs de page ou le calendrier de page Web. L'exemple suivant affiche les quatre premières colonnes des trois premières lignes de la base de données des utilisateurs.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Références

* [Côté serveur inclut] (https://en.wikipedia.org/wiki/Server_Side_Includes)

