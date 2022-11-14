{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "fichier", "extension", "format de fichier", "Word", "Document" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Fichier de document Microsoft Word",
  "description":"En savoir plus sur le format de fichier DOC et les API qui peuvent créer et ouvrir des fichiers DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Qu'est-ce qu'un fichier DOC ?

Les fichiers avec l'extension .doc représentent des documents générés par Microsoft Word ou d'autres documents de traitement de texte au format de fichier binaire. L'extension était initialement utilisée pour la documentation en texte brut sur plusieurs systèmes d'exploitation différents. Il peut contenir plusieurs types de données différents tels que des images, formatées ainsi que du texte brut, des graphiques, des tableaux, des objets intégrés, des liens, des pages, le formatage des pages, les paramètres d'impression et bien d'autres. Le format était populaire pour toutes sortes de documents en raison de la variété d'options qu'il offre aux utilisateurs pour la rédaction de manuels, de propositions, de spécifications, de CV, d'articles ou de tout autre document similaire. La version mise à jour de DOC est [DOCX](/fr/Word%20Processing/DOCX/) qui est basée sur Office OpenXML dont les spécifications sont librement disponibles.

## Bref historique ##

WordPerfect, un produit de [Corel](https://www.corel.com/en/), a utilisé DOC comme extension de son format propriétaire. Dans les années 1980, WordPerfect est resté le choix d'utilisation sur la plupart des ordinateurs en raison de sa disponibilité facile, de sa conformité avec la plupart des machines informatiques et des systèmes d'exploitation. Cependant, WordPerfect a connu sa chute sur le système d'exploitation Windows lorsque Microsoft a introduit Microsoft Word comme son produit pour le format de fichier de documents et a choisi l'extension DOC pour son format propriétaire. Au fur et à mesure que Microsoft Word devenait de plus en plus populaire, le format de fichier DOC a subi plusieurs révisions à partir de Microsoft Word 97 - 2003. C'était en 2007 lorsque le format de fichier DOC par défaut a été remplacé par le format Office Open XML (connu sous le nom de DOCX) et les nouvelles versions de Microsoft Word utilise désormais cette nouvelle extension comme format de fichier par défaut.

## Spécifications du format de fichier DOC - Plus d'informations

Microsoft n'a pas publié les spécifications de format de fichier DOC pendant une longue période jusqu'en 2008. En février 2008, des spécifications de format ont été publiées pour le format de fichier .doc dans le cadre de la promesse de spécification ouverte de Microsoft. Bien que la spécification ne décrive pas toutes les fonctionnalités utilisées par le format DOC, elle donne de nombreuses informations sur les connaissances requises pour travailler avec ce format de fichier. Néanmoins, l'ingénierie inverse est nécessaire pour utiliser les informations disponibles. Les spécifications ont été mises à jour plusieurs fois et la dernière [révision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) est la 8.0 qui a été mise à jour en août 2018 .

### Quelques concepts fondamentaux ###

Avant d'entrer dans les détails des spécifications de format de fichier pour DOC, certains concepts fondamentaux sont nécessaires pour comprendre afin de travailler avec ce format de fichier.

**Base d'informations sur le fichier (Fib) :** La structure Fib contient des informations sur le document et spécifie les pointeurs de fichier vers les différentes parties qui composent le document.
Le Fib est une structure de longueur variable. À l'exception de la partie de base dont la taille est fixe, chaque section est précédée d'un champ de comptage qui spécifie la taille de la section suivante.

**Position du caractère :** CP ou position du caractère représente un entier 32 bits non signé qui sert d'index de base zéro d'un caractère dans le texte du document. L'emplacement et la taille de chaque caractère dans le fichier ne peuvent pas être récupérés directement et doivent être calculés à l'aide d'un algorithme prédéfini. Les personnages incluent :

* Texte du document
* Ancres d'objets tels que des notes de bas de page ou des zones de texte
* Caractères de contrôle tels que les marques de paragraphe et les marques de cellule de tableau

**PLC :** La structure PLC est un tableau de CP suivi d'un tableau d'éléments de données. Les éléments de données de tout API doivent avoir la même taille de zéro octet ou plus, et pour cette raison, le nombre de CP doit être supérieur d'un au nombre d'éléments de données. Les structures API sont de différents types où chaque type spécifie si les CP en double sont autorisés ou non pour ce type. Une structure API se compose de :

* **aCP (longueur variable) :** Un tableau d'éléments CP. Chaque type de structure **PLC** spécifie la signification des éléments CP et la plage autorisée.
* **aData (longueur variable) :** Chaque type de structure **PLC** spécifie la structure et la signification des éléments de données, toute restriction sur le nombre d'éléments de données et toute restriction sur les données qu'ils contiennent. Il spécifie également la relation entre les éléments de données et les PC correspondants.

**Sélection valide :** Les constructions de fichiers .DOC sont principalement décrites par une gamme de CP. Il existe un certain nombre de [règles](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) spécifiées par Microsoft à suivre dans ce cas.

**STTB :** Le STTB est une table de chaînes composée d'un en-tête suivi d'un tableau d'éléments. La valeur **cData** spécifie le nombre d'éléments contenus dans le tableau.

**Stockage des propriétés :** Un fichier Word peut avoir différents éléments tels que du texte, des paragraphes, des tableaux, des images et des sections où chacun peut avoir ses propres propriétés. Les propriétés de ceux-ci sont stockées dans le fichier Word en tant que différences par rapport à la valeur par défaut. De telles différences sont spécifiées par PR1 qui consiste en un modificateur de propriété unique (Sprm) et son opérande. Une application peut déterminer l'ensemble final de propriétés en appliquant des listes de **Prl**.

**Protection par mot de passe :** Les fichiers Word peuvent également être protégés par un mot de passe, pour lequel l'un des mécanismes suivants peut être utilisé.

* Obfuscation XOR
* Chiffrement RC4 du document binaire Office
* Chiffrement du document binaire Office RC4 CryptoAPI

Si FibBase.fEncrypted et FibBase.fObfuscation valent tous les deux 1, le fichier est obscurci à l'aide de l'obscurcissement XOR.

Si FibBase.fEncrypted est 1 et FibBase.fObfuscation est 0, le fichier est chiffré à l'aide du chiffrement Office Binary Document RC4 ou du chiffrement Office Binary Document RC4 CryptoAPI, avec EncryptionHeader stocké dans les premiers octets FibBase.lKey du flux Table. EncryptionHeader.EncryptionVersionInfo spécifie le mécanisme de chiffrement utilisé pour chiffrer le fichier.

### Structure du fichier ###

Un fichier Word binaire dans son originalité est un fichier composé OLE qui comprend plusieurs stockages et flux. Ces stockages et flux ont leur propre structure et taille, qui spécifient les paramètres d'écriture et de lecture. Ceux-ci sont:

#### Flux de documents Word ####

Ce flux contient le texte du document et d'autres informations référencées à partir d'autres parties du fichier. Le flux n'a pas de structure prédéfinie autre que le FIB au début qui est obligatoire et doit être à l'offset 0. Ce flux ne doit pas dépasser 2147 Mo.

#### 1TableStream ou 0TableStream ####

Un fichier Word binaire peut contenir des flux de table appelés flux 1Table ou flux 0Table. Au moins l'un d'entre eux doit être présent dans le document. Cependant, si un document contient à la fois des flux 1Table et 0Table, seul le flux référencé par base.fWhichTblStm est utilisé. Le flux non référencé DOIT être ignoré.
Le flux de table NE DOIT PAS être supérieur à 2 147 Mo.

#### Flux de données ####

Le flux de données n'a pas de structure prédéfinie. Il contient des données référencées à partir du FIB ou d'autres parties du fichier. Ce flux n'a pas besoin d'être présent s'il n'y a pas de références à celui-ci. Le flux de données NE DOIT PAS dépasser 2 147 Mo.

#### Stockage de pool d'objets ####

Le stockage du pool d'objets contient des stockages pour les objets OLE intégrés. Ce stockage n'a pas besoin d'être présent s'il n'y a pas d'objets OLE incorporés dans le document.

#### Stockage de données XML personnalisé ####

Le stockage de données XML personnalisé est un stockage facultatif dont le nom DOIT être "MsoDataStore".

#### Flux d'informations récapitulatives ####

Le flux d'informations récapitulatives est un flux facultatif dont le nom DOIT être "\005SummaryInformation", où \005 est le caractère avec la valeur 0x0005, et non le littéral de chaîne "\005".

#### Flux d'informations sur le résumé du document ####

Le flux d'informations de résumé de document est un flux facultatif dont le nom DOIT être "\005DocumentSummaryInformation", où \005 est le caractère avec la valeur 0x0005, et non le littéral de chaîne "\005".

#### Flux de chiffrement ####

Le flux de chiffrement est un flux facultatif dont le nom DOIT être "chiffrement". Ce flux NE DOIT PAS être présent à moins que les deux conditions suivantes ne soient remplies :

* Le document est chiffré avec Office Binary Document RC4 CryptoAPI Encryption.
* La valeur fDocProps est définie dans EncryptionHeader.Flags.

#### Stockage de macros ####

Le stockage des macros est un stockage facultatif qui contient les macros du fichier. S'il est présent, il DOIT être un stockage racine de projet.

#### Stockage des signatures XML ####

Le stockage des signatures XML est un stockage optionnel dont le nom DOIT être "_xmlsignatures".

#### Flux de signatures ####

Le flux de signatures est un flux facultatif dont le nom DOIT être "_signatures". Ce flux contient des signatures numériques.

#### Stockage de l'espace de données de gestion des droits à l'information ####

Le stockage de l'espace de données de gestion des droits relatifs à l'information est un stockage facultatif dont le nom DOIT être "\006DataSpaces", où \006 est le caractère avec la valeur 0x0006, et non le littéral de chaîne "\006". Si ce stockage est présent, le flux de contenu protégé DOIT également être présent.
Si ce stockage est présent, tous les flux et stockages spécifiés autres que ce stockage et le flux de contenu protégé DEVRAIENT être lus à partir du flux de contenu protégé comme spécifié dans [MS-OFFCRYPTO] et si l'un de ces flux et stockages existe en dehors du contenu protégé Stream, ils DEVRAIENT être ignorés.

#### Flux de contenu protégé ####

Le flux de contenu protégé est un flux facultatif dont le nom DOIT être "\009DRMContent", où \009 est le caractère avec la valeur 0x0009, et non le littéral de chaîne "\009".
Si ce flux est présent, le stockage de l'espace de données de gestion des droits relatifs à l'information DOIT également être présent.

## Références ##

* [Spécifications de formation de fichiers MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Informatique](https://en.wikipedia.org/wiki/Doc_(informatique))

