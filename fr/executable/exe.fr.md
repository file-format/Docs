{
  "date" : "2021-06-30",
  "keywords" :[ "fichier exe", "format de fichier exe", "qu'est-ce qu'un fichier exe", "fichier", "exemple d'exe", "extension de fichier exe","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Un fichier .exe est un fichier exécutable Microsoft exécuté sur le système d'exploitation Windows. En savoir plus sur le format de fichier EXE.",
  "title" :"Qu'est-ce qu'un fichier exécutable EXE ?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Qu'est-ce qu'un fichier EXE ?

Le mot EXE est l'abréviation de **exécutable**. Un fichier .exe est un programme qui peut être exécuté sur le système d'exploitation Microsoft Windows. Les développeurs d'applications publient principalement leurs programmes pour le système d'exploitation Windows au format exécutable sous forme de fichiers exe. C'est le format de fichier standard pour exécuter des applications sous Windows. **Setup.exe**, **Install.exe** et **cmd.exe** sont des noms courants et bien connus des fichiers EXE.

## Format de fichier EXE

Les compilateurs MS-DOS ont été introduits avec les modèles de mémoire ayant la limitation de mémoire 64K. Le concept général consiste à définir différents registres de segments dans le processeur x86 (CS, DS, ES, SS) pour pointer vers les différents ou les mêmes segments, permettant ainsi différents degrés d'accès à la mémoire. Certains modèles de mémoire spécifiques étaient:

- **Tiny** : Tous les accès mémoire sont en 16 bits (registres de segments inchangés). Génère un fichier .COM au lieu d'un fichier .EXE.
- **Petit** : Tous les accès mémoire sont en 16 bits (registres de segments inchangés).
- **Compact** : les adresses de données incluent à la fois le segment et l'offset, rechargeant les registres DS ou ES lors de l'accès et permettant jusqu'à 1 M de données. Les accès au code ne modifient pas le registre CS, autorisant 64 Ko de code.
- **Moyen** : les adresses de code incluent l'adresse du segment, rechargeant CS à l'accès et autorisant jusqu'à 1 M de code. Les accès aux données ne modifient pas les registres DS et ES, permettant 64K de données.
- **Large** : les adresses de code et de données sont des paires (segment, décalage), rechargeant toujours les adresses de segment. L'ensemble de l'espace mémoire de 1 Mo est disponible pour le code et les données.
- **Énorme** : Identique au grand modèle, avec une arithmétique supplémentaire générée par le compilateur pour permettre l'accès à des tableaux supérieurs à 64 Ko.

Les développeurs doivent décider quel modèle doit être sélectionné lors de la création d'un fichier exe.

### Format de fichier EXE portable

Le format de fichier exécutable portable (PE) contient un certain nombre d'en-têtes d'information, voici la liste des en-têtes :

- **En-tête DOS** : l'en-tête MS-DOS assure soit la rétrocompatibilité, soit le déclin gracieux des nouveaux types de fichiers.
- **En-tête PE** : Au décalage 60 (0x3C) à partir du début de l'en-tête DOS se trouve un pointeur vers l'en-tête du fichier PE
- **En-tête COFF** : l'en-tête COFF contient des informations utiles à un exécutable et des informations plus utiles à un fichier objet.
- **En-tête facultatif PE** : l'en-tête facultatif PE apparaît directement après l'en-tête COFF, et certaines sources montrent même que les deux en-têtes font partie de la même structure.
- **Table de section** : Immédiatement après l'en-tête facultatif PE, nous trouvons une table de section. La table de section consiste en un tableau de structures IMAGE_SECTION_HEADER.
- **Sections mappables** : peut économiser de l'espace en mémoire en mappant le code d'une bibliothèque dans plusieurs processus.

## Pouvez-vous exécuter un fichier EXE sur un Mac ?

Les fichiers exe ne sont pas utilisés comme exécutables sur Mac OS. Cependant, si vous souhaitez exécuter un fichier exe sur Mac OS, les méthodes suivantes peuvent être utilisées.

1. **Wine** - Wine est la solution idéale pour les personnes qui souhaitent utiliser leurs applications PC sur des systèmes Mac. C'est un acronyme qui signifie "Wine Is Not A Emulator", ce qui signifie. Wine crée le même environnement de répertoires que celui utilisé par Microsoft afin que vous puissiez exécuter votre application Windows en l'utilisant.
2. **Machines virtuelles** - Créez une machine virtuelle Windows à l'aide de Parallel Desktop ou de VM Virtual Box et exécutez votre application à l'intérieur de la machine virtuelle.
3. **Boot Camp** - L'installation et la configuration de Windows Boot Camp sur Mac OS vous permettent d'exécuter le système d'exploitation Windows sur une machine Mac.

## Références

* [.exe - par Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [Désassemblage x86/Fichiers exécutables Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

