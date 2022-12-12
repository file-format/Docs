{
  "date" : "2019-10-11",
  "keywords" :[ "vsdx fájl", "vsdx fájlformátum", "mi az a vsdx fájl", "fájl", "vsdx példa", "vsdx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"További információ a VSDX fájlformátumról és az API-król, amelyek VSDX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VSDX fájl?

A .vsdx kiterjesztésű fájlok a Microsoft Office 2013-tól kezdődően bevezetett Microsoft Visio fájlformátumot képviselik. A Microsoft Visio korábbi verziói által támogatott [.VSD](/hu/image/vsd/) bináris fájlformátum helyettesítésére fejlesztették ki. A Microsoft SharePoint Server 2013 Visio Services szolgáltatása is támogatja, és nem igényel közvetítő fájlformátumot a SharePoint Serveren való közzétételhez. A Visio fájlokat olyan rajzok készítésére használják, amelyek vizuális objektumokat, folyamatábrákat, UML-diagramokat, információáramlást, szervezeti diagramokat, szoftverdiagramokat, hálózati elrendezést, adatbázis-modelleket, objektumleképezést és más hasonló információkat tartalmaznak. A Visio segítségével generált fájlok exportálhatók különböző fájlformátumokba is, például [PNG](/hu/image/png/), [BMP](/hu/image/bmp/), [PDF](/hu/pdf/) és mások.

## Fájlformátum ##

A VSDX fájlok a nyílt csomagolási egyezményeken és az XML-en alapulnak, és a fejlesztők profitálhatnak ebből a formátumból, ha megtanulják, hogyan kell programozottan dolgozni ezekkel a fájlokkal. A formátum ugyanazokat az XML-struktúrákat örökli, mint a Visio XML Drawing fájlformátum (.vdx) részei. A Visio fájlokkal való együttműködés nagymértékben megnövekedett, mivel a harmadik féltől származó szoftverek képesek fájlformátum szinten kezelni a Visio fájlokat.

Bizonyos egyéb fájltípusok, amelyek a Visio 2013 fájlformátumot tartalmazzák, a következők:

* .vsdm (Visio makró-kompatibilis rajz)
* .vssx (Visio stencil)
* .vssm (Visio makró-kompatibilis sablon)
* .vstx (Visio sablon)
* .vstm (Visio makró-kompatibilis sablon)

A motorháztető alatt a Visio 2013 fájlformátum strukturált módon tárolja az alkalmazásadatokat a kapcsolódó erőforrásokkal együtt egy archívumban, például [ZIP](/hu/compression/zip/). A ZIP fájl bármely szabványos kicsomagoló segédprogrammal kibontható, ahol más típusú fájlokat is tartalmaz. A Windows Explorerben egyszerűen lecserélheti a .vsdx fájlkiterjesztést .zip-re, hogy megtekinthesse a VSDX fájl tartalmát.

Minden Visio-fájlt más fájlokat vagy részeket tartalmazó csomagnak neveznek. A csomag része lehet XML fájl, kép vagy akár VBA-megoldás is. A csomagon belüli részek feloszthatók „dokumentum” és „kapcsolat” részekre.

### Dokumentum ###

A dokumentum részei tartalmazzák a Visio fájl tényleges tartalmát és metaadatait, például a fájl nevét, az első oldalt és a benne lévő összes alakzatot, sőt az alakzatokhoz tartozó adatkapcsolatokat is. A csomagon belüli képek és szöveges fájlok dokumentumrészeknek minősülnek.

### Kapcsolatok ###

A Visio-fájlok kapcsolati részei a „\_rels” mappában vannak tárolva, és leírják, hogy a csomagon belüli részek hogyan kapcsolódnak egymáshoz. Megadja a fájl szerkezetét is. Egy önálló XML-dokumentum az elemek szülő/utód kapcsolatát használja az entitások egymáshoz való viszonyának meghatározására. Egy érvényes Visio 2013 fájlformátum tartalmazza az alkatrészek megfelelő készletét, és a csomag tartalmazza az alkatrészek közötti kapcsolatokat.

A kapcsolati részek olyan XML dokumentumok, amelyek a csomagon belüli különböző dokumentumrészek közötti kapcsolatokat írják le. Társulást határoznak meg két elem között: egy meghatározott forrás (a kapcsolatfájl neve és helye által meghatározott) és egy meghatározott céldokumentum rész között. A kapcsolati részek például arra szolgálnak, hogy leírják, mely alakzat-mesterek vannak társítva a fájlhoz, hogyan kapcsolódnak az oldalak a fájlhoz és egymáshoz, vagy hogyan kapcsolódnak a képek és az objektumok egy adott oldalhoz.

## Hivatkozások ##

* [Bevezetés a Visio fájlformátumba](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

