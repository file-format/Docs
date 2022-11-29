{
  "date" : "2020-08-20",
  "keywords" :[ "ttf-fil", "ttf-filformat", "vad är en ttf-fil", "fil", "ttf-exempel", "ttf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType Font File Format",
  "description":"TrueType-teckensnitt (TTF) är baserade på tekniska specifikationer för digitala teckensnitt som ursprungligen designades av Apple, Inc. Både Apple och Microsoft använde TTF på Mac- och Windows-operativsystem.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Vad är TTF fil?

En fil med filtillägget .ttf representerar teckensnittsfiler baserade på TrueType-specifikationens teckensnittsteknik. Det designades och lanserades från början av Apple Computer, Inc för Mac OS och antogs senare av Microsoft för Windows OS. TrueType-teckensnitt ger visning av högsta kvalitet på datorskärmar och skrivare utan något beroende av upplösning. Alla moderna applikationer som använder typsnitt kan arbeta med TTF-filer. TTF-teckensnittsfiler är fritt tillgängliga över internet och kan även konverteras till andra typsnittsfilformat som OTF och WOFF.

## Kortfattad bakgrund

TTF-teckensnittsformatet designades av Apply Computer, Inc på 1980-talet för MacOS och syftade till att lösa vissa tekniska begränsningar av Adobes typ 1-format. Apple inkluderade stöd för TrueType-teckensnitt i Mac 1991. Designmålet bakom TTF-teckensnitt var effektivitet i lagring och bearbetning samt utbyggbarhet. Baserat på denna utökningsmöjlighet kan befintliga teckensnitt konverteras till TrueType-format.

Microsoft använde först TrueType-teckensnitten i Windows 3.1 i april 1992 efter att Apple gick med på att licensiera TrueType till Microsoft. Det förbättrade rastreringsmekanismen och förbättrade dess effektivitet och prestanda.

## True Type filformatspecifikationer

En TrueType-teckensnittsfil är en binär fil som består av en sekvens av sammanlänkade tabeller. Varje tabell är en sekvens av ord och har ett namn som kallas "Tag". Varje tagg är av datatypen uint32 och består av fyra tecken. Den första tabellen i filen är teckensnittskatalog som ger tillgång till andra tabeller i teckensnittsfilen. Teckensnittsdata finns i andra tabeller följt efter teckensnittskatalogtabellen. Eftersom varje tabell är tillgänglig med sin tagg, kan tabellerna visas i valfri ordning i filen.

De obligatoriska tabellerna och deras taggnamn visas i följande tabell.

|**Tagg**|**Tabell**|
---|---|
|'cmap'| tecken till glyph mappning|
|'glyf'| glyph data|
|'huvud'| teckensnittshuvud|
|'hhea'| horisontell rubrik|
|'hmtx'| horisontella mått|
|'loca'| indexera till plats|
|'maxp'| maximal profil|
|'namn'| namnge|
|'post'| PostScript|

### Datatyper
TrueType-teckensnitt använder standard heltal och ytterligare datatyper som anges i följande tabell.

|**Datatyp** | **Beskrivning** |
---|---|
|shortFrac| 16-bitars signerad bråkdel|
|Fastad| 16,16-bitars signerat fastpunktsnummer|
|FWord| 16-bitars heltal med tecken som beskriver en kvantitet i FUnits, det minsta mätbara avståndet i em space.|
|uFWord| 16-bitars heltal utan tecken som beskriver en kvantitet i FUnits, det minsta mätbara avståndet i em space.|
|F2Punkt14| 16-bitars signerat fast nummer med de låga 14 bitarna som representerar bråk.|
|longDateTime| Det långa interna formatet för ett datum i sekunder sedan 12:00 midnatt, 1 januari 1904. Det representeras som ett signerat 64-bitars heltal.|

### Teckensnittskatalog

Den första tabellen i TrueType-teckensnittet är teckensnittskatalogen som ger åtkomst till den information som krävs för att komma åt data i andra tabeller. Den består vidare av:

* `Offset subtable` - håller register över tabellerna i typsnittet och tillhandahåller offsetinformation för att komma åt varje tabell i katalogen
* `Tabell Directory` - Innehåller poster för varje tabell i typsnittet

#### Offset SubTable
Offset-undertabellen visas nedan.

|**Typ**|**Namn**|**Beskrivning**|
---|---|---|
|uint32| scaler typ| En tagg för att indikera den OFA-skalare som ska användas för att rastrera detta teckensnitt; se anteckningen om scaler-typen nedan för mer information.|
|uint16| numTables| antal bord|
|uint16| sökintervall| (maximal potens av 2 <= numTables)*16|
|uint16| entrySelector| log2(maximal potens av 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Tabellkatalog
Tabellkatalogen kommer direkt efter offset-undertabellen. Dess struktur är som visas i följande tabell.

|**Typ**|**Namn**|**Beskrivning**|
---|---|---|
|uint32| tagg| 4-byte identifierare|
|uint32| kontrollsumma| kontrollsumma för denna tabell|
|uint32| offset| offset från början av sfnt|
|uint32| längd| längden på denna tabell i byte (faktisk längd inte vadderad längd)|

Varje tabell i en teckensnittsfil måste ha sin egen tabellkatalogpost. Poster i en tabell måste sorteras i stigande ordning efter tagg.


## Referenser
* [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType-översikt](https://docs.microsoft.com/en-us/typography/truetype/)

