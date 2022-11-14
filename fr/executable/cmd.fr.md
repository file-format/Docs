{
  "date" : "2021-07-12",
  "keywords" :[ "fichier cmd", "qu'est-ce qu'un fichier cmd", "fichier", "exemple cmd", "extension de fichier cmd","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier CMD et les API qui peuvent créer et ouvrir des fichiers CMD.",
  "title" :"CMD - Format de fichier de commande Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Qu'est-ce qu'un fichier CMD ?
Un fichier CMD consiste en un script contenant une ou plusieurs commandes sous forme de texte brut qui sont exécutées afin d'exécuter diverses tâches. Il est similaire à un fichier [BAT](/fr/executable/bat/), qui est également généralement utilisé pour stocker un lot de commandes exécutables. Les fichiers CMD sont largement utilisés dans le système d'exploitation Microsoft Windows. Ces fichiers ont été introduits presque dans les années 90 mais sont toujours utilisés dans le dernier système d'exploitation Windows. Ces fichiers sont généralement écrits pour exécuter plus d'une commande dans une séquence.

## Format de fichier CMD
CMD est un format de fichier utilisé par les programmes exécutables de style CP/M. Il est généralement comparable à [COM](/fr/executable/com/) sous CP/M-80 et [EXE](/fr/executable/exe/) sous DOS. Un fichier CMD contient de 1 à 8 groupes de code ou de données et un en-tête de 128 octets. Chaque groupe peut peser jusqu'à 1 Mo. Les fichiers CMD peuvent également contenir des informations de relocalisation et des extensions système résidentes (RSX) dans ses versions ultérieures. Le CMD est un nouveau venu par rapport au fichier [BAT](/fr/executable/bat/) ; utilisé pour MS-DOS avant la sortie de Windows dans MS-DOS. Bien que vous puissiez toujours enregistrer des fichiers avec l'extension .bat aujourd'hui, de nombreuses personnes utilisent l'extension .cmd pour enregistrer leurs scripts exécutables.

### Spécification du format CMD

Le début de l'en-tête contient la liste des groupes présents dans le fichier ainsi que leurs types. Chaque type peut être utilisé une fois au maximum. Ces types sont :

-Code
- Données
- En plus
- Empiler
- Utilisateur 1
- Utilisateur 2
- Utilisateur 3
- Utilisateur 4
- Code partagé

De même, le préfixe de segment de programme sous DOS, les 256 premiers octets du groupe de données sont nuls. Ils seront remplis par CP/M-86 avec la page zéro. S'il n'y a pas de groupe de données, les 256 premiers octets du groupe de codes seront utilisés à la place.
## Exemple de fichier CMD
Voici un exemple de script CMD pour afficher les informations système.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Références

* [Comment écrire un script CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Fichier CMD (CP/M) - par Wikipédia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

