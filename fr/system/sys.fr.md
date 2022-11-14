{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extension", "fichier", "format", "système", "Pilote", "Fichier système", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Format de fichier système",
  "description":"En savoir plus sur le format de fichier SYS et les API qui peuvent créer et ouvrir des fichiers SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Qu'est-ce qu'un fichier SYS ? ##

Les fichiers SYS sont des "fichiers système" utilisés dans les applications Windows OS et MS-DOS. Ces fichiers ne peuvent pas être ouverts directement et se composent du pilote et de la configuration de l'appareil. Les fichiers SYS sont chargés de contenir les fichiers des fonctions principales du système d'exploitation. Ceux-ci sont considérés comme des fichiers critiques du pilote de périphérique et peuvent également être utilisés lorsqu'un problème du pilote de course doit être résolu. Ceux-ci sont responsables du bon fonctionnement d'un système informatique et les fichiers .sys doivent être corrects et complets.


## Spécification technique ##

Les fichiers .sys sont en fait le sous-ensemble du format [BMP](/fr/image/bmp) car il n'autorise que des combinaisons spécifiques. Le format habituel de ces fichiers est comme LOGOS.SYS, LOGOW.SYS et LOGO.SYS. Tous les autres fichiers n'ont pas ce format.

Ces fichiers sont principalement utilisés dans le répertoire *C* de Windows au moment de l'installation. La plupart des problèmes liés aux pilotes de périphériques sont résolus en mettant à jour le système d'exploitation Windows. Les détails et les informations de ces fichiers peuvent être visualisés à l'aide des programmes intégrés du système d'exploitation Windows. Ceux-ci comprennent également les références aux différents modules d'un système d'exploitation.
Certains des exemples de fichiers système sont :

* IO.SYS (Ceux-ci stockent les pilotes de périphérique du système d'exploitation du disque)
* MSDOS.SYS (Ceux-ci contiennent le noyau ou le code principal du système d'exploitation)
* CONFIG.SYS (ceux-ci contiennent diverses options de configuration)
* KEYBOARD.SYS (Ceux-ci contiennent des informations relatives à la disposition du clavier)
* COUNTRY.SYS (Ceux-ci contiennent des informations relatives au pays et à la page de code)

## Format de fichier SYS ##

Microsoft a développé les fichiers avec les extensions .sys. Les variables et les fonctions sont incluses dans les fichiers SYS. Ceux-ci sont principalement utilisés par le système d'exploitation Microsoft. Ces fichiers sont principalement situés dans le répertoire racine du disque :

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Certains avertissements courants concernant les fichiers SYS sont les suivants :

* Les noms de ces fichiers ne doivent pas être modifiés car ces fichiers sont responsables des fonctions principales et des variables du système d'exploitation
* Ces fichiers ne doivent pas être supprimés car leur absence de ces fichiers peut provoquer des erreurs
* Les fichiers .sys ne doivent pas être téléchargés depuis Internet tant que vous n'êtes pas sûr de la légitimité de la source
* Il ne faut pas jouer avec ces fichiers car les modifier ou jouer avec ceux-ci provoque de graves erreurs système
* Si ces fichiers sont corrompus par un virus ou un logiciel malveillant, ils doivent être réinstallés

## Exemple SYS ##

Voici un exemple de fichier de configuration système SYS simple :

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
