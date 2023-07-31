{
  "date" : "2019-10-11",
  "keywords" :[ "vssx fájl", "vssx fájlformátum", "mi az a vssx fájl", "fájl", "vssx példa", "vssx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Visio Stencil File Format",
  "description":"További információ a VSSX fájlformátumról és az API-król, amelyek VSSX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VSSX fájl?

A .vssx kiterjesztésű fájlok a [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013-as vagy újabb verziójával létrehozott rajzsablonok. A VSSX fájlformátum a Visio 2013 és újabb verzióival nyitható meg. A Visio fájlok számos rajzelem megjelenítéséről ismertek, mint például alakzatok gyűjteménye, csatlakozók, folyamatábrák, hálózati elrendezés, UML-diagramok, szoftverdiagramok, adatbázis-modellek, objektumleképezés és más hasonló információk. A Microsoft Visio lehetőséget biztosít Visio-fájlok különböző fájlformátumokká konvertálására is, például [PNG](/hu/image/png/), [BMP](/hu/image/bmp/), [PDF](/hu/pdf/) és mások. Windows és Mac OS rendszerre is elérhető.

## VSSX fájlformátum

A VSSX fájlformátum a Microsoft által 2007 óta elfogadott OpenOffice formátumon alapul. A [ZIP](/hu/compression/zip/) archívumra épül, amely a teljes fájlformátumot képviseli az XML fájlformátum specifikációi alapján. A VSSX bináris fájlformátumának megfelelője a Visio 2007-ig támogatott VSS volt. A VSSX fájlformátum tartalmát megtekintheti, ha a kiterjesztését .ZIP-re cseréli, és megnyithatja bármely archiválási fájlformátumban, például a WinZIP-ben.

A VSDX fájlok a nyílt csomagolási egyezményeken és az XML-en alapulnak, és a fejlesztők profitálhatnak ebből a formátumból, ha megtanulják, hogyan kell programozottan dolgozni ezekkel a fájlokkal. A formátum ugyanazokat az XML-struktúrákat örökli, mint a Visio XML Drawing fájlformátum (.vdx) részei. A Visio fájlokkal való együttműködés nagymértékben megnövekedett, mivel a harmadik féltől származó szoftverek képesek fájlformátum szinten kezelni a Visio fájlokat.

Bizonyos egyéb fájltípusok, amelyek a Visio 2013 fájlformátumot tartalmazzák, a következők:

* .vsdm (Visio makró-kompatibilis rajz)
* .vssx (Visio stencil)
* .vssm (Visio makró-kompatibilis sablon)
* .vstx (Visio sablon)
* .vstm (Visio makró-kompatibilis sablon)

Minden Visio-fájlt más fájlokat vagy részeket tartalmazó csomagnak neveznek. A csomag része lehet XML fájl, kép vagy akár VBA-megoldás is. A csomagon belüli részek feloszthatók „dokumentum” és „kapcsolat” részekre.

## Referenciák ##

* [Bevezetés a Visio fájlformátumba](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [Sématérkép – Visio XML](https://learn.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)

