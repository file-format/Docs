{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extension", "fichier sav", "format de fichier sav", "Type de fichier de base de données", "Format de fichier de base de données", "qu'est-ce qu'un fichier sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier SAV et les API qui peuvent créer et ouvrir des fichiers SAV.",
  "title" :"SAV - Fichier de données SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Qu'est-ce qu'un fichier SAV ?
Le fichier SAV est un fichier de données créé par le progiciel statistique pour les sciences sociales (SPSS), qui est une application largement utilisée par les chercheurs de marché, les chercheurs en santé, les sociétés d'enquête, le gouvernement, les chercheurs en éducation, les organisations de marketing, les mineurs de données pour l'analyse statistique. Le SAV enregistré dans un format binaire propriétaire et se compose d'un ensemble de données ainsi que d'un dictionnaire qui représente l'ensemble de données, enregistre les données en lignes et en colonnes.

## Format de fichier SAV
Le format de fichier SAV est devenu relativement stable, mais on ne peut pas dire qu'il soit statique. La compatibilité ascendante et descendante est disponible en option si nécessaire, mais n'est pas maintenue correctement. Les données d'un fichier SAV sont classées dans les sections suivantes :

### En-tête de fichier
Il se compose de 176 octets. Les 4 premiers octets indiquent la chaîne **$FL2** ou **$FL3** dans le codage de caractères utilisé pour le fichier. Les trois derniers octets indiquent que les données du fichier sont compressées à l'aide de **ZLIB**. La chaîne suivante de 60 octets commence **@(#) SPSS DATA FILE** et détermine également le système d'exploitation et la version SPSS qui ont créé le fichier. L'en-tête continue ensuite avec des champs à six chiffres, contenant le nombre de variables par observation et un code numérique pour la compression, et se termine par des données textuelles indiquant la date et l'heure de création et une étiquette de fichier.
### Enregistrements de description de variable
L'enregistrement contient une séquence fixe de champs, classifiant le type et le nom de la variable ainsi que les informations de formatage utilisées par SPSS. Chaque enregistrement de variable peut éventuellement contenir une étiquette de variable de 120 caractères maximum et jusqu'à trois spécifications de valeur manquante.
### Étiquettes de valeur
Les étiquettes de valeur sont facultatives et stockées dans des paires d'enregistrements avec des étiquettes entières 3 et 4. Le premier enregistrement qui est l'étiquette 3 a une séquence de paires de champs, chaque paire contenant une valeur et l'étiquette de valeur associée. Le deuxième enregistrement, qui est la balise 4, représente les variables auxquelles s'applique l'ensemble de valeurs/étiquettes.
### Documents
Enregistrements uniques ou multiples avec étiquette entière 6. Documentation facultative. contient des lignes de 80 caractères.
### Enregistrements d'extensions
Enregistrements uniques ou multiples avec une balise entière 7. Les enregistrements d'extension fournissent des informations qui peuvent être ignorées en toute sécurité, mais conservées, dans de nombreuses situations, permettent aux fichiers écrits par un logiciel plus récent de préserver la compatibilité descendante. Les enregistrements d'extension ont des balises de sous-type entier.
### Terminateur de dictionnaire
N'enregistrer qu'avec l'étiquette entière 999. Il sépare le dictionnaire des observations de données.
### Observations des données
Il est considéré que les données sont dans l'ordre d'observation, par exemple toutes les valeurs variables pour la première observation, suivies de toutes les valeurs pour la deuxième observation, etc. Le format de l'enregistrement de données varie en fonction du code de compression dans l'enregistrement d'en-tête de fichier. La partie données d'un fichier .sav peut être décompressée :
- **code 0** : compressé par bytecode
- **code 1** : compressé à l'aide de la compression ZLIB
 







## Références ##

* [Famille de formats de fichiers de données système SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

