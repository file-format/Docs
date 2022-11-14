{
  "date" : "2019-10-11",
  "keywords" :[ "fichier tar", "format de fichier tar", "qu'est-ce qu'un fichier tar", "fichier", "exemple tar", "extension de fichier tar","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Format de fichier d'archive Unix",
  "description":"Découvrez ce qu'est un fichier Tar et les API qui peuvent créer et ouvrir des fichiers TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier TAR ?

Les fichiers avec l'extension .tar sont des archives créées avec un utilitaire basé sur Unix pour collecter un ou plusieurs fichiers. Plusieurs fichiers sont stockés dans un format non compressé avec la prise en charge de l'ajout de fichiers ainsi que de dossiers à l'archive. L'utilitaire TAR sur Unix est basé sur des commandes, mais les fichiers ainsi créés sont pris en charge par la plupart des systèmes d'archivage de fichiers sur presque tous les systèmes d'exploitation. Il a été créé pour la première fois en 1979 par les laboratoires AT&T Bell et des versions ultérieures ont été publiées au fil du temps.

## Format de fichier TAR

TAR est un format de fichier ouvert avec des spécifications complètes disponibles pour la référence du développeur. Sa structure de fichiers a été normalisée dans POSIX.1-1988 et plus tard dans POSIX.1-2001. Les ensembles de données créés par tar conservent des informations sur les paramètres du système de fichiers tels que :

* Nom
* Horodatage
* La possession
* Autorisations d'accès aux fichiers
* Organisation du répertoire

Un fichier Tar n'a pas de nombre magique. Il contient une série de blocs où chaque bloc est de BLOCKSIZE octets.

Chaque fichier archivé est représenté par un bloc d'en-tête qui décrit le fichier, suivi de zéro ou plusieurs blocs qui donnent le contenu du fichier. À la fin du fichier d'archive, il y a deux blocs de 512 octets remplis de zéros binaires comme marqueur de fin de fichier. Un système raisonnable devrait écrire un tel marqueur de fin de fichier à la fin d'une archive, mais ne doit pas supposer qu'un tel bloc existe lors de la lecture d'une archive. En particulier, GNU tar émet toujours un avertissement s'il ne le rencontre pas.

Les blocs peuvent être bloqués pour les opérations d'E/S physiques. Chaque enregistrement de n blocs (où n est défini par l'option blocking-factor = 512-size de tar) est écrit avec une seule opération "write()". Sur les bandes magnétiques, le résultat d'une telle écriture est un enregistrement unique. Lors de l'écriture d'une archive, le dernier enregistrement de blocs doit être écrit en taille réelle, avec des blocs après le bloc zéro contenant tous les zéros. Lors de la lecture d'une archive, un système raisonnable devrait gérer correctement une archive dont le dernier enregistrement est plus court que le reste, ou qui contient des enregistrements inutiles après un bloc zéro.

### En-tête de goudron

Comme tout autre en-tête de fichier, l'enregistrement d'en-tête de fichier tar contient des métadonnées sur un fichier et est indiqué dans le tableau suivant.


|Décalage du champ|Taille du champ (octets)|Champ
---|---|---|
|0|100|Nom de fichier
|100|8|Mode fichier
|108|8|ID utilisateur numérique du propriétaire
|116|8|ID utilisateur numérique du groupe
|124|12|Taille du fichier en octets (base octale)
|136|12|Heure de la dernière modification au format numérique Unix (octal)
|148|8|Somme de contrôle pour l'enregistrement d'en-tête
|156|1|Indicateur de lien (type de fichier)
|157|100|Nom du fichier lié

Les champs inutilisés sont remplis avec des octets NUL. Un en-tête comprend 257 octets qui sont remplis avec des octets NUL pour le remplir à un enregistrement de 512 octets.

## Références ##

* [TAR - Par Wikipédia](https://en.wikipedia.org/wiki/Tar_(informatique))
* [Format de base TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

