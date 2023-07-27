
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier APK - Archive de l'ensemble APK",
  "description":"En savoir plus sur ce qu'est un fichier APKS ?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Qu'est-ce qu'un fichier APKS ?

Un fichier avec l'extension .apks est un fichier d'archive qui est une collection de fichiers **APK** du package Android. Chaque fichier APK individuel dans le fichier APKS est généré en tenant compte de divers aspects des appareils. Il s'agit notamment de l'architecture, de la langue, de la densité de l'écran et d'autres fonctionnalités de l'appareil. Les fichiers APKS sont générés par **bundletool**. Il est utilisé pour créer un ensemble d'applications Android et convertir un ensemble d'applications en différents APK pour le déploiement sur les appareils.

## Format de fichier APKS - Plus d'informations

Les fichiers APKS sont enregistrés sous forme de fichiers compressés au format de fichier [ZIP](/fr/compression/zip/).

## Comment générer un fichier APKS ?

Lorsque l'Android App Bundle (AAB) est prêt, son comportement sur Google Play Store peut être testé pour le déploiement sur un appareil. Les fichiers APKS peuvent être générés, à cette fin, à partir de fichiers AAB et installés sur des appareils de test à l'aide de l'outil Android [bundletool](https://developer.android.com/tools/bundletool) de Google. Il fournit des outils de ligne de commande pour créer le fichier d'archive APKS à partir d'APK à l'aide de la commande suivante.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Afin de déployer les APK sur un appareil, le fichier APKS peut être signé avec les informations de signature de l'appareil comme suit.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Références

* [bundletool - ligne de commande](https://developer.android.com/tools/bundletool)

