{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Format de fichier Microsoft OneNote",
  "description":"En savoir plus sur le format de fichier ONE et les API qui peuvent créer et ouvrir des fichiers ONE.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier .ONE ? ##

Les fichiers représentés par l'extension .ONE sont créés par l'application Microsoft OneNote. OneNote vous permet de collecter des informations à l'aide de l'application comme si vous utilisiez votre bloc-notes pour prendre des notes. Les fichiers OneNote peuvent contenir différents éléments qui peuvent être placés à des emplacements non fixes sur les pages du document. Ces éléments peuvent contenir du texte, de l'écriture manuscrite numérisée et des objets copiés à partir d'autres applications, notamment des images, des dessins et des clips multimédias (audio/vidéo). Microsoft propose désormais une version en ligne de OneNote dans le cadre d'Office365 où les notes peuvent être partagées avec d'autres utilisateurs de OneNote sur Internet.

## Spécifications du format de fichier .ONE ##

Le format de fichier OneNote offre un moyen efficace de représenter des notes numériques sous forme d'ensembles hiérarchiques de sections et de pages. Chaque page contient un contenu défini par l'utilisateur dans une structure spécifique pour la représentation par le format de fichier Document Object Model (DOM). Le modèle de données de ce format est illustré ci-dessous.

### Vue d'ensemble de la structure ###

Comme illustré dans le modèle de données pour le format de fichier OneNote, un document OneNote se compose de différents éléments.

#### Section ####

Une section est le conteneur le plus haut dans un fichier OneNote qui contient en outre différents éléments comme :

* Pages
* Métadonnées
* Propriétés

Les métadonnées et les propriétés incluent le nom de la section, l'identification des pages contenues dans la section et l'ordre dans lequel ces pages apparaissent. Le terme « section » fait référence à toutes les pages qui se trouvent dans une section et à la représentation de ces données dans un fichier de magasin de révision OneNote®, qui a une extension de nom de fichier .one.

#### Page ####

Le contenu défini par l'utilisateur dans un document OneNote est contenu dans une page. Les informations sur la page comprennent du texte, des listes, des tableaux, des titres de page, des images et des balises de note. Une page se compose d'objets de plan auxquels la plupart des objets contenus sont ajoutés. Chaque page peut se voir attribuer un nom pour une représentation significative et des objets peuvent également être ajoutés directement aux pages. Une page peut en outre contenir des sous-pages dans un système hiérarchique.

#### Propriétés et jeux de propriétés ####

Le contenu OneNote se compose de propriétés, de jeux de propriétés et d'objets de données de fichier. Un jeu de propriétés est une collection de propriétés qui représente un certain type de contenu. Un objet de données de fichier est un bloc de données binaires contenant des images, des fichiers intégrés ou du contenu audio/vidéo.

#### Bloc-notes OneNote ####

Un bloc-notes est une collection de fichiers de section qui sont stockés dans le même répertoire. Une collection de propriétés est utilisée pour spécifier des paramètres tels que l'ordre des sections dans le bloc-notes et la couleur du bloc-notes.

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

|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un entier non signé. DOIT être l'une des valeurs du tableau suivant, selon le format de fichier de ce fichier.

|Format de fichier|Valeur
--- | --- |
|.un|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Une structure **FileChunkReference32** qui DOIT avoir une valeur de "fcrZero".

`fcrLegacyTransactionLog (8 bytes):` Une structure **FileChunkReference32** qui DOIT être "fcrNil".

`cTransactionsInLog (4 bytes):` Un entier non signé qui spécifie le nombre de transactions dans le journal des transactions. NE DOIT PAS être égal à zéro.

`cbLegacyExpectedFileLength (4 bytes):` Un entier non signé qui DOIT être zéro et DOIT être ignoré.

`rgbPlaceholder (8 bytes):` Un entier non signé qui DOIT être zéro et DOIT être ignoré.

`fcrLegacyFileNodeListRoot (8 octets) :` Une structure **FileChunkReference32** qui DOIT être "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Un entier non signé qui DOIT être zéro et DOIT être ignoré.

`fNeedsDefrag (1 byte):` DOIT être ignoré.

`fRepairedFile (1 byte):` DOIT être ignoré.

`fNeedsGarbageCollect (1 byte):` DOIT être ignoré.

`fHasNoEmbeddedFileObjects (1 byte):` Un entier non signé qui DOIT être zéro et DOIT être ignoré.

`guidAncestor (16 bytes):` Un GUID qui spécifie le champ **Header.guidFile** du fichier de table des matières, donné par le tableau suivant :


|Format du fichier de la table des matières|Emplacement du fichier de la table des matières
--- | --- |
|Section File - .One|Le fichier de la table des matières se trouve dans le même répertoire que ce fichier.
|Fichier de table des matières - .onetoc2|Le fichier de table des matières se trouve dans le répertoire parent de ce fichier.

Si le GUID est {00000000-0000-0000-0000-000000000000}, ce champ ne fait pas référence à un fichier de table des matières.

`crcName (4 bytes):` Un entier non signé qui spécifie la valeur CRC du nom de ce fichier de magasin de révision. Le nom est la représentation Unicode du nom de fichier avec son extension et un caractère nul supplémentaire à la fin. Ce CRC est toujours calculé à l'aide de l'algorithme CRC pour le fichier .one, quel que soit le format de fichier du magasin de révisions.

`fcrHashedChunkList (12 bytes):` Une structure **FileChunkReference64x32** qui spécifie une référence au premier **FileNodeListFragment** dans une liste de blocs hachés. Si la valeur de la structure **FileChunkReference64x32** est "fcrZero" ou "fcrNil", la liste de blocs hachés n'existe pas.

`fcrTransactionLog (12 bytes):` Une structure **FileChunkReference64x32** qui spécifie une référence à la première structure **TransactionLogFragment** dans un journal de transactions. La valeur du champ **fcrTransactionLog** NE DOIT PAS être "fcrZero" et NE DOIT PAS être "fcrNil".

`fcrFileNodeListRoot (12 bytes):` Une structure **FileChunkReference64x32** qui spécifie une référence à une liste de nœuds de fichier racine. La valeur du champ **fcrFileNodeListRoot** NE DOIT PAS être "fcrZero" et NE DOIT PAS être "fcrNil".

`fcrFreeChunkList (12 bytes):` Une structure **FileChunkReference64x32** qui spécifie une référence à la première structure **FreeChunkListFragment**. Si la valeur de la structure **FileChunkReference64x32** est "fcrZero" ou "fcrNil", la liste de blocs libres n'existe pas.

`cbExpectedFileLength (8 bytes):` Un entier non signé qui spécifie la taille, en octets, de ce fichier de magasin de révision.

`cbFreeSpaceInFreeChunkList (8 bytes):` Un entier non signé qui DEVRAIT spécifier la taille, en octets, de l'espace libre spécifié par la liste de blocs libres.

`guidFileVersion (16 octets):` Un GUID. Lorsque la valeur du champ **cTransactionsInLog** ou du champ **guidDenyReadFileVersion** est modifiée, **guidFileVersion** DOIT être remplacé par un nouveau GUID.

`nFileVersionGeneration (8 bytes):` Un entier non signé qui spécifie le nombre de fois que le fichier a changé. DOIT être incrémenté lorsque le champ **guidFileVersion** change.

`guidDenyReadFileVersion (16 octets):` Un GUID. Lorsque le contenu existant du fichier est modifié, à l'exclusion de la structure **Header** du fichier et des blocs de stockage inutilisés, **guidDenyReadFileVersion** DOIT être remplacé par un nouveau GUID.

`grfDebugLogFlags (4 bytes):` DOIT être zéro. DOIT être ignoré.

`fcrDebugLog (12 bytes):` Une structure **FileChunkReference64x32** qui DOIT avoir une valeur "fcrZero". DOIT être ignoré.

`fcrAllocVerificationFreeChunkList (12 bytes):` Une structure **FileChunkReference64x32** qui DOIT être "fcrZero". DOIT être ignoré.

`bnCreated (4 bytes):` Un entier non signé qui spécifie le numéro de build de l'application qui a créé ce fichier de magasin de révisions. DOIT être ignoré.

`bnLastWroteToThisFile (4 bytes):` Un entier non signé qui spécifie le numéro de build de l'application qui a écrit en dernier dans ce fichier de magasin de révisions. DOIT être ignoré.

`bnOldestWritten (4 bytes):` Un entier non signé qui spécifie le numéro de build de l'application la plus ancienne qui a écrit dans ce fichier de magasin de révisions. DOIT être ignoré.

`bnNewestWritten (4 bytes):` Un entier non signé qui spécifie le numéro de build de l'application la plus récente qui a écrit dans ce fichier de magasin de révisions. DOIT être ignoré.

`rgbReserved (728 bytes):` DOIT être zéro. DOIT être ignoré.

## Références ##

* [[MS-ONESTORE] - Format de fichier OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipédia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

