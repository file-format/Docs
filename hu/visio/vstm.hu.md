{
  "date" : "2019-10-11",
  "keywords" :[ "vstm fájl", "vstm fájlformátum", "mi az a vstm fájl", "fájl", "vstm példa", "vstm fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM – Microsoft Visio sablonfájlformátum",
  "description":"További információ a VSTM fájlformátumról és az API-król, amelyek létrehozhatnak és megnyithatnak VSTM fájlokat.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VSTM fájl?

A VSTM kiterjesztésű fájlok a Microsoft Visio programmal létrehozott sablonfájlok, amelyek támogatják a makrókat. A VSDX fájloktól eltérően a VSTM-sablonokból létrehozott fájlok Visual Basic for Applications (VBA) kóddal kifejlesztett makrókat futtathatnak. A dokumentum alapbeállításainak megadásához sablonfájlt lehet létrehozni, amely felhasználható további dokumentumok létrehozására ezekkel a beállításokkal. A Visio fájlokat olyan rajzok készítésére használják, amelyek vizuális objektumokat, folyamatábrákat, UML-diagramokat, információáramlást, szervezeti diagramokat, szoftverdiagramokat, hálózati elrendezést, adatbázis-modelleket, objektumleképezést és más hasonló információkat tartalmaznak. A Visio segítségével generált fájlok exportálhatók különböző fájlformátumokba is, például PNG, BMP, PDF és másokba.

## Fájlformátum ##

A VSTM-fájlok a nyílt csomagolási egyezményeken és az XML-en alapulnak, és a fejlesztők profitálhatnak ebből a formátumból, ha megtanulják, hogyan kell programozottan dolgozni ezekkel a fájlokkal. A formátum ugyanazokat az XML-struktúrákat örökli, mint a Visio XML Drawing fájlformátum (.vdx) részei. A Visio fájlokkal való együttműködés nagymértékben megnövekedett, mivel a harmadik féltől származó szoftverek képesek fájlformátum szinten kezelni a Visio fájlokat.

Minden Visio-fájlt más fájlokat vagy részeket tartalmazó csomagnak neveznek. A csomag része lehet XML fájl, kép vagy akár VBA-megoldás is. A csomagon belüli részek feloszthatók „dokumentum” és „kapcsolat” részekre.

### Dokumentum ###

A dokumentum részei tartalmazzák a Visio fájl tényleges tartalmát és metaadatait, például a fájl nevét, az első oldalt és a benne lévő összes alakzatot, sőt az alakzatokhoz tartozó adatkapcsolatokat is. A csomagon belüli képek és szöveges fájlok dokumentumrészeknek minősülnek.

### Kapcsolatok ###

A Visio-fájlok kapcsolati részei a „_rels” mappában vannak tárolva, és leírják, hogy a csomagon belüli részek hogyan kapcsolódnak mindegyikhez. A fájl szerkezetét is megadja. Egy önálló XML-dokumentum az elemek szülő/utód kapcsolatát használja az entitások egymáshoz való viszonyának meghatározására. Egy érvényes Visio 2013 fájlformátum tartalmazza az alkatrészek megfelelő készletét, és a csomag tartalmazza az alkatrészek közötti kapcsolatokat.

A kapcsolati részek olyan XML dokumentumok, amelyek a csomagon belüli különböző dokumentumrészek közötti kapcsolatokat írják le. Ezek társítást határoznak meg két elem között: egy meghatározott forrás (a kapcsolatfájl neve és helye által meghatározott) és egy meghatározott céldokumentum rész között. A kapcsolati részek például arra szolgálnak, hogy leírják, mely alakzat-mesterek vannak társítva a fájlhoz, hogyan kapcsolódnak az oldalak a fájlhoz és egymáshoz, vagy hogyan kapcsolódnak a képek és az objektumok egy adott oldalhoz.

## Referenciák ##

* [Bevezetés a Visio fájlformátumba](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

