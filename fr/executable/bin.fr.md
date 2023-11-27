{
"date": "20/07/2023",
   "keywords":[
"POUBELLE",
"Fichier BIN",
"déposer",
"Extension de fichier BIN",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier BIN - Fichier exécutable Unix",
   "description":"Découvrez le format BIN et les API permettant de créer et d'ouvrir des fichiers BIN.",
"linktitle": "BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent" : "executable"
}
},
"lastmod": "20/07/2023"
}

## Qu'est-ce qu'un fichier BIN ?

Un fichier BIN est un fichier exécutable sur les systèmes d'exploitation Unix tels que Linux ou FreeBSD. Il contient un programme compilé composé de code binaire dérivé du code source, le rendant compatible avec l'architecture système sous-jacente. Les fichiers BIN exécutables Unix peuvent être comparés aux fichiers Windows .EXE et aux fichiers macOS .APP en termes de leur rôle en tant que formats exécutables.

Dans le domaine du développement de logiciels pour les systèmes Unix, les fichiers BIN sont couramment utilisés par les développeurs pour empaqueter et distribuer des programmes. Ils offrent un moyen pratique de fournir des logiciels aux utilisateurs, permettant une installation et une exécution faciles. Outre les fichiers BIN, il existe d'autres types d'exécutables Unix, notamment [.ELF](/fr/executable/elf/), .X86, [.RUN](/fr/executable/run/) et .X86_64, chacun adapté à un matériel ou à un matériel spécifique. Configuration requise.

En ce qui concerne la structure interne d'un fichier BIN, il s'agit de données codées que le système d'exploitation Unix utilise pour identifier, lire et exécuter le programme ci-joint. Le système s'appuie sur des signatures ou des en-têtes de fichiers spécifiques pour reconnaître le fichier BIN comme un exécutable, suivi de l'interprétation et de l'exécution des instructions binaires qu'il contient.

Les fichiers BIN sont souvent fournis avec un fichier **INSTALL.TXT** qui fournit des instructions détaillées sur la façon d'installer et de configurer correctement le programme. Cette documentation garantit que les utilisateurs peuvent naviguer avec succès dans le processus d'installation et commencer à utiliser le logiciel sans complications.

## Comment ouvrir le fichier BIN ?

Les fichiers BIN ne sont pas conçus pour être directement ouverts et visualisés. Cependant, vous pouvez exécuter les programmes ou extraire les données qu'ils contiennent. Pour accéder au contenu d'un fichier BIN, suivez ces étapes sur la ligne de commande, en supposant que le nom du fichier BIN est « sample.bin » :

1. **Assurez-vous des autorisations des exécutables :**

Avant d'exécuter le fichier BIN, assurez-vous qu'il dispose des autorisations nécessaires pour être exécuté en tant qu'exécutable. Utilisez la commande :

```
$ chmod +x sample.bin
```

Cette commande accorde au fichier les privilèges exécutables.

2. **Exécutez le fichier BIN :**

Après avoir défini les autorisations de l'exécutable, vous pouvez exécuter le fichier BIN en entrant la commande suivante :

```
$ ./sample.bin
```

**Avertissement**

_Faites preuve de prudence lorsque vous manipulez des fichiers BIN téléchargés ou envoyés par courrier électronique, car ils peuvent potentiellement être utilisés par des cybercriminels pour distribuer des logiciels malveillants. Exécutez uniquement des fichiers BIN provenant de sources fiables pour atténuer le risque d'attaques exécutables malveillantes._

## Autres fichiers BIN

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.bin**.

- [BIN - Fichier codé MacBinary](/fr/compression/bin/)
- [BIN - Fichier image de disque binaire](/fr/disc-and-media/bin/)
- [BIN - Fichier de stratégie informatique BlackBerry](/fr/settings/bin/)
- [BIN - ROM du jeu Sega Genesis](/fr/game/bin/)
- [BIN - Image du BIOS PSX PlayStation](/fr/game/bin-pcsx/)

## Les références

* [Comment exécuter des fichiers binaires sous Linux](https://linuxhint.com/execute-binary-files-in-linux/)


