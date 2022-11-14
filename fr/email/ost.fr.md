{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Format de fichier de stockage Outlook",
  "description":"En savoir plus sur le format de fichier OST et les API qui peuvent créer et ouvrir des fichiers OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier OST ?

OST ou les fichiers de stockage hors ligne représentent les données de la boîte aux lettres de l'utilisateur en mode hors ligne sur la machine locale lors de l'enregistrement auprès d'Exchange Server à l'aide de Microsoft Outlook. Il est créé automatiquement lors de la première utilisation de Microsoft Outlook lors de la connexion avec le serveur. Une fois le fichier créé, les données sont synchronisées avec le serveur de messagerie afin qu'elles soient également disponibles hors ligne en cas de déconnexion du serveur de messagerie. Les fichiers OST peuvent utiliser des éléments de boîte aux lettres tels que des e-mails, des contacts, des informations de calendrier, des notes, des tâches et d'autres données similaires. Les utilisateurs peuvent créer des e-mails et d'autres éléments de données dans le fichier OST même en l'absence de connexion au serveur, mais ceux-ci ne seront pas synchronisés avec le serveur. Une fois la connexion établie, le fichier local est à nouveau synchronisé avec le serveur afin que le serveur et la copie locale soient au même niveau d'information.

## Format de fichier OST

Le format de fichier OST (table de stockage hors ligne) et [PST](/fr/email/pst/) (table de stockage personnel) se compose du format de fichier de dossiers personnels (PFF) qui correspond au stockage des e-mails, contacts et rendez-vous de l'utilisateur. Les données d'un fichier PFF sont stockées en petit-boutiste avec toutes les dates et heures représentées en tant que FILETIME en UTC. [MS-PST] définit deux types de PFF :

* Format ANSI 32 bits
* Format Unicode 64 bits

Le format de fichier PST [spécifications] (https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx), tel que disponible auprès de Microsoft, s'applique également au format de fichier OST en tant que gratuit et licence de brevet irrévocable par le biais de la promesse de spécification ouverte. Il se compose des éléments distinctifs suivants :

* En-tête de fichier
* Données d'en-tête de fichier
* Nœud de branche d'index
* Nœud feuille d'index
* Indice de décalage (fichier)
* Index des descripteurs (d'article)
* Descripteurs locaux
* Type de tableau d'articles

### Informations d'en-tête

La structure HEADER du fichier OST est située au tout début du fichier à 0 décalage. Il contient des informations de métadonnées sur le fichier OST et les informations ROOT pour accéder aux structures de données de la couche NDB décrites ci-dessus. La structure HEADER diffère pour les versions Unicode et ANSI du format de fichier OST.

L'en-tête commence par un mot magique de 4 octets **!BDN** représenté par des octets (0x21, 0x42, 0x44, 0x4E). Un autre nombre magique de 2 octets, **SM** (0x53, 0x4D), est situé au décalage 8 à partir du début du fichier. Les informations de version (ANSI ou Unicode) se situent à un décalage de 10 à partir du début du fichier. La valeur hexadécimale (0x17) spécifie le fichier Unicode OST tandis que 0x0E ou 0x0F représente le format de fichier ANSI.

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
|rgnid[] (128 octets)|Un tableau fixe de 32 NID, chacun correspondant à l'un des 32 NID_TYPE possibles (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
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

## Références

* [Format de fichier des dossiers personnels Outlook (.ost)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Spécifications du format de fichier de dossier personnel] (https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

