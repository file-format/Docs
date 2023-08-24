{
  "date" : "2019-10-11",
  "keywords" :[ "odg fájl", "odg fájl formátum", "mi az odg fájl", "fájl", "odg példa", "odg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG fájlformátum",
  "description":"További információ az ODG fájlformátumról és az API-król, amelyek ODG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ODG fájl?

Az ODG fájlformátumot az Apache OpenOffice Draw alkalmazása használja a rajzelemek vektorképként történő tárolására. Követi az Advancement of Structural Information Standards (OASIS) XML-alapú fájlformátum-specifikációit. Az ODG a rajzokat vektorképként ábrázolja pontok, vonalak és görbék segítségével. Az OpenOffice mellett a LibreOffice és más alkalmazások is támogatják az ODG fájlformátumokkal való munkát. Az OpenOffice által támogatott egyéb formátumok közé tartozik például az [ODT](/hu/word-processing/odt/), az ODF, az [ODP](/hu/presentation/odp/) és az [ODS](/hu/spreadsheet/ods/).


## ODG fájlformátum specifikációi

Az ODG fájlformátum az OpenDocument formátumon alapul, amely strukturált XML dokumentumformátum, jól meghatározott sémával.
Az OpenDocument formátum minden egyes szerkezeti összetevőjét egy olyan elem képviseli, amelyhez társított attribútumok tartoznak. Az XML alapú struktúra minden dokumentumtípusnál közös, például szöveges dokumentumban, táblázatban vagy rajzfájlban. Egy dokumentum különböző stílusokat tartalmazhat. Az OpenDocument fájlszerkezet a következő elemekből áll.
* Dokumentumgyökér
* Dokumentum metaadatai
* Testelem és dokumentumtípusok
* Alkalmazás beállítások
* Szkriptek
* Font Face nyilatkozatok
* Stílusok
* Oldalstílusok és elrendezések

## Dokumentumgyökerek ##

A dokumentum gyökéreleme a teljes dokumentumot tartalmazza, és egy OpenDocument formátumú fájl elsődleges eleme. Ugyanazok a típusú dokumentum gyökérelemek alkalmazhatók minden típusú dokumentumhoz, például szöveghez, dokumentumokhoz, táblázatokhoz és rajzdokumentumokhoz.

### Gyökérelemek ###
Egyetlen XML dokumentumot a saját gyökéreleme képvisel. Az öt különböző támogatott gyökérelem a következő.

`<office:document>` - Teljes irodai dokumentum egyetlen XML dokumentumban.
`<office:document-content>` - Dokumentumtartalom és a tartalomban használt automatikus stílusok.
`<office:document-styles>` - A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
`<office:document-meta>` - A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
`<office:document-settings>` - Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

### ODG dokumentum metaadatai ###
Az OpenDocument tartalmazza az összes metaadat elemet a \<office:meta> elem. A dokumentumra vonatkozó általános információk a dokumentum elején találhatók, és az alkalmazások ugyanazon elemek több példányát is frissíthetik.

### Testelemek és dokumentumtípusok ###
A dokumentumtörzs a dokumentumtípus elem segítségével jelzi a dokumentumban található tartalom típusát. Ezek a dokumentumtípusok a következők:
* szöveges dokumentumok
* rajz dokumentumok
* bemutató dokumentumok
* táblázatos dokumentumok
* diagram dokumentumok
* képes dokumentumok

### Alkalmazás beállítások ###
Az irodai alkalmazások beállításai különböző beállításokat képviselnek, amelyek a dokumentum konfigurációjához vagy a dokumentum vizuális megjelenéséhez kapcsolódnak. Minden kategóriát egy  jelöl `<config:config-item-set>`. Példák az ilyen beállítási kategóriákra:
* Dokumentumbeállítások pl. alapértelmezett nyomtató
* Beállítások megtekintése pl. nagyítási szint

### Szkriptek ###
Gyakori, hogy egy dokumentum több szkriptet is tartalmaz. Az OpenDocument fájlban minden szkriptet egy jelöl `<office:script>` elemet. Ezeket a szkriptelemeket egyetlen tartalmazza `<office:scripts>` elemet. A szkriptek nem frissítik a dokumentumot a dokumentum betöltése közben.
### Betűtípus-nyilatkozatok ###

A betűtípus deklarációja információkat tartalmaz a dokumentum szerzője által használt betűtípusokról. Ez az információ segít megtalálni ezeket a betűtípusokat más rendszereken.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stílusok ###
Az OpenDocument formátum a következő stílusokat támogatja.

"Közös stílusok" – Az ilyen stílusok XML-reprezentációit stílusoknak nevezzük
"Automatikus stílusok" – Formázási tulajdonságokat tartalmaz, amelyek a dokumentum felhasználói felület nézetében egy objektumhoz, például egy bekezdéshez vannak hozzárendelve.
"Mater Styles" - egy általános stílus, amely formázási információkat és további tartalmat tartalmaz, amely a stílus alkalmazásakor a dokumentumtartalommal együtt jelenik meg. A mesterstílusra példák a mesteroldalak.

## Referenciák ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

