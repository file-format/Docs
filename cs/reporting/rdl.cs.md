{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Report Definition Language File",
  "keywords" :[ "rdl", "jazyk definice sestavy", "XmlTextWriter", "XSD", "prvek RDL"],
  "description":"Další informace o formátu souboru RDL, což je reprezentace XML definice sestavy SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Co je soubor RDL? ##

RDL (Report Definition Language) je benchmark stanovený společností Microsoft pro definování sestav. Soubor RDL se skládá z jednoho nebo více prvků RDL. Zatímco prvek RDL se skládá z jeho datového typu a mohutnosti. Prvek může být jednoduchý nebo složitý. Jednoduchý prvek nemá žádný podřízený prvek nebo atributy, zatímco složitý prvek má potomky a volitelné atributy.

## Definice schématu RDL XML
Soubor XML Schema Definition (XSD) ověřuje soubor RDL. Schéma definuje pravidla pro umístění prvků RDL v souboru .rdl. Prvek RDL může být jednoduchý nebo složitý. Jednoduchý prvek nemá podřízené prvky nebo atributy a složitý prvek má potomky a volitelně atributy.

## Vytváření RDL
Vzhledem k tomu, že RDL je ve své podstatě otevřený a rozšiřitelný, lze vytvořit mnoho aplikací a nástrojů, které generují soubory RDL na základě schématu XML. Jedním z nejjednodušších způsobů vytvoření RDL z aplikace je použití tříd Microsoft .NET Framework jmenného prostoru **System.Xml** a jmenného prostoru System.Linq. K zápisu RDL lze použít zejména třídu **XmlTextWriter**. Pomocí **XmlTextWriter** můžete vygenerovat úplnou definici sestavy od začátku do konce v jakékoli aplikaci .NET Framework. Vývojáři mohou také přidat vlastní položky sestavy s vlastními vlastnostmi pro rozšíření RDL.

## Typy RDL
Následující tabulka uvádí typy a atributy používané v prvcích RDL.

|Typ|Popis|
---|---|
|Binární |Vlastnost s binární hodnotou zakódovanou na bázi 64.|
|Boolean| Vlastnost s true nebo false jako hodnotou objektu. Pokud není uvedeno jinak, hodnota vynechaného volitelného booleovského objektu je False.|
|Datum |Vlastnost s plně zadaným datem nebo hodnotou data a času zadanou ve formátu data ISO8601: RRRR-MM-DD[THH:MM[:SS[.S]]].|
|Výčet |Vlastnost s textovou hodnotou řetězce, která musí být jednou ze seznamu určených hodnot.|
|Float |Vlastnost s plovoucí hodnotou. Tečka (.) se používá jako volitelný oddělovač desetinných míst.|
|Celé číslo |Vlastnost s celočíselnou (int32) hodnotou.|
|Jazyk |Vlastnost s textovou hodnotou, která obsahuje kód jazyka a kultury, například "en-us" pro americkou angličtinu. Hodnota musí být buď konkrétní jazyk, nebo neutrální jazyk, pro který je v rozhraní Microsoft .NET Framework definován výchozí jazyk.|
|Jméno |Vlastnost s textovou hodnotou řetězce. Názvy musí být jedinečné v rámci jmenného prostoru položky. Pokud není zadán, jmenný prostor pro položku je nejvnitřnější obsahující objekt, který má jméno.|
|NormalizedString |Vlastnost s textovou hodnotou řetězce, která byla normalizována.|
|Velikost |Prvek velikosti musí obsahovat číslo (se znakem tečky použitým jako volitelný oddělovač desetinných míst). Za číslem musí následovat označení jednotky délky CSS, jako je cm, mm, in, pt nebo pc. Mezera mezi číslem a označením je volitelná. Další informace o označovačích velikosti naleznete v tématu CSS Values and Units Reference.V RDL je maximální hodnota pro Size 160 in. Minimální velikost je 0 in.|
|String |Vlastnost s textovou hodnotou řetězce.|
|UnsignedInt |Vlastnost s hodnotou celého čísla bez znaménka (uint32).|
|Varianta |Vlastnost s libovolným jednoduchým typem XML.|

## Datové typy RDL
V RDL definuje DataType Enumeration datový typ atributu, výrazu nebo parametru. Následující tabulka ukazuje, jak datové typy CLR odpovídají datovým typům RDL.

|Typ(y) CLR |Odpovídající typ dat|
---|---|
|Boolean| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Celé číslo|
|Jednoduchý, dvojitý |Plovákový|
|Řetězec, znak, GUID, časový rozsah |řetězec|


## Reference ##

– [Jazyk definice přehledu (Wikipedie)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

