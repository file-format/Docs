{
  "date" : "2019-10-11",
  "keywords" :[ "vstx fájl", "vstx fájlformátum", "mi az a vstx fájl", "fájl", "vstx példa", "vstx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX – Microsoft Visio fájlformátum",
  "description":"További információ a VSTX fájlformátumról és az API-król, amelyek VSTX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VSTX fájl?

A .vstx kiterjesztésű fájlok a Microsoft Visio 2013 vagy újabb verziójával létrehozott rajzsablonfájlok. Ezek a VSTX-fájlok kiindulási alapot biztosítanak a Visio-rajzok létrehozásához, amelyeket [.VSDX](/hu/image/vsdx/) fájlként mentenek el, alapértelmezett elrendezéssel és beállításokkal. Általában a Visio fájlokat olyan rajzok létrehozására használják, amelyek vizuális objektumokat, folyamatábrákat, UML-diagramokat, információáramlást, szervezeti diagramokat, szoftverdiagramokat, hálózati elrendezést, adatbázis-modelleket, objektumleképezést és más hasonló információkat tartalmaznak. A Visio segítségével létrehozott fájlok exportálhatók különböző fájlformátumokba is, például [PNG](/hu/image/png/), [BMP](/hu/image/bmp/), [PDF](/hu/pdf/) és mások. A VSTX fájlokat megnyitó programok közé tartozik a Microsoft Visio for Windows és Mac, amely lehetővé teszi a fájlok megnyitását megtekintés és szerkesztés céljából. Lehetővé teszi a Visio fájlformátumok számos más formátumba való konvertálását is.

# VSTX fájlformátum #

A fájlkiterjesztésben szereplő "X" az OpenOffice fájlformátumra utal, amelyet a Microsoft [ZIP](/hu/compression/zip/) archív fájlformátumként vezetett be a korábban támogatott bináris fájlformátumok helyettesítésére. A VSTX-fájlok tehát az OpenOffice-specifikációk XML-fájlformátumán alapulnak, ellentétben a [.VST](/hu/image/vst/) fájlformátummal, amely bináris formátumú.

A VSDX fájlok a nyílt csomagolási egyezményeken és az XML-en alapulnak, és a fejlesztők profitálhatnak ebből a formátumból, ha megtanulják, hogyan kell programozottan dolgozni ezekkel a fájlokkal. A formátum ugyanazokat az XML-struktúrákat örökli, mint a Visio XML Drawing fájlformátum (.vdx) részei. A Visio fájlokkal való együttműködés nagymértékben megnövekedett, mivel a harmadik féltől származó szoftverek képesek fájlformátum szinten kezelni a Visio fájlokat.

Bizonyos egyéb fájltípusok, amelyek a Visio 2013 fájlformátumot tartalmazzák, a következők:

* .vsdm (Visio makró-kompatibilis rajz)
* .vssx (Visio stencil)
* .vssm (Visio makró-kompatibilis sablon)
* .vstx (Visio sablon)
* .vstm (Visio makró-kompatibilis sablon)

A motorháztető alatt a Visio 2013 fájlformátum strukturált módon tárolja az alkalmazásadatokat a kapcsolódó erőforrásokkal együtt egy archívumban, például [ZIP](/hu/compression/zip/). A ZIP fájl bármely szabványos kicsomagoló segédprogrammal kibontható, ahol más típusú fájlokat is tartalmaz. A .VSTX fájlkiterjesztést .ZIP-re cserélheti a Windows Explorerben, hogy megtekinthesse a VSTX fájl tartalmát.

Minden Visio-fájlt más fájlokat vagy részeket tartalmazó csomagnak neveznek. A csomag része lehet XML fájl, kép vagy akár VBA-megoldás is. A csomagon belüli részek feloszthatók „dokumentum” és „kapcsolat” részekre.

### Dokumentum ###

A dokumentum részei tartalmazzák a Visio fájl tényleges tartalmát és metaadatait, például a fájl nevét, az első oldalt és a benne lévő összes alakzatot, sőt az alakzatokhoz tartozó adatkapcsolatokat is. A csomagon belüli képek és szöveges fájlok dokumentumrészeknek minősülnek.

### Kapcsolatok ###

A Visio-fájlok kapcsolati részei a „_rels” mappában vannak tárolva, és leírják, hogy a csomagon belüli részek hogyan kapcsolódnak mindegyikhez. Megadja a fájl szerkezetét is. Egy önálló XML-dokumentum az elemek szülő/utód kapcsolatát használja az entitások egymáshoz való viszonyának meghatározására. Egy érvényes Visio 2013 fájlformátum tartalmazza az alkatrészek megfelelő készletét, és a csomag tartalmazza az alkatrészek közötti kapcsolatokat.

A kapcsolati részek olyan XML dokumentumok, amelyek a csomagon belüli különböző dokumentumrészek közötti kapcsolatokat írják le. Társulást határoznak meg két elem között: egy meghatározott forrás (a kapcsolatfájl neve és helye által meghatározott) és egy meghatározott céldokumentum rész között. A kapcsolati részek például arra szolgálnak, hogy leírják, mely alakzat-mesterek vannak társítva a fájlhoz, hogyan kapcsolódnak az oldalak a fájlhoz és egymáshoz, vagy hogyan kapcsolódnak a képek és az objektumok egy adott oldalhoz.

## Hivatkozások ##

* [Bevezetés a Visio fájlformátumba](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

