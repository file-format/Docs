{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","qu'est-ce qu'un fichier jar","comment ouvrir un fichier jar", "extension", "fichier", "fichier jar","format de fichier jar", "extension .jar " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Format de fichier d'archive Java",
  "description":"En savoir plus sur le format de fichier JAR et les API qui peuvent créer et ouvrir un fichier JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier JAR ?

Un fichier avec l'extension .jar est un fichier d'archive Java qui contient de nombreux fichiers liés à des applications différentes dans un seul fichier. Ce format de fichier a été créé pour réduire la vitesse de chargement d'une applet Java téléchargée dans le navigateur via une transaction HTTP, en évitant de créer plusieurs connexions HTTP. Un seul fichier JAR peut contenir des fichiers de classe Java ([.class](/fr/programming/class/)), [images](/fr/image/) et [sounds](/fr/audio/). Les éléments individuels d'un fichier JAR peuvent être signés numériquement par le développeur de l'application pour authentifier leur origine. Les fichiers JAR sont régulièrement utilisés pour créer des API fonctionnelles contenant des fonctionnalités spécifiques liées à cette API.

## Format de fichier JAR

Les fichiers JAR sont basés sur le populaire [format de fichier ZIP](/fr/compression/zip/) qui archive ses fichiers de contenu individuels dans un seul fichier. Le format de fichier JAR prend en charge les compressions, ce qui réduit la taille du fichier à télécharger et améliore donc encore le temps de téléchargement. L'article [Spécifications du fichier JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) d'Oracle donne des détails complets sur les spécifications internes des fichiers JAR.

### Le fichier manifeste

Lorsqu'un fichier JAR est créé, un fichier manifeste est automatiquement créé à l'intérieur de celui-ci qui contient les informations de métadonnées sur le contenu du fichier JAR. Ce fichier affiche le contenu qui est empaqueté dans le fichier JAR. Un fichier manifeste typique ressemble à ce qui suit qui montre les dossiers et les classes inclus dans le fichier JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Spécifications du manifeste

Les spécifications de manifeste sont définies par Oracle comme suit.

`fichier-manifeste` : saut de ligne de la section principale \*section-individuelle

`main-section` : nouvelle ligne d'informations sur la version \* attribut principal

`version-info` : Manifest-Version : numéro de version

`numéro de version` : chiffre+{.chiffre+}*

`main-attribute` : (tout attribut principal légitime) retour à la ligne

`individual-section` : Nom : valeur newline \*perentry-attribute

`perentry-attribute` : (tout attribut de perentry légitime) retour à la ligne

`nouvelle ligne` : CR LF | LF | CR (non suivi de LF)

`digit`: {0-9}

### JAR exécutable

Les fichiers JAR peuvent également comprendre une application qui peut être exécutée par Java Virtual Machine (JVM) similaire à toute autre application sur le système d'exploitation Microsoft Windows. Dans ce cas, la JVM doit connaître le point d'entrée de l'application, c'est-à-dire n'importe quelle classe avec une méthode principale publique static void. Le fichier manifeste identifie une telle classe avec l'en-tête "Main-Class" au format suivant :

```
Main-Class: com.example.MyClassName
```



## Références

* [Aperçu du fichier JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Format de fichier JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

