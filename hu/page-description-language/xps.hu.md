{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML Paper Specifications", "File", "Extension", "File Format", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Oldalelrendezés fájlformátum",
  "description":"További információ az XPS fájlformátumról és az XPS-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az XPS fájl? ##

Az XPS-fájlok olyan oldalelrendezési fájlok, amelyek a Microsoft által létrehozott XML-papírspecifikációkon alapulnak. Az EMF fájlformátum helyettesítésére fejlesztették ki, és hasonló a [PDF](/hu/pdf/) fájlformátumhoz, de XML-t használ a dokumentumok elrendezésében, megjelenésében és nyomtatási információiban. Valójában indokoltabb azt állítani, hogy az XPS egy kísérlet a PDF-re, de sok okból nem tudott elég népszerűséget szerezni a PDF tulajdonában. A Microsoft alapértelmezés szerint XPS Document Writert biztosít a Windows 7-től kezdve az XPS-fájlok létrehozásához. Az XPS-fájlok a „Microsoft XPS Document Writer” nyomtatóként történő kiválasztásával hozhatók létre a dokumentum nyomtatása közben.

Az XPS-megtekintők a Windows Vista, a Windows 7, a Windows 8 és az Internet Explorer 6 vagy újabb részeként kerülnek beépítésre. Az XPS-fájlok csak olvashatóvá válnak a létrehozásuk után. Ez növeli a felhasználó bizalmát az XPS-ként küldött fogadott dokumentumokban a dokumentum hitelessége miatt. Egy XPS-dokumentum egy vagy több oldalt tartalmazhat az eredeti dokumentumból konvertálva.

## Rövid története ##

A Microsoft benyújtotta az XPS-specifikációt az Ecma International-nek. 2007 júniusában létrehozták az Ecma Technical Committee 46-ot (TC46), hogy az OpenXPS papírspecifikációkon alapuló szabványt dolgozzon ki. Az Ecma International 2009 júniusában, a 97. közgyűlésen jóváhagyta az Ecma szabványt (ECMA-388) [XPS-specifikáció](http://www.ecma-international.org/publications/standards/Ecma-388.htm).

## XPS fájlformátum ##

Az XPS formátum XML jelölésekből áll, amelyek meghatározzák a dokumentum összetételét és az egyes oldalak vizuális megjelenését, valamint a dokumentum megjelenítésére vagy nyomtatására vonatkozó renderelési szabályokat. Megőrzi az összes információt, hogy újra létrehozhasson egy dokumentumot bármely rendszeren, ami függetlenné teszi az adott rendszeren rendelkezésre álló erőforrásoktól. A formátum lényegében egy ZIP-archívum, és ha átnevezi a fájl kiterjesztését ZIP-re, látni fogja a dokumentumadatokat tartalmazó fájlokat. Ezek a dokumentumok a következőket tartalmazzák:

* dokumentumoldal fájlok (.fpage) – Dokumentumtartalom- és dokumentumformátum-beállításokat tartalmaz. Az XPS-dokumentum minden oldalán egy FPAGE fájl található.
* dokumentumbeállítási fájl (.fdoc) – Az XPS archívumban található beállításokat tárolja.
* dokumentumtöredékfájlok (.frag) – Meghatározza a tényleges XPS-fájl beállításait, és a dokumentum minden oldalának saját .frag fájlja van.

{{< figure src="../XPS-1.png" alt="XPS fájlformátum" >}}

Ezek a fájlok megőrzik a dokumentum tartalmát oly módon, hogy ha például valakinek nem ugyanazok a betűtípusok vannak telepítve a gépére, az XPS megjelenítő továbbra is az eredeti betűtípusokat jeleníti meg. Ez azt jelenti, hogy minden egyes XML-jelölőfájlt tartalmaznia kell:

* Oldal
* Szöveg
* Beágyazott betűtípusok
* Raszteres képek
* 2D vektorgrafika
* Digitális jogkezelés

Az XPS-dokumentum formátuma részek és kapcsolatok jól meghatározott készletét tartalmazza, amelyek mindegyike egy adott célt tölt be a dokumentumban. A formátum a csomag szolgáltatásait is kiterjeszti, beleértve a digitális aláírásokat, bélyegképeket és interleavingeket.

Egy tipikus XPS-dokumentum a következőképpen néz ki, és az XPS-fájlformátum [specifikációi](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf) fényében elemezhető.

{{< figure src="../XPS-2.png" alt="XPS fájlformátum" >}}


## Referenciák ##

* [XPS fájlformátum specifikációi](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS – a Wikipedia által](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

