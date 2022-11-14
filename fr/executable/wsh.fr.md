{
  "date" : "2021-08-27",
  "keywords" :[ "fichier wsh", "format de fichier wsh", "qu'est-ce qu'un fichier wsh", "fichier", "exemple wsh", "extension de fichier wsh","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier WSH et les API qui peuvent créer et ouvrir des fichiers WSH.",
  "title" :"WSH - Fichier de script Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Qu'est-ce qu'un fichier WSH ?
Un fichier avec l'extension .wsh contient des propriétés et des paramètres pour un certain script de langage de programmation tel que VB ou VBS, etc. Le besoin réel de WSH est de les utiliser pour personnaliser l'exécution de certains scripts. WScript ou CScript sont requis pour s'exécuter et les deux sont inclus avec le système d'exploitation Windows. Les fichiers WSH étaient initialement fournis sur Windows 95 sur les disques d'installation en tant que composants configurables et installables facultatifs pour le Panneau de configuration, puis en tant que composant par défaut de Windows 98.

## Format de fichier WSH
WSH (Windows Script Host) peut être utilisé à diverses fins, notamment l'administration, les scripts de connexion et l'automatisation générale. WSH établit un environnement pour l'exécution des scripts. il appelle le moteur de script approprié et alloue un ensemble de services et d'objets avec lesquels le script doit fonctionner. Ces scripts peuvent être exécutés en mode GUI, à partir d'un objet COM ou en mode ligne de commande, offrant une flexibilité à l'utilisateur pour les scripts interactifs ou non interactifs.

### Exemples
Voici un exemple très simple qui montre un VBScript qui utilise l'objet racine WSH COM "WScript" pour afficher un message avec un bouton "OK". Lorsque ce script sera lancé, le moteur CScript ou WScript sera appelé et l'environnement d'exécution sera établi.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Références

* [Windows Script Host - par Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



