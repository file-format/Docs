{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az OTS-fájlformátumról és az API-król, amelyek OTS-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"OTS – OpenDocument Spreadsheet Template File Format",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Mi az az OTS fájl?

Az .ots kiterjesztésű fájl egy OpenDocument Spreadsheet Template fájl, amely az Apache OpenOffice-ban található Calc alkalmazásszoftverrel jön létre. A Calc szoftver hasonló a Microsoft Office-ban elérhető Excelhez. Az OTS fájlformátumot olyan sablonok létrehozására használják, amelyek előre meghatározott beállításokat tartalmaznak a stílusokhoz, betűtípusokhoz, adatokhoz, táblázatelrendezéshez és formázáshoz. Az OTF-fájlok "mime-type application/vnd.oasis.opendocument.spreadsheet-template"-vel rendelkeznek. Ezek a sablonfájlok kiindulási pontként használhatók [ODS fájlformátumban](/hu/spreadsheet/ods/) mentett tényleges adatfájlok létrehozásához és mentéséhez. Az OTS-fájlok olyan alkalmazásokkal használhatók, mint az OpenOffice és a LibreOffice.

## OTS fájlformátum

Az OTS-fájlok az OASIS OpenDocument XML-alapú fájlformátumában kerülnek mentésre, amely több aldokumentum gyűjteményéből áll, egy csomaggal [ZIP](/hu/compression/zip/) archívumként. Minden zip-archívum a teljes dokumentum egy részét, minden aldokumentum pedig a dokumentum egy-egy aspektusát tárolja. Például egy aldokumentum tartalmazza a stílusinformációkat, egy másik pedig a dokumentum tartalmát. Egy tipikus ODF dokumentum a következő összetevőket tartalmazza:

### OTS Content.xml

A content.xml fájl tartalmazza a dokumentum tényleges tartalmát. Ez azonban nem tartalmazza a bináris adatokat, például a képeket.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml OTS fájlformátum

A styles.xml fájl stílusinformációkat tartalmaz, és gyakran használják formázáshoz és elrendezéshez. A stílustípusok a következők:

* Bekezdésstílusok
* Oldalstílusok
* Karakterstílusok
* Keret stílusok
* Stílusok listája

### Meta.xml

A meta.xml fájl információkat tartalmaz a fájl metaadatairól, például Szerző, Utolsó módosítás dátuma stb.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

A "settings.xml" fájl dokumentum szintű beállításokat tartalmaz, például nagyítási tényezőt és kurzorpozíciót.

## Referenciák ##

* [OpenDocument 1.2 specifikáció](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

