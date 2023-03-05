{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Format de fichier du magasin d'informations personnelles Outlook",
  "description":"En savoir plus sur le format de fichier PST et les API qui peuvent créer et ouvrir des fichiers PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PST ?

Les fichiers avec l'extension .pst représentent des fichiers de stockage personnels Outlook (également appelés table de stockage personnel) qui stockent diverses informations utilisateur. Les informations utilisateur sont stockées dans des dossiers de différents types qui incluent des e-mails, des éléments de calendrier, des notes, des contacts et plusieurs autres formats de fichiers. Les fichiers PST sont utilisés pour archiver les données d'e-mailing hors ligne qui peuvent ensuite être chargées et visualisées dans diverses applications.

## Spécifications du format de fichier PST

Le format de fichier PST [spécifications](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) est disponible auprès de Microsoft sous forme de licence de brevet gratuite et irrévocable via la promesse de spécification ouverte .

### Type de format PST

Les formats de fichiers PST sont classés en deux types en fonction de l'encodage du type de fichier. Les fichiers PST encodés ANSI sont des formats de fichiers plus anciens et sont pris en charge par Outlook 2002 et les versions antérieures uniquement. Ces fichiers ont une limite de taille maximale de 2 Go (2^^31^^ octets) et ne prennent pas en charge Unicode. Un type de format de fichier plus moderne, basé sur le codage Unicode, supprime la limite de taille de fichier et peut atteindre une taille de données maximale de 50 Go.

### Organisation logique du format de fichier PST

À la base du format de fichier PST se trouve B-Tree qui maintient les données triées et permet les recherches, l'accès séquentiel, les insertions, les suppressions, etc. en temps logarithmique. La structure globale d'un fichier PST est organisée en trois couches.

![Logical layers of a PST file](/fr/email/PST-1.png "Logical layers of a PST file")

`Couche de base de données de nœuds (NDB)` - La couche de base de données de nœuds se situe au niveau inférieur d'un fichier PST et inclut une base de données de nœuds. Ces nœuds représentent en fait des installations de stockage de niveau inférieur du format de fichier PST. La couche NDB comprend l'en-tête, les informations d'allocation de fichiers, les blocs et les BTrees (Node BTree et Block BTree) du point de vue du stockage. Les nœuds et les blocs de la couche NDB sont liés via Data BID qui est l'une des quatre propriétés de la référence de nœud, c'est-à-dire NID (ID de nœud), Parent NID, Data BID (Block BID) et SubNode BID.

`Lists, Tables and Properties Layer -` La couche LTP fournit la compréhension logique des concepts de niveau supérieur au-dessus de NDB. Outre d'autres éléments, la couche LTP comprend principalement le contexte de propriété (PC) et le contexte de table (TC). PC est une collection de propriétés, tandis que TC représente une matrice bidimensionnelle de collection de propriétés par rapport à la présence de celles-ci. Implémentation efficace des PC et des TC, la couche LTP utilise les deux types de structures de données suivants au sommet du nœud NDB :

* Heap On Node (HN) - permet de sous-allouer le flux de données d'un nœud en petits fragments de taille variable.
* BTree on Heap (BTH) - BTH fournit un moyen pratique et pratique de rechercher dans les données Les PC, décrits ci-dessus, sont implémentés en tant que BTH et c'est pourquoi il est implémenté en construisant à l'intérieur d'une structure HN.

`Messaging Layer -` Des règles de niveau supérieur et une logique métier pour travailler avec des fichiers PST sont implémentées à cette couche. La sortie logique de cette couche se traduit par des objets de dossier, des objets de message, des objets de pièce jointe et des propriétés, ce qui est rendu possible en combinant les couches LTP et NDB. Les règles et les exigences, qui doivent être suivies lors de la modification du contenu PST, sont également définies au niveau de cette couche.

### Organisation physique du format de fichier PST

Le haut niveau d'organisation des fichiers du fichier PST est illustré dans la figure ci-dessous. Ceci est juste un aperçu des différents concepts des éléments logiques du fichier PST.

![Physical organization of the PST file format](/fr/email/PST-2.png "Physical organization of the PST file format")


#### Informations d'en-tête PST

La structure HEADER du fichier PST est située au tout début du fichier à 0 décalage. Il contient des informations de métadonnées sur le fichier PST et les informations ROOT pour accéder aux structures de données de la couche NDB décrites ci-dessus. La structure HEADER diffère pour les versions Unicode et ANSI du format de fichier PST.

L'en-tête commence par un mot magique de 4 octets **!BDN** représenté par des octets (0x21, 0x42, 0x44, 0x4E). Un autre nombre magique de 2 octets, **SM** (0x53, 0x4D), est situé au décalage 8 à partir du début du fichier. Les informations de version (ANSI ou Unicode) se situent à un décalage de 10 à partir du début du fichier. La valeur hexadécimale (0x17) spécifie le fichier PST Unicode tandis que 0x0E ou 0x0F représente le format de fichier ANSI.

|Champ|Description
---|---|
|dwMagic (4 octets)|DOIT être "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|La valeur CRC 32 bits des 471 octets de données à partir de wMagicClient (0ffset 0x0008)
|wMagicClient (2 octets)|DOIT être "{ 0x53, 0x4D }".
|wVer (2 octets)|Version du format de fichier. Cette valeur DOIT être 14 ou 15 si le fichier est un fichier ANSI PST, et DOIT être 23 si le fichier est un fichier Unicode PST.
|wVerClient (2 octets)|Version du format du fichier client. La version qui correspond au format décrit dans ce document est 19. Les créateurs d'un nouveau fichier PST basé sur ce document DEVRAIENT initialiser cette valeur à 19.
|bPlatformCreate (1 octet)|Cette valeur DOIT être définie sur 0x01.
|bPlatformAccess (1 octet)|Cette valeur DOIT être définie sur 0x01.
|dwRéservé (8 octets)|
|bidUnused (8 octets Unicode uniquement)|Remplissage inutilisé ajouté lors de la création du format de fichier Unicode PST.
|bidNextP (Unicode : 8 octets ; ANSI : 4 octets)|Page suivante BID. Les pages ont un compteur spécial pour allouer les valeurs bidIndex. La valeur de bidIndex pour les BID pour les pages est allouée à partir de ce compteur.
|bidNextB (4 octets ANSI uniquement) : |Prochain BID. Cette valeur est le compteur monotone qui indique le BID à attribuer pour le prochain bloc alloué. Les valeurs BID avancent par incréments de 4. Pour plus de détails, voir la section 2.2.2.2.
|dwUnique (4 bytes)|Il s'agit d'une valeur croissante de manière monotone qui est modifiée à chaque fois que la structure HEADER du fichier PST est modifiée. La fonction de cette valeur est de fournir une valeur unique et de s'assurer que les CRC HEADER sont différents après chaque modification d'en-tête.
|rgnid[](128 octets)|Un tableau fixe de 32 NID, chacun correspondant à l'un des 32 NID_TYPE possibles (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 bytes)|Espace inutilisé ; DOIT être mis à zéro. Format de fichier Unicode PST uniquement.
|root (Unicode : 72 octets ; ANSI : 40 octets)|Une structure ROOT (section 2.2.2.5).
|dwAlign (4 bytes)|Octets d'alignement inutilisés ; DOIT être mis à zéro. Format de fichier Unicode PST uniquement.
|rgbFM (128 octets)|FMap obsolète. Ceci n'est plus utilisé et DOIT être rempli avec 0xFF. Les lecteurs DEVRAIENT ignorer la valeur de ces octets.
|rgbFP (128 octets)|FPMap obsolète. Ceci n'est plus utilisé et DOIT être rempli avec 0xFF. Les lecteurs DEVRAIENT ignorer la valeur de ces octets.
|bSentinel (1 octet)|DOIT être défini sur 0x80.
|bCryptMethod (1 octet)|Indique comment les données du fichier PST sont encodées. DOIT être défini sur l'une des valeurs prédéfinies (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRéservé (2 octets)| Réservé; DOIT être mis à zéro.
|bidNextB (8 bytes)|Indique la prochaine valeur de BID disponible. Format de fichier Unicode PST uniquement.
|bidNextB (Unicode UNIQUEMENT : 8 octets)|Prochaine OFFRE. Cette valeur est le compteur monotone qui indique le BID à attribuer pour le prochain bloc alloué. Les valeurs BID avancent par incréments de 4. Pour plus de détails, voir la section 2.2.2.2.
|dwCRCFull (4 bytes)|La valeur CRC 32 bits des 516 octets de données à partir de wMagicClient jusqu'à bidNextB, inclus. Format de fichier Unicode PST uniquement.
|ullRéservé (8 octets)|Réservé ; DOIT être mis à zéro. Format de fichier ANSI PST uniquement.
|dwRéservé (4 octets)|Réservé ; DOIT être mis à zéro. Format de fichier ANSI PST uniquement.
|rgbRéservé2 (3 octets)|
|bRéservé (1 octet) |
|rgbReserved3 (32 octets) |

### Protection des données ###

Pour des raisons de sécurité, les fichiers PST peuvent également être protégés par un mot de passe, ce qui nécessite que l'application de chargement applique un mot de passe avant de pouvoir être visualisé. Le mot de passe appliqué au fichier PST est stocké dans la banque de messages. Cependant, cela ne fournit pas une protection solide des données car le mot de passe peut être supprimé par les outils disponibles. En outre, le mot de passe spécifié par l'utilisateur n'est pas utilisé dans le cadre de la clé pour le codage et le décodage des algorithmes de chiffrement. Ainsi, il n'y a aucun avantage à protéger les données accessibles par des parties non autorisées. Le stockage du mot de passe sous forme de hachage CRC-32 de la chaîne d'origine en fait également une méthode faible pour la sécurité des données contre l'approche par force brute.

## Références ##

* [Format de fichier des dossiers personnels Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Spécifications du format de fichier de dossier personnel](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

