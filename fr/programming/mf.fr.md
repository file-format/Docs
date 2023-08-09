{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Format de fichier manifeste Java",
  "description":"En savoir plus sur le format de fichier MF et les API qui peuvent créer et ouvrir des fichiers MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier MF ?

Un fichier avec l'extension .mf est un fichier manifeste Java qui contient des informations sur les entrées de fichier [JAR](/fr/programming/jar/) individuelles. Le fichier MF lui-même est contenu dans le fichier JAR et fournit toutes les définitions liées à l'extension et au package. Les fichiers JAR peuvent être produits pour être utilisés comme fichier exécutable. Dans ce cas, le fichier mainfest spécifie la classe principale de l'application qui contient l'instruction **`public static void main`**. Les fichiers manifestes sont nommés MANIFEST.MF et peuvent être ouverts avec n'importe quel éditeur de texte sur les systèmes d'exploitation Windows, MacOS et Linux.

## Spécifications du format de fichier manifeste

[Spécifications du format de fichier manifeste](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) sont disponibles par Oracle dans leur guide pour le format de fichier JAR. Un fichier manifeste comprend des sections principales suivies d'une liste de sections pour les entrées de fichier JAR individuelles. Chaque section suit certaines règles et restrictions.

### Sections principales

Une rubrique principale :

* contient des informations sur la sécurité et la configuration du fichier JAR
* contient des informations sur l'application ou l'extension dont le fichier JAR fait partie
* définit les principaux attributs de chaque élément de manifeste individuel

**Remarque** : Aucun attribut de cette section ne peut être nommé "Nom".

### Sections individuelles

Une section individuelle définit divers attributs pour les packages ou les fichiers d'un fichier JAR. Chaque section doit commencer par un attribut nommé "Name" dont la valeur doit être un chemin relatif vers le fichier, ou une URL absolue référençant des données en dehors de l'archive.

### Spécifications du manifeste

|Attributs|Description|
---|---|
|fichier-manifeste|retour à la ligne de la section principale *section-individuelle|
|main-section|version-info newline *main-attribute|
|info-version|Manifest-Version : numéro-version|
|numéro-de-version|chiffre+{.chiffre+}*|
|main-attribute|(tout attribut principal légitime) newline|
|individual-section|Nom : valeur newline *perentry-attribute|
|perentry-attribute|(tout attribut de perentry légitime) newline|
|nouvelle ligne|CR LF | LF | CR (non suivi de LF) |
|chiffre|{0-9}|

## Références

* [Oracle - Format de fichier JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Format de fichier JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

