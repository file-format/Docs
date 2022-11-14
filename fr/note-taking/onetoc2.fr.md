{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Format de fichier Microsoft OneNote",
  "description":"En savoir plus sur le format de fichier ONETOC2 et les API qui peuvent créer et ouvrir des fichiers ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'ONETOC2 ? ##

Ceux qui ont travaillé avec l'application [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) ont peut-être remarqué la présence de fichiers .onetoc2 dans le dossier du bloc-notes. Microsoft OneNote crée un fichier binaire .onetoc2 en tant que table des matières pour conserver un index sur l'ordre des différentes sections de prise de notes dans un bloc-notes. Un bloc-notes est une collection de fichiers de section qui sont stockés dans le même répertoire. Le fichier .onetoc2 utilise une collection de propriétés pour spécifier des paramètres tels que l'ordre des sections dans le bloc-notes et la couleur du bloc-notes.

Lorsque vous créez un bloc-notes dans OneNote 2016, il est automatiquement enregistré dans le nouveau format de fichier 2010-2016. Vous aurez besoin de ce format si vous souhaitez que toutes les fonctionnalités de OneNote 2016, telles que les équations mathématiques et les notes liées, fonctionnent correctement.

## Format de fichier ONETOC2 ##

Le format de fichier .onetoc2 est représenté par le format de fichier OneNote Revision Store et est une collection de structures qui spécifient un magasin de révision organisé en espaces d'objets référencés, contenant des objets avec des ensembles de propriétés et contenant un journal des transactions pour assurer l'intégrité des fichiers à travers asynchrone. écrit. Les spécifications complètes pour le format de fichier .onetoc2 sont disponibles [en ligne](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) et peuvent être consultées pour le développement d'applications .

### Structure du fichier ###

Un fichier de magasin de révision DOIT commencer par une structure **Header**. Le reste du fichier est partitionné en blocs d'octets, où la taille et la structure de chaque bloc sont spécifiées par le champ qui y fait référence. Un bloc est accessible s'il est référencé par la structure **Header**, ou s'il est référencé par un champ dans un autre bloc accessible. Les données en dehors de la structure **Header** et tous les blocs accessibles DOIVENT être ignorés.

Toutes les structures sont alignées sur des limites de 1 octet. Tous les entiers sont signés sauf indication contraire. Tous les champs sont [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) sauf indication contraire.

#### Entête ####

L'en-tête du fichier .ONE comprend des morceaux qui contiennent différents identifiants uniques et des champs pour la représentation des informations de fichier comme suit :

`guidFileType (16 bytes):` Un GUID qui spécifie le type du fichier de magasin de révision. DOIT être l'une des valeurs du tableau suivant.

|Format de fichier|Valeur
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Un GUID qui spécifie l'identité de ce fichier de magasin de révision. DOIT être unique au monde.

`guidLegacyFileVersion (16 bytes):` DOIT être "{00000000-0000-0000-0000-000000000000}" et DOIT être ignoré.

`guidFileFormat (16 bytes):` Un GUID qui spécifie que le fichier est un fichier de magasin de révision. DOIT être "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 bytes):` Un entier non signé. DOIT être l'une des valeurs du tableau suivant, selon le type de fichier.

|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Un entier non signé. DOIT être l'une des valeurs du tableau suivant, selon le format de fichier de ce fichier.


|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Un entier non signé. DOIT être l'une des valeurs du tableau suivant, selon le format de fichier de ce fichier.
:


|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un entier non signé. DOIT être l'une des valeurs du tableau suivant, selon le format de fichier de ce fichier.


|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

## Références ##

* [[MS-ONESTORE] - Format de fichier OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipédia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

