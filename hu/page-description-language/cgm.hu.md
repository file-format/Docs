{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CGM fájlformátum",
  "description":"További információ a CGM fájlformátumról és az API-król, amelyek CGM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az a CGM fájl? ##

A Computer Graphics Metafile (CGM) egy ingyenes, platformfüggetlen, nemzetközi szabványos metafájl formátum vektorgrafikák (2D), rasztergrafikák és szövegek tárolására és cseréjére. A CGM objektum-orientált megközelítést és számos funkciófeltételt használ a képkészítéshez. A CGM ezeket az objektumorientált jellemzőket használja a grafikus elemek újraformázásához a kép megjelenítéséhez. A metafájl olyan szükséges információkat tartalmaz, amelyek más fájlokat határoznak meg. A CGM-ben a szöveg alapú forrásfájl tartalmazza az összes grafikus elemet, amely később bináris fájllá fordítható. A CGM alapvetően egy módja annak, hogy megkönnyítse a 2D grafikus adatcserét, függetlenül minden adott platformtól vagy eszköztől.

A CGM formátum különböző elemeket biztosít a funkciók végrehajtásához és az objektumok jelöléséhez a geometriai primitívek és a grafikus információk beállításához. Bár a CGM-et más formátumok váltották fel a grafika weboldalakon való megjelenítésére, mivel a weboldalak nem támogatják megfelelően, még mindig nagyon népszerű az ipari, repülési és egyéb műszaki alkalmazások körében. Bár a World Wide Web Consortium kifejlesztette a WebCGM-et, amely egy alternatív megközelítés a CGM webes használatához. Az elsődleges CGM implementáció a grafikus kernelrendszer (GKS) alapvető műveleteinek sorozatát illusztrálta. A professzionális tervezésben nem nagyon alkalmazták, de nagyrészt kiszorította más formátumok, például a DXF és az SVG.

## Előzmények ##

A CGM 1987-ben nemzetközi szabványnak bizonyult (ISO 8632-1987), és az Egyesült Királyságban a BSI, az Egyesült Államokban pedig az ANSI nemzeti szabványként is elfogadta. Számos 1991-es módosítás után 1992-ben megjelent a CGM felülvizsgált szabványa (ISO 8632:1992). 2001-ben a World Wide Web Consortium kifejlesztette a WebCGM-et, amely továbbfejlesztett képességgel rendelkezik a weboldalakkal való használatra. 2007-ben adták ki a WebCGM második verzióját, a harmadik verziót pedig 2010-ben, továbbfejlesztett képességekkel.

## CGM fájlformátum ##

A számítógépes grafikai metafájlok alapvetően grafikus információk adatbázisai, és grafikus adatok rögzítésére, tárolására és továbbítására szolgálnak. Következésképpen egy grafikus rendszerkomponensnek kell lennie az adatbázis létrehozásához az alkalmazás metafájl formátumú végrehajtásával egyidejűleg. A legtöbb esetben ez az összetevő a Metafile generátor. Emellett szükség van egy másik összetevőre is, amely képes lekérni, értelmezni és megjeleníteni egy metafájlban lévő grafikus adatokat. Ezt az igényt egy metafájl értelmező jelenléte elégíti ki. A következő ábra a grafikus metafájl munkakörnyezetet mutatja be.

A CGM kapcsolatát egy tipikus grafikus rendszer más komponenseivel a fenti ábra szemlélteti. Az ábrán az is látható, hogy a metafájl funkcionalitása nem függ az eszköz végső kimenetétől.

A metafájloknak általában két kategóriája van: **szakaszrögzítés** és **képrögzítés**. A képrögzítési metafájl elsődleges funkciója az eszközfüggetlen, többszörös képdefiníciók rögzítése. Míg a munkamenet-rögzítési metafájlok a rendszerfelületet használják a kimeneti párbeszéd rögzítésére egy grafikus rendszerben. A CGM a statikus képrögzítési metafájlok kategóriájába tartozik. A CGM az alkatrészek jól szervezett elrendezését biztosítja kétszintű felépítéssel.

1. Metafájl leíró
1. Logikailag független képek halmaza

Minden kép képleírók gyűjteménye, valamint egy képtörzs, beleértve a képdefiníciót. A metafile descriptor olyan leíró információt definiál, amely egyformán vonatkozik a metafájl összes képére. Ez az információ segít a tolmácsnak a metafájl helyes elemzésében és a kép helyes megjelenítéséhez szükséges erőforrások felismerésében. Bár a képleíró tartalmazza a leíró információt is, mégis csak azt a képet tudja felismerni, amelyben a leíró található. Ebben a fájlformátumban minden képdefiníció önálló és logikailag szuverén. Függetlenek a fájlban található összes többi képdefiníciótól. Közvetlenül a meta-leíró értelmezése után a képek véletlenszerűen érhetők el és értelmezhetők. A korábbi képek állapotának változása nincs hatással az utódaikra. Ez a képfüggetlenség a CGM másik kiemelkedő jellemzője. A CGM koordinátateret tartalmaz, amelyek 2D derékszögű koordináták, amelyeket virtuális eszköz koordinátáinak neveznek, és számmal vagy pontossággal ábrázolhatók, amelyek a tartományt és a részletességet reprezentálják. A CGM a színek közvetlen kiválasztását és az index alapú kijelölést egyaránt meghatározza. Az előbbi esetben a színmeghatározó egy RGB hármasból áll, míg később a színmeghatározó egy színtáblázatba mutató indexet jelez.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
