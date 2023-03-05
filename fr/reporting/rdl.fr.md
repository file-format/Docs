{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Fichier de langage de définition de rapport",
  "keywords" :[ "rdl", "langage de définition de rapport", "XmlTextWriter", "XSD", "élément RDL"],
  "description":"En savoir plus sur le format de fichier RDL qui est une représentation XML d'une définition de rapport SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Qu'est-ce qu'un fichier RDL ? ##

Le RDL (Report Definition Language) est une référence établie par Microsoft pour la définition des rapports. Un fichier RDL se compose d'un ou plusieurs éléments RDL. Alors qu'un élément RDL se compose de son type de données et de sa cardinalité. Un élément peut être simple ou complexe. L'élément simple n'a pas d'élément ou d'attribut enfant, alors qu'un élément complexe a des enfants et des attributs facultatifs.

## Définition de schéma XML RDL
Un fichier XML Schema Definition (XSD) valide le fichier RDL. Le schéma définit les règles d'emplacement des éléments RDL dans un fichier .rdl. Un élément RDL peut être simple ou complexe. Un élément simple n'a pas d'éléments ou d'attributs enfants et un élément complexe a des enfants et éventuellement des attributs.

## Création de RDL
Étant donné que RDL est de nature ouverte et extensible, de nombreuses applications et outils peuvent être créés pour générer des fichiers RDL basés sur son schéma XML. L'un des moyens les plus simples de créer RDL à partir d'une application consiste à utiliser les classes Microsoft .NET Framework de l'espace de noms **System.Xml** et de l'espace de noms System.Linq. En particulier, la classe **XmlTextWriter** peut être utilisée pour écrire du RDL. Vous pouvez générer une définition de rapport complète du début à la fin dans n'importe quelle application .NET Framework en utilisant **XmlTextWriter**. Les développeurs peuvent également ajouter des éléments de rapport personnalisés avec des propriétés personnalisées pour étendre le RDL.

## Types RDL
Le tableau suivant répertorie les types et attributs utilisés dans les éléments RDL.

|Type|Description|
---|---|
|Binaire |Une propriété avec une valeur binaire encodée en base 64.|
|Booléen| Une propriété avec true ou false comme valeur de l'objet. Sauf indication contraire, la valeur d'un objet booléen facultatif omis est False.|
|Date |Une propriété avec une valeur date ou datetime entièrement spécifiée au format de date ISO8601 : AAAA-MM-JJ[THH:MM[:SS[.S]]].|
|Enum |Une propriété avec une valeur de texte de chaîne qui doit faire partie d'une liste de valeurs désignées.|
|Float |Une propriété avec une valeur flottante. Un point (.) est utilisé comme séparateur décimal facultatif.|
|Entier |Une propriété avec une valeur entière (int32).|
|Langue |Une propriété avec une valeur de texte qui contient un code de langue et de culture, comme « en-us » pour l'anglais américain. La valeur doit être soit une langue spécifique, soit une langue neutre pour laquelle une langue par défaut est définie dans Microsoft .NET Framework.|
|Nom |Une propriété avec une valeur de texte de chaîne. Les noms doivent être uniques dans l'espace de noms de l'élément. S'il n'est pas spécifié, l'espace de noms d'un élément est l'objet contenant le plus interne qui a un nom.|
|NormalizedString |Une propriété avec une valeur de texte de chaîne qui a été normalisée.|
|Taille |Un élément de taille doit contenir un nombre (avec un point utilisé comme séparateur décimal facultatif). Le nombre doit être suivi d'un indicateur pour une unité de longueur CSS telle que cm, mm, in, pt ou pc. Un espace entre le numéro et l'indicatif est facultatif. Pour plus d'informations sur les indicateurs de taille, consultez CSS Values and Units Reference.Dans RDL, la valeur maximale de Size est de 160 pouces. La taille minimale est de 0 pouces.|
|Chaîne |Une propriété avec une valeur de texte de chaîne.|
|UnsignedInt |Une propriété avec une valeur entière non signée (uint32).|
|Variante |Une propriété avec n'importe quel type XML simple.|

## Types de données RDL
Dans RDL, l'énumération DataType définit le type de données d'un attribut, d'une expression ou d'un paramètre. Le tableau suivant montre comment les types de données CLR correspondent aux types de données RDL.

|Type(s) CLR |Type de données correspondant|
---|---|
|Booléen| Booléen|
|DateHeure, DécalageDateHeure |DateHeure|
|Int16, Int32, UInt16, Octet, SByte |Entier|
|Simple, Double |Flottant|
|Chaîne, caractère, GUID, durée |Chaîne|


## Références ##

- [Langage de définition de rapport (Wikipédia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Langage de définition de rapport (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

