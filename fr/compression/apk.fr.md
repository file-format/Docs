{
  "date" : "2019-10-11",
  "keywords" :[ "fichier apk", "format de fichier apk", "qu'est-ce qu'un fichier apk", "fichier", "exemple d'apk", "extension de fichier apk","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Qu'est-ce qu'un fichier APK ?",
  "description":"Apprenez à savoir ce qu'est un fichier APK et les API qui peuvent créer et ouvrir des fichiers APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Qu'est-ce qu'un fichier APK ?

Un fichier avec l'extension .apk est un fichier d'application Google Android utilisé pour installer des applications (applications) sur les appareils Android. Il est créé en tant que fichier exécutable à l'aide de l'IDE officiel Google Android Studio, et est téléchargé sur Google Play Store pour être téléchargé et installé par les utilisateurs finaux. Les fichiers APK peuvent être générés et mis à disposition pour une installation manuelle également avant la publication sur Google Play Store. Cela aide à tester la fonctionnalité et le comportement du fichier de package APK généré. Par conséquent, il faut être sûr que le fichier APK provient d'une source fiable et ne contient aucun logiciel malveillant.

## Format de fichier APK

Les fichiers APK sont compressés au format de fichier [ZIP](/fr/compression/zip/) qui peut être ouvert avec n'importe quel logiciel d'ouverture de fichier ZIP. L'extension .apk d'un tel fichier peut être renommée en .zip et ouvrir le fichier dans n'importe quelle application ZIP ou extraire son contenu.

## Contenu du paquet APK

Un seul fichier APK contient tous les fichiers nécessaires à son installation et à son exécution. Un fichier APK, lorsqu'il est extrait avec une application ZIP, contient les fichiers et dossiers suivants.

* `META-INF/` : répertoire contenant le fichier manifeste, la signature et une liste de ressources dans l'archive
* `lib/` : répertoire contenant le code compilé lié à des plates-formes spécifiques telles que armeabi-v7a, x86, arm64-v8a, etc.
* `res/` : répertoire contenant des ressources non compilées telles que des images
* `assets/` : Répertoire contenant les assets des applications, récupérables par AssetManager.
* `androidManifest.xml` : Contient le nom, les informations de version et le contenu du fichier APK
* `classes.dex` : ce sont des classes Java compilées qui peuvent être exécutées sur la machine virtuelle Dalvik et par le Runtime Android
* `resources.arsc` : fichier de ressources compilé tel que des chaînes

## Comment installer le fichier APK sur un appareil Android ?

Afin d'installer un fichier APK sur vos appareils Android, les étapes suivantes peuvent être utilisées.

1. Téléchargez l'APK à l'aide d'un navigateur Web
2. Appuyez dessus - vous devriez alors pouvoir le voir se télécharger sur la barre supérieure de votre appareil
3. Une fois téléchargé, ouvrez Téléchargements, appuyez sur le fichier APK, puis appuyez sur Oui lorsque vous y êtes invité.

Suivre ces étapes lancera l'installation de l'application sur votre appareil.

## Références

* [Format de fichier APK] (https://en.wikipedia.org/wiki/Android_application_package)

