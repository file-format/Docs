{
  "date" : "2019-10-11",
  "keywords" :[ "osm fájl", "mi az osm fájl", "fájl", "osm példa", "osm fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap fájlformátum",
  "description":"További információ az OSM fájlformátumról és az API-król, amelyek OSM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az OSM fájl?

Az OpenStreetMap (OSM) önkéntes földrajzi információk hatalmas gyűjteménye, amelyek különböző típusú fájlokban tárolódnak, különböző kódolási sémákat használva az adatok bitekké és bájtokká alakításához. Az OSM egy közös erőfeszítés egy ingyenesen szerkeszthető világtérkép létrehozására. Ennek az együttműködésnek az elsődleges eredménye a földrajzi adatok, nem pedig maga a térkép. A földrajzi információk felhasználásának vagy elérhetőségének korlátai a világ nagy részén szükségessé teszik az OSM létrehozását. Az OSM-től elérhető adatok készen állnak arra, hogy helyettesítsék a Google Térképet a klasszikus alkalmazásokhoz (Facebook, Craigslist stb.) és az alapértelmezett adatokat a GPS-vevő alkalmazásokhoz.^^ ^^Bár az adatok minősége világszerte változatos, az OpenStreetMap adatok kényelmesen összehasonlíthatók a szabadalommal adatforrások.

## Rövid története ##

A Wikipédia sikere által ihletett 2004-ben Steve Coast brit vállalkozó létrehozta ezt a közösségi alapú világtérképezési projektet az Egyesült Királyságban. Kezdetben az Egyesült Királyság feltérképezésére összpontosított. Az OpenStreetMap Foundationt először 2006 áprilisában hozták létre, hogy bárki számára támogassa az ingyenes térinformatikai adatok fejlődését, terjeszkedését és terjesztését. 2006 decemberében a Yahoo segítette az OpenStreetMap légifelvételeit a térképkészítéshez. Hollandia teljes útadatait, valamint India és Kína főútvonaladatait 2007 áprilisában az Automotive Navigation Data (AND) szolgáltatta az OSM-nek. 2007 decemberében az Oxfordi Egyetem volt a legjelentősebb szervezet, amely az OpenStreetMap adatokat integrálta fő webhelyére. Azóta több mint 2 millió regisztrált felhasználó járult hozzá adatokkal ehhez a projekthez GPS-eszközök, légi fényképezés és kézi felmérések segítségével. Ezek a közösség által hozzáadott adatok az Open Database License alatt érhetők el. Egy Angliában bejegyzett non-profit szervezet, az OpenStreetMap Foundation tartotta fenn az OSM oldalát.

## OSM fájlformátum ##

Számos mód és fájlformátum létezik a földrajzi adatok tárolására, de az **OSM** fájlformátum az OpenStreetMap-re korlátozódik. Az OSM kifejezetten szabványos formátum, amelyet az interneten való könnyű szállításra terveztek. Az XML-ben kódolt strukturált, rendezett formátum .osm fájlt alkot. Az OpenStreetMapben négy pivot elem van a topológiai adatstruktúra tárolására:

{{< figure src="../OSM.png" alt="OSM fájlformátum" >}}


|Csomópontok|Utak|Kapcsolatok|Címkék
---|---|---|---|
|<ul><li> A földrajzi helyzetet szélességi és hosszúsági fokok párjaként tárolja.</li><li> A méret nélküli térképelemek, például hegycsúcsok megjelenítésére szolgál.</li></ul> |<ul><li> A csomópontok rendezett listái, amelyek vonalláncot vagy sokszöget jelölnek</li><li> Lineáris elemeket, például utakat és folyókat, valamint zónákat, például parkolóhelyeket, dzsungeleket és parkokat ábrázol.</li></ul> |<ul><li> A csomópontok és utak rendezett listái reprezentálják kapcsolatukat, például sorompók és u kanyarok az utakon, autópályák különböző meglévő utakat és lyukakkal ellátott területeket fednek le.</li></ul> |<ul><li> Tárolja metaadatokat a térképobjektumokról.* Mindig minden csomóponthoz, úthoz vagy relációhoz kapcsolódik</li></ul>


A címkék a földi fizikai jellemzők (épületek és utak stb.) jellemzésére szolgálnak az OpenStreetMapben. Minden címke az adott csomópont vagy reláció által képviselt jellemző földrajzi jellemzőihez kapcsolódik. Ebben az ingyenes címkézési rendszerben egy jellemző leírásához korlátlan számú attribútum szerepelhet egy térképen. A regisztrált felhasználók által jóváhagyott speciális kulcs- és értékkombinációk informális szabványokként szolgálnak a gyakran használt címkék számára. Mindazonáltal új címkék hozhatók létre, amikor új szempontok szükségesek a jellemzők korábban nem leképezett attribútumainak elemzéséhez. A legtöbb funkció csak kevés címkét használ a leíráshoz.

Az OSM háromféle fájlt használ fő adatainak tárolására.

Az OSM ezeket a fájlokat a formázási részletekkel együtt kezeli. De ezek a fájlok ugyanazokat a belső objektumokat állítják elő. Adatfájlok esetén az OSM objektumokon látható jelző mindig igaz, ami nem igaz az előzmények és a változásfájlok esetében.

Általános használatban az OSM fájlformátumok változatosak. A fájlformátumok bitekben és bájtokban határozzák meg a lemezen vagy vezetéken lévő tartalomkódolást. Az OSM a legtöbb ilyen formátumot képes olvasni és írni.

**XML**

Az eredeti OSM formátum XML alapú. A fő OSM adatbázis API visszatérési adatai XML formátumban vannak.

**PBF**

A Protocol Buffers kódolás bináris formátumú, és az egyik legkompaktabb formátum.

**O5M/O5C**

Bináris formátum alapú egyszerűbb formátum, de viszonylag kevésbé használt. Az OSM tudja olvasni, de nem írja ezt a formátumot.

**OPL**

A szabványos UNIX parancssori eszközökhöz javasolt egyszerű formátum. Közel a CSV-fájlokhoz, egyetlen OSM entitást tesz lehetővé egy sorban.

**DEBUG**

Hibakereséshez létrehozandó szöveges formátum. Az OSM tudja írni ezt a formátumot, de nem tudja olvasni.

**FEKETE LYUK**

Hamis formátum, amely minden adatot tartalmaz. Az OSM tudja írni ezt a formátumot, de nem tudja olvasni.

## OSM adattárolás ##

Az OSM fő **PostgreSQL** adatbázisa megőrzi az OSM adatok fő példányát PostGIS kiterjesztéssel. A fő adatbázis minden adatprimitívhez egy táblát tart fenn, amelynek sorai egyedi objektumokat tárolnak. Minden szerkesztés frissíti ezt az adatbázist, és minden más formátum ennek az adatbázisnak a felhasználásával jön létre. Számos letölthető adatbázis-készlet jön létre az adatok egyik helyről a másikra történő átvitelére. Két formátum határozza meg ezeket a készleteket, az egyik XML-t, a másik pedig a Protocol Buffer Binary Format (PBF) formátumot használja. A teljes adatot a planet.osm nevű fájl tárolja

## Tömörítés az OSM fájlokban ##

A szövegalapú formátumok (XML, OPL és Debug) opcionálisan gzip vagy bzip2 tömörítést használnak.

## Referenciák ##

* [OSM fájlformátumok kézikönyve](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Learn OSM](https://learnosm.org/en/osm-data/getting-data/)

