{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "fichier stml", "format de fichier stml", "type de fichier stml", "fichier", "type", "qu'est-ce qu'un fichier stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Fichier HTML SSI",
  "description":"En savoir plus sur le format de fichier STML et les API qui peuvent créer et ouvrir des fichiers STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Qu'est-ce qu'un fichier STML ?

Un fichier avec l'extension .stml est une page Web avec des instructions côté serveur qui sont exécutées lorsqu'un utilisateur charge la page dans un navigateur Web. Les pages STML contiennent du code côté serveur qui contient des inclusions côté serveur pour effectuer des tâches qui ne sont pas possibles avec du HTML brut. Bien que similaire à [HTML](/fr/web/html/), STML offre plus de puissance en exécutant les commandes sur le serveur, également appelées Server Side Include (SSI). Avec l'introduction de nouveaux langages de programmation avec des scripts côté serveur tels que PHP, l'utilisation de STML est réduite bien qu'il soit toujours pris en charge par toutes les technologies côté serveur. Les fichiers STML peuvent être ouverts dans n'importe quel éditeur de texte et modifiés pour mettre à jour les commandes.

## Format de fichier STML

STML est basé sur un format de fichier texte ascii simple lisible par l'homme. Cependant, il suit la syntaxe telle que définie et exercée à l'aide des [commandes SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) qui sont exécutées côté serveur. Comme tout autre langage de script côté serveur, STML peut utiliser les commandes côté serveur pour effectuer des tâches telles que le compteur de visiteurs de la page, le calendrier de la page Web, la récupération des enregistrements de la base de données, etc.

## Exemple STML

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

* [Côté serveur inclut](https://en.wikipedia.org/wiki/Server_Side_Includes)

