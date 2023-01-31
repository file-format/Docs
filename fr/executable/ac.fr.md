{
  "date" : "2023-01-11",
  "keywords" :["fichier ac", "qu'est-ce qu'un fichier aci", "fichier", "comment ouvrir un fichier ac", "extension de fichier ac","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier AC et les API qui peuvent créer et ouvrir des fichiers ACCDB.",
  "title" :"Format de fichier AC - Fichier de script Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Qu'est-ce qu'un fichier AC ?

Le fichier AC est le fichier de script Autoconf. **Autoconf** est un package extensible de macros M4 qui produit des scripts shell pour configurer automatiquement les packages de code source du logiciel. Ces scripts peuvent adapter les packages à de nombreux types de systèmes de type UNIX sans intervention manuelle de l'utilisateur. Autoconf crée un script de configuration pour un package à partir d'un fichier modèle qui répertorie les fonctionnalités du système d'exploitation que le package peut utiliser, sous la forme d'appels de macro M4.

La production de scripts de configuration à l'aide d'Autoconf nécessite GNU M4. Vous devez installer GNU M4 (au moins la version 1.4.6, bien que 1.4.13 ou une version ultérieure soit recommandée) avant de configurer Autoconf, afin que le script de configuration d'Autoconf puisse le trouver. Les scripts de configuration produits par Autoconf sont autonomes, de sorte que leurs utilisateurs n'ont pas besoin d'avoir Autoconf (ou GNU M4).

## Comment ouvrir le fichier AC?

AC signifie configuration automatique. Il s'agit d'un script généré par GNU Autoconf qui permet d'adapter le code source du logiciel à divers systèmes de type Posix en testant les fonctionnalités nécessaires dans le package. Le script est appelé un fichier AC.

## Principaux composants d'Autotools

Une compréhension des outils automatiques GNU (`automake`, `autoconf` etc.) peut être utile lorsque vous travaillez avec des ebuilds :

Autotools est une collection de packages connexes qui, lorsqu'ils sont utilisés ensemble, suppriment une grande partie de la difficulté liée à la création de logiciels portables. Ces outils, ainsi que quelques fichiers d'entrée relativement simples fournis en amont, sont utilisés pour créer le système de construction d'un paquet.

**Un aperçu de base de la façon dont les principaux composants des outils automatiques s'emboîtent.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Dans une configuration simple :

- Le programme `autoconf` produit un script de configuration depuis `configure.in` ou `configure.ac`.
- Le programme `automake` produit un Makefile.in à partir d'un Makefile.am.
- Le script `configure` est exécuté pour produire un ou plusieurs fichiers Makefile à partir des fichiers Makefile.in.
- Le programme `make` utilise le Makefile pour compiler le programme.

## Références
* [Logiciel Autoconf](https://www.gnu.org/software/autoconf/)
* [Les bases des outils automatiques] (https://devmanual.gentoo.org/general-concepts/autotools/index.html)


