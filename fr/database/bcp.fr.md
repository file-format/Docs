{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "extension", "fichier", "format de fichier", "Type de fichier de base de données", "Format de fichier de base de données", "Fichiers de base de données" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier BCP et les API qui peuvent créer et ouvrir des fichiers BCP.",
  "title" :"BCP - Format de fichier de copie en bloc SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Qu'est-ce qu'un fichier BCP ?

BCP (Bulk Copy Format) est le format de données techniques de Microsoft SQL Server qui définit les structures de données pour stocker différentes valeurs de type de données de base de données pour l'importation/exportation. Le format définit entièrement l'interprétation de chaque colonne de données afin que l'ensemble de valeurs spécifié dans le fichier de données puisse être lu. L'utilitaire [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) utilise le format de fichier BCP pour lire données d'un tel fichier et de l'identifier.


## Format de fichier BCP

Le fichier au format BCP est un document XML qui définit l'ordre des colonnes, le nom et le type de données. Il permet aux utilisateurs d'importer/exporter de grandes quantités de données à partir d'un fichier de données en spécifiant ces champs. Ceci est utile pour l'importation en bloc de valeurs de données à partir de fichiers de données. Le nombre et l'ordre des champs de données dans le fichier de données peuvent être différents de ceux des colonnes de la table de destination. C'est alors que le fichier de format de données BCP vient en aide en spécifiant l'ordre et le type des colonnes pour importer les données.

La structure du fichier de format est représentée dans le format suivant.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Types de données BCP

|Type de données|Plage|Représentation|
---|---|---|
|BigInt|-263 (-9 223 372 036 854 775 808) à 263-1 (9 223 372 036 854 775 807)|`BigInt = ["-"]1*19DIGIT`|
|Binaire|1 à 8000 octets|Format de chaîne Unicode codé en hexadécimal `Binaire = 32000OCTET`|
|Bit|0 ou 1|chaîne Unicode simple Bit = "0" / "1"|
|Char|1 à 8000|Format de chaîne Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET avec n = 4 x (2 147 483 647)|
|Date|0001-01-01 à 9999-12-31|Format de chaîne AAAA-MM-JJ|
|DateHeure|1753-01-01 00:00:00.000 à 9999-12-31 23:59:59.997| Format de chaîne Unicode AAAA-MM-JJ hh:mm:ss[.nnn]|
|DateHeure2|0001-01-01 00:00:00.0000000 à 9999-12-31 23:59:59.9999999.| Format de chaîne Unicode AAAA-MM-JJ hh:mm:ss[.nnnnnnn]|
|DateTimeOffset|0001-01-01 00:00:00.0000000 à 9999-12-31 23:59:59.9999999 dans le fuseau horaire UTC (Coordinated Universal Time)| Unicode AAAA-MM-JJ hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] format de chaîne|
|Decimal|-1038 + 1 à 1038 – 1|Format de chaîne Unicode `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Flottant|-1.79E+308 à -2.23E-308 ; 0 ; de 2.23E-308 à 1.79E+308|Format de chaîne Unicode|
|Image|séquence d'octets allant de 0 à 231 – 1 (2 147 483 647)|format de chaîne Unicode codé en hexadécimal|
|Int|-231 (-2 147 483 648) à 231 – 1 (2 147 483 647)|Format de chaîne Unicode|

## Références

* [Format BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

