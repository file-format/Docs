{
  "date" : "2020-03-16",
  "keywords" :[ "IFC fájl", "Formátum", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az IFC fájlformátumról és az API-król, amelyek IFC-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"IFC fájlformátum",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az IFC fájl?

Az IFC kiterjesztésű fájlok az Industry Foundation Classes (IFC) fájlformátumra vonatkoznak, amely nemzetközi szabványokat állapít meg az épületobjektumok és tulajdonságaik importálására és exportálására. Ez a fájlformátum együttműködést biztosít a különböző szoftveralkalmazások között. Ennek a fájlformátumnak a specifikációit a buildingSMART International fejlesztette ki és tartja karban, mint adatszabványt. Az IFC fájlformátum végső célja a kommunikáció, a termelékenység, a szállítási idő és a minőség javítása az épület teljes életciklusa során.

Az építőiparban általánosan elterjedt tárgyakra megállapított szabványoknak köszönhetően csökkenti az információvesztést az egyik alkalmazásból a másikba történő átvitel során. Az IFC számos különböző szakmához (építész, villamos, HVAC, szerkezeti, terep stb.) tárolhat geometriai, számítási, mennyiségi, létesítménygazdálkodási, árképzési stb. adatokat.

## Rövid története ##

Az IFC kezdeményezést 1994-ben az Autodesk kezdeményezte, hogy támogassa az integrált alkalmazásfejlesztést, és olyan cégeket is magában foglal, mint a Honeywell, a Butler Manufacturing és az AT&T. 1995-ben a tagság megnyílt bárki számára, a név pedig International Alliance for Interoperability névre változott. A non-profit szervezet célja az volt, hogy az Industry Foundation Class-t (IFC) AEC termékmodellként tegye közzé. 2005-ben a név ismét megváltozott, és most a buildSMART tartja karban.

## IFC fájlformátum ##

Az IFC fájlformátum az elmúlt időszakban számos változáson ment keresztül, hogy elérje a v4 fájlformátum-specifikációt. Időről időre több kisebb változtatás is történt, valamint kiegészítésekként a specifikációk részévé váltak. Az alábbiakban felsoroljuk a fájlspecifikációk különböző verzióit, amelyeket a múltban nyilvánosságra hoztak.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (2013. március) ifcXML2x3 (2007. június)
* IFC2x3 (2006. február) ifcXML2 for IFC2x2 add1 (RC2)
* IFC2x2 1. kiegészítés (2004. július) ifcXML2 az IFC2x2 (RC1) számára
* IFC 2x2IFC 2x Addendum 1ifcXML1 az IFC2x és
* IFC2x kiegészítés 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Az IFC fájlformátum-specifikációk legfrissebb verziói mindig elérhetők a buildingSMART webhelyen, és a fejlesztőnek meg kell tekintenie ezeket az általa fejleszteni tervezett bármilyen típusú alkalmazáshoz. A cikk írásakor a 4-es verzió specifikációi az online legfrissebbek.

### IFC adatfájl formátumok ###

Az IFF fájlformátum támogatja az alkalmazások közötti adatcserét az alábbiak szerint különböző formátumokat használva:

**IFC:** Ez az alapértelmezett IFC csereformátum, és az ISO 10303-21 szabvány szerinti STEP fizikai fájlstruktúrát használja. Ez a fájlformátum .ifc kiterjesztésű, és a leggyakrabban használt IFC formátum.

**IFC-XML:** Az IFC XML fájlformátumú változata, amelyet közvetlenül a küldő alkalmazás generálhat az ISO 10303-28 szabvány szerint, más néven STEP-XML. Az IFC-XML fájlformátum alkalmasnak tekinthető az XML-eszközök közötti együttműködésre. Az IFC fájlformátumhoz képest az IFC-XML mérete 300-400%-kal nagyobb.

**IFC-ZIP:** Ez az IFC vagy IFC-XML [ZIP](/hu/compression/zip/) tömörített változata, ahol a fájlok egyike a zip-archívum fő könyvtára. Ez a formátum az .ifc fájlokat 60-80%-kal, az .ifc XML fájlokat pedig 90-95%-kal tömöríti.

### IFC architektúra ###

Az IFC specifikáció olyan kifejezéseket, fogalmakat és adatspecifikációs elemeket tartalmaz, amelyek az építőipari és létesítménygazdálkodási ágazat tudományágain, szakmáin és szakmáin belüli felhasználásból származnak. A kifejezések és fogalmak az egyszerű angol szavakat használja, az adatspecifikációban szereplő adatelemek elnevezési konvenciót követnek.

a típusok, entitások, szabályok és függvények adatelemnevei az „Ifc” előtaggal kezdődnek, és a CamelCase elnevezési konvencióban szereplő angol szavakkal folytatódnak (aláhúzás nélkül, a szó első betűje nagybetűvel); az entitáson belüli attribútumnevek előtag nélkül követik a CamelCase elnevezési konvenciót; a szabvány részét képező tulajdonságkészlet-definíciók a "Pset_" előtaggal kezdődnek, és az angol szavakkal folytatódnak a CamelCase elnevezési konvencióban; a szabvány részét képező mennyiségkészlet-definíciók a "Qto_" előtaggal kezdődnek, és a CamelCase elnevezési konvencióban szereplő angol szavakkal folytatódnak.

Az IFC adatséma architektúrája négy fogalmi réteget határoz meg, minden egyes séma pontosan egy fogalmi réteghez van hozzárendelve.

**Erőforrás réteg** — a legalsó réteg tartalmazza az összes erőforrás-definíciót tartalmazó egyedi sémát, ezek a definíciók nem tartalmaznak globálisan egyedi azonosítót, és nem használhatók a magasabb rétegben deklarált definíciótól függetlenül;

**Alapréteg** – a következő réteg tartalmazza a kernelsémát és az alapkiterjesztési sémákat, amelyek a legáltalánosabb entitásdefiníciókat tartalmazzák, a magrétegben vagy a felett definiált összes entitás globálisan egyedi azonosítót és opcionálisan tulajdonosi és előzményinformációkat hordoz;

**Interoperabilitási réteg** — a következő réteg olyan entitásdefiníciókat tartalmazó sémákat tartalmaz, amelyek egy általános termék-, folyamat- vagy erőforrás-specializációra jellemzőek, több tudományágon keresztül, ezeket a definíciókat jellemzően a tartományok közötti cserére és az építési információk megosztására használják;

**Domain réteg** — a legmagasabb réteg olyan entitásdefiníciókat tartalmazó sémákat tartalmaz, amelyek egy bizonyos tudományágra jellemző termékek, folyamatok vagy erőforrások specializációi, ezeket a definíciókat jellemzően a domainen belüli cserére és információmegosztásra használják.

## Referenciák ##

* [Industry Foundation Classes – Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

