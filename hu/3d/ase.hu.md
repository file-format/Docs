{
  "date" : "2021-01-22",
  "keywords" :[ "ASE", "fájl", "formátum", "fájl típusa", "kiterjesztés", "mi az ASE fájl?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az ASE fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak ASE-fájlokat.",
  "title" :"ASE - Autodesk ASCII Scene Export File",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Mi az ASE fájl?

Az .ase kiterjesztésű fájl egy Autodesk ASCII Scene Export fájlformátum, amely egy jelenet ASCII-ábrázolása, amely 2D vagy 3D információkat tartalmaz, miközben jelenetadatokat exportál az Autodesk használatával. Az Autodesk lehetőséget biztosít jelenet-összetevők bevonására a jelenetadatok exportálása során. Felveheti a háló definícióját a csúcs- és arcinformációkkal együtt, az anyagleírást, az objektumok animációs adatait, a teljes háló definíciót minden n képkockához, a kamerák és lámpák animációs adatait, valamint az IK illesztési beállításokat.

## ASE fájlformátum – További információ

Az ASE fájlok ASCII formátumban tárolt szövegfájlok, amelyek bármely szövegszerkesztőben megnyithatók. Az ASE-fájlok az Autodesk által biztosított alábbi típusú információkat tartalmazhatják.

### Kimeneti beállítások

* "Mesh Definition" - Exportálja az egyes hálók definícióit, beleértve a geometriai objektumok csúcs- és felületinformációit. Ezen túlmenően, ha ezt bekapcsolja, akkor az alábbiakban ismertetett Hálóbeállítások csoportdobozban lévő elemek is engedélyezhetők.
* "Anyagok" - Tartalmazza az anyag leírását. Ha egy anyag nincs hozzárendelve egy objektumhoz, a rendszer exportálja a drótváz színét. Az anyagfa minden szintje benne van, így ez sok szöveget eredményezhet.
* `Animációs kulcsok átalakítása` – Tartalmazza az objektumok átalakítási animációs adatait. Ha az objektum célkamera vagy reflektorfény, ez tartalmazza a célanimációs adatokat.
* "Animált háló" - Minden n képkocka teljes hálódefinícióját exportálja. A frekvenciát a Controller Output spinner határozza meg (lásd alább). Minden blokk ugyanazokat az információkat tartalmazza, amelyeket az alábbiakban ismertetett Hálóbeállítások csoportdobozban megadott. Ennek bekapcsolása hatalmas fájlt eredményezhet, még kis jeleneteknél is.
* `Animált kamera/fénybeállítások` – Exportálja a kamerákhoz és a fényekhez tartozó animációs adatokat, például színt, intenzitást, kiesést, térképeltolódást és így tovább. n képkockánként egy blokkot ad ki a Controller Output spinner által meghatározottak szerint.
* `Inverz kinematikai illesztések` - Exportálja az IK illesztési beállításokat a Hierarchia ágban.

### Objektumtípusok

Az itt található elemek segítségével megadhatja, hogy az objektum melyik kategóriáját kívánja szerepeltetni a kimenetben. Használhat geometriai objektumokat, formákat, kamerákat, fényeket és segédobjektumokat.

* Geometrikus
* Formák
* Kamerák
* Lámpák
* Segítők

### Háló opciók

* "Mesh Normals" - Exportálja az arc- és csúcsnormálokat. Először az arc normálja szerepel, majd az arcot támasztó három csúcs normálértéke. Ennek bekapcsolása sokkal nagyobb fájlt eredményez.
* `Mapping Coordinates` - A leképezési csúcsok és lapok listáját exportálja a 3ds Max Software Development Kitben leírt TVert és TVFace struktúrák szerint. Ha egy objektum arcleképezést használ, akkor a rendszer egy arctérkép-listát exportál, amely minden egyes arc UVW-koordinátáit tartalmazza.
* "Csúcsszínek" - Csúcsszínek exportálása.

### Vezérlő kimenet

* "Kulcsok használata" - Kulcsértékek exportálása. Ha a vezérlő nem használ kulcsokat, akkor a Force Sample módszert használja. Transzformációs vezérlők esetén a Kulcsok használata opció csak akkor működik, ha az összes transzformációs vezérlő Lineáris/TCB vagy Bezier. Ha az egyik transzformációs sáv más típusú vezérlőt használ, akkor a Force Sample metódus minden transzformációs sávhoz használatos.
* `Force Samples` – Mintavételezési vezérlőértékek a Frames per Sample Controllerben megadott gyakoriság alapján.

## Hivatkozások

* [Autodesk – Exportálás ASCII-be](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

