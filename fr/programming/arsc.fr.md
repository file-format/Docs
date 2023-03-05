{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","qu'est-ce qu'un fichier arsc","comment ouvrir un fichier arsc", "extension", "fichier", "fichier arsc","format de fichier arsc", "extension de fichier arsc" ,"exemple de fichier arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Fichier de table de ressources de package Android",
  "description":"En savoir plus sur le format de fichier ARSC et les API qui peuvent créer et ouvrir un fichier ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Qu'est-ce qu'un fichier ARSC ?

Un fichier ARSC est un fichier de table de ressources Android qui contient la liste des ressources de l'application dans un format de table. Il contient des informations telles que les noms de ressources, les propriétés et les ID. Les fichiers ARSC font partie des packages APK utilisés pour installer ces applications Android. Toutes les ressources telles que les images, les mises en page, les styles et les chaînes d'une application Android sont converties en fichiers binaires lorsque le fichier APK est généré. Le fichier ARSC est également généré en même temps, contenant la liste de toutes les ressources compilées du programme et leurs identifiants.

## Format de fichier ARSC

Les fichiers d'extension .arsc sont des fichiers binaires générés après que le compilateur, tel que ANT (Eclipse) ou Gradle (AS), compile le code de l'application Android pour produire le fichier [APK](/fr/compression/apk/). Vous pouvez extraire le fichier APK à l'aide de n'importe quel utilitaire d'archivage tel que WinZip pour afficher son contenu, qui sont les fichiers de classe Java compilés, c'est-à-dire classes.dex. En plus de ceux-ci, il contient également ce fichier ARSC qui contient des méta-informations sur :

* Les nœuds XML
* Les attributs
* Les identifiants de ressources

Les ressources d'un fichier APK sont référencées par les ID de ressource, tandis que les attributs sont résolus en une valeur au moment de l'exécution. L'outil Android aapt collecte toutes les ressources définies dans les fichiers au moment de la génération et leur attribue des ID de ressource. Une fois les identifiants attribués aux ressources compilées, un fichier R.java est généré à partir du code source ainsi que de resources.arsc.

## Références

* [Structure de la table des ressources binaires](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

