{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extension", "fichier dbf", "format de fichier dbf", "Type de fichier de base de données", "Format de fichier de base de données", "qu'est-ce qu'un fichier dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DBF et les API qui peuvent créer et ouvrir des fichiers DBF.",
  "title" :"DBF - Fichier de base de données dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Qu'est-ce qu'un fichier DBF ?
Le fichier avec l'extension .dbf est un fichier de base de données utilisé par une application de système de gestion de base de données appelée **dBASE**. Initialement, la base de données dBASE s'appelait Project Vulcan ; lancé par **Wayne Ratliff** en 1978. Le type de fichier DBF a été introduit avec dBASE II en 1983. Il organise plusieurs enregistrements de données avec des champs de type Array. Le logiciel de base de données **xBase** qui est populaire en raison de sa compatibilité avec une large gamme de formats de fichiers ; prend également en charge les fichiers DBF.

## Format de fichier DBF
Le format de fichier DBF appartient au système de gestion de base de données dBASE mais il peut être compatible avec xBase ou d'autres logiciels SGBD. La version initiale du fichier dbf consistait en un simple tableau dans lequel des données pouvaient être ajoutées, modifiées, supprimées ou imprimées à l'aide du jeu de caractères ASCII. Au fil du temps, .dbf a été amélioré et des fichiers supplémentaires ont été ajoutés pour augmenter les fonctionnalités et les capacités du système de base de données.

Dans dBASE moderne, un fichier DBF se compose d'un en-tête, des enregistrements de données et du marqueur EOF (End of File)

- L'en-tête contient des informations sur le fichier, telles que le nombre d'enregistrements et le nombre de types de champs utilisés dans les enregistrements.
- Les enregistrements contiennent les données réelles.
- La fin du fichier est marquée par un seul octet, de valeur 0x1A.

### En-tête de fichier
La disposition de l'en-tête de fichier dans dBase est donnée dans le tableau suivant :

| Octet | Sommaire | Signification |
---|---|---|
| 0 | 1 octet | Fichier dBASE valide pour DOS ; les bits 0 à 2 indiquent le numéro de version, le bit 3 indique la présence d'un fichier mémo dBASE pour DOS, les bits 4 à 6 indiquent la présence d'une table SQL, le bit 7 indique la présence de tout fichier mémo (soit dBASE m PLUS, soit dBASE pour DOS) |
| 1–3 | 3 octets | Date de la dernière mise à jour ; formaté comme AAMMJJ |
| 4–7 | nombre 32 bits | Nombre d'enregistrements dans le fichier de base de données |
| 8–9 | nombre 16 bits | Nombre d'octets dans l'en-tête |
| 10–11 | nombre 16 bits | Nombre d'octets dans l'enregistrement |
| 12–13 | 2 octets | Réservé; remplir avec 0 |
| 14 | 1 octet | Drapeau signalant une transaction incomplète[note 1] |
| 15 | 1 octet | Indicateur de chiffrement[note 2] |
| 16–27 | 12 octets | Réservé à dBASE pour DOS dans un environnement multi-utilisateurs |
| 28 | 1 octet | Indicateur de fichier .mdx de production ; 1 s'il existe un fichier .mdx de production, 0 sinon |
| 29 | 1 octet | ID du pilote de langue |
| 30–31 | 2 octets | Réservé; remplir avec 0 |
| 32–n [note 3][note 4] | 32 octets chacun | tableau de descripteurs de champ (voir ci-dessous pour la disposition des descripteurs) |
| n + 1 | 1 octet | 0x0D comme terminateur de tableau de descripteur de champ |

- La fonction ISMARKEDO vérifie ce drapeau (BEGIN TRANSACTION le met à 1, END TRANSACTION et ROLLBACK le remettent à 0).
- Si ce drapeau est à 1, le message Base chiffrée apparaît.
- Le nombre maximum de champs est de 255.
- n signifie le dernier octet du tableau de descripteurs de champ.

### Tableau de descripteurs de champ
Disposition des descripteurs de champs dans dBASE :

| Octet | Sommaire | Signification |
---|---|---|
| 0–10 | 11 octets | Nom du champ en ASCII (zéro rempli) |
| 11 | 1 octet | Type de champ. Valeurs autorisées : C, D, F, L, M ou N (voir le tableau suivant pour les significations) |
| 12–15 | 4 octets | Réservé |
| 16 | 1 octet | Longueur de champ en binaire (maximum 254 (0xFE)). |
| 17 | 1 octet | Nombre décimal de champ en binaire |
| 18–19 | 2 octets | ID de la zone de travail |
| 20 | 1 octet | Exemple |
| 21–30 | 10 octets | Réservé |
| 31 | 1 octet | Indicateur de champ MDX de production ; 1 si le champ a une balise d'index dans le fichier MDX de production, 0 sinon |

### Enregistrements de la base de données
Chaque enregistrement commence par un indicateur de suppression (1 octet). Les champs sont enveloppés dans des enregistrements sans séparateurs de champs. Toutes les données de champ sont au format ASCII. Selon le type de champ, l'application impose des restrictions supplémentaires. Voici les types de champs dans dBase :

| Type de champ | Mnémonique | Ce qu'il accepte |
-------|-----|----|
| C | Caractère | N'importe quel texte ASCII (rempli d'espaces jusqu'à la longueur du champ) |
| D | Rendez-vous | Des chiffres et un caractère pour séparer le mois, le jour et l'année (stockés en interne sous forme de 8 chiffres au format AAAAMMJJ) |
| F | Virgule flottante | -, ., 0–9 (justifié à droite, rempli d'espaces) |
| L | Logique | Y, y, N, n, T, t, F, f ou ? (lorsqu'il n'est pas initialisé) |
| M | Mémo | Tout texte ASCII (stocké en interne sous forme de 10 chiffres représentant un numéro de bloc .dbt, justifié à droite, rempli d'espaces) |
| N | Numérique | -, ., 0–9 (justifié à droite, rempli d'espaces) |









## Références ##

* [.dbf - Wikipédia](https://en.wikipedia.org/wiki/.dbf)

