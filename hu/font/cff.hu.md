{
  "date" : "2020-08-20",
  "keywords" :[ "cff fájl", "cff fájlformátum", "mi az a cff fájl", "fájl", "cff példa", "cff fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Compact Font File Format",
  "description":"További információ a CFF-fájlformátumról és a CFF-fájlok létrehozásához és megnyitásához szükséges API-król.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Mi az a CFF fájl?

A .cff kiterjesztésű fájl kompakt betűformátum, és PostScript Type 1 vagy CIDFont néven is ismert. A CFF tárolóként működik, ahol több betűtípust tárolhat egyetlen FontSet néven ismert egységben. A CFF-betűtípusok kialakítása lehetővé teszi a PostScript nyelvi kód beágyazását, amely további rugalmasságot és bővíthetőséget tesz lehetővé a formátumban a nyomtatókörnyezetekkel való használatra. A CFF-betűkészlet-fájlok megnyithatók és konvertálhatók olyan API-k használatával, mint például az [Aspose.Font](https://products.aspose.com/font).

## CFF fájlformátum

A CFF fájlok olyan bináris fájlok, amelyek strukturált adatelrendezést, meghatározott adattípusokat, fejlécet, karakterjel-szervezést és táblázatszótárakat tartalmaznak. Ezekről további részletek a [kompakt betűtípus-specifikációk](https://docs.microsoft.com/en-us/typography/opentype/spec/cff) részben találhatók.

### Adatelrendezés
A CFF fájlformátum adatelrendezése az alábbiak szerint látható.

|Bejegyzés|Megjegyzések|
---|---|
|Fejléc|–|
|NévINDEX|–|
|Legfelső DICT INDEX|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Kódolások–Karakterkészletek|–|
|FDSelect|Csak CIDFonts|
|CharStrings INDEX|betűtípusonként|
|Font DICT INDEX|betűtípusonként, csak CIDFonts|
|Privát DICT|betűtípusonként|
|Helyi előfizetési INDEX|betűtípusonként vagy privát DICT-ként CIDFonts-hoz|
|Szerzői jogi és védjegyekkel kapcsolatos megjegyzések|–|

### Adattípusok

A CFF adattípusok a következő táblázatban láthatók.

|Név|Tartomány|Leírás|
---|---|---|
|Card8|0 –255|1 bájtos előjel nélküli szám|
|16. kártya|0 – 65535|2 bájtos előjel nélküli szám|
|Eltolás|változó|1, 2, 3 vagy 4 bájtos eltolás (az OffSize mező határozza meg)|
|OffSize|1–4|1 bájtos előjel nélküli szám határozza meg az Eltolás mező vagy mezők méretét|
|SID|0 – 64999|2 bájtos karakterlánc-azonosító|

### Fejléc

A bináris adat a következő táblázatban látható formátumú fejléccel kezdődik.

|Típus|Név|Leírás|
---|---|---|
|Card8|major|A fő verzió formázása (1-től kezdődően)|
|Card8|minor|Format minor verzió (0-tól kezdődően)|
|Kártya8|hdrSize| Fejléc mérete (byte)|
|OffSize|offSize|Abszolút eltolás (0) méret|

## Hivatkozások

* [Compact Font Format Table](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF fájlformátum](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 diagramkészlet](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

