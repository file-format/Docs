{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "alapok" ],
  "description":"A Portable Document Format (PDF) a dokumentumok szabványos, szoftvertől, hardvertől és operációs rendszertől független megjelenítése. A PDF szabványok közé tartozik a PDF/A, PDF/E, PDF/UA, PDF/VT és PDF/X.",
  "title" :"PDF fájlformátum - Mi az a PDF fájl?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

A Portable Document Format (PDF) az Adobe által az 1990-es években létrehozott dokumentumtípus. Ennek a fájlformátumnak az volt a célja, hogy szabványt vezessen be a dokumentumok és egyéb referenciaanyagok olyan formátumban, amely független az alkalmazásszoftvertől, a hardvertől és az operációs rendszertől. A PDF fájlformátum teljes mértékben képes olyan információkat tartalmazni, mint például szöveg, képek, hiperhivatkozások, űrlapmezők, multimédiás média, digitális aláírások, mellékletek, metaadatok, térinformatikai jellemzők és 3D objektumok, amelyek a forrásdokumentum részeivé válhatnak.

A legtöbb esetben a meglévő dokumentumokat a rendszer PDF formátumba konvertálja, ahelyett, hogy a semmiből hozna létre egy új PDF-et. Ez azonban nem jelenti azt, hogy nincsenek szoftverek a PDF-fájlok létrehozására vagy manipulálására.

**(Meg kell osztanod valamit a PDF fájlformátumról? Megállapításaidat a [PDF File Format News](https://news.fileformat.com/t/PDF) részben teheted közzé.)**

## PDF fájl formátum - Rövid előzmények

A PDF-fájlok létrehozásának idővonalának gyors áttekintése az idővonal szempontjából a következő:

**1993** – Az Adobe Systems ingyenesen elérhetővé tette a PDF specifikációkat

**2008** – A PDF nyílt szabványként 2008. július 1-jén jelent meg, és a Nemzetközi Szabványügyi Szervezet **ISO 32000-1:2008** néven tette közzé.

**2008** – Az Adobe nyilvános szabadalmi licencet tett közzé az ISO 32000-1 formátumú jogdíjmentes jogokra vonatkozóan az Adobe tulajdonában lévő összes szabadalomra vonatkozóan, amely PDF-kompatibilis megvalósítások készítéséhez, használatához, értékesítéséhez és terjesztéséhez szükséges.

A PDF első verzióját PDF 1.0-nak nevezték el, amely később a PDF 1.7-ig terjedő felülvizsgálatokon ment keresztül. A PDF 1.7, amely az ISO 32000-1 lett, tartalmaz néhány nem szabványosított szabadalmaztatott technológiát, valamint az Adobe XML Forms Architecture (XFA) és az Acrobat JavaScript kiterjesztését. 2017. július 28-án jelent meg az ISO 32000-2:2017 néven ismert PDF 2.0, amely nem tartalmaz nem szabványosított technológiát.

## PDF fájlformátum specifikációi

A PDF-fájl bájtok halmaza, amely a PDF-specifikációkban meghatározott szintaktikai szabályok szerint tokenekbe csoportosítható. Egyszer vagy több token kombinálva magasabb szintű szintaktikai entitásokat, főként objektumokat képez, amelyek azok az alapvető adatértékek, amelyekből a PDF-dokumentum készül.

### PDF fájlok fájlszerkezete

A PDF fájl tartalma a következő sorrendben van elrendezve a fájlon belül.

|Fejléc
|Test
|Kereszthivatkozási táblázat
|Tréler

#### PDF fájl fejléc ####

A PDF-verziótól függetlenül a PDF-fájl egy fejléccel kezdődik, amely tartalmazza a PDF egyedi azonosítóját és a formátum verzióját, például a %PDF-1.x, ahol az x 1 és 7 között van.

#### Fájltörzs ####

A PDF-fájl törzse a dokumentum tartalmát reprezentáló közvetett objektumok sorozatából áll. Az objektumok a fent leírtak szerint a dokumentum összetevőit képviselik, például betűtípusokat, oldalakat és mintaképeket. A PDF 1.5-től kezdődően a törzs tartalmazhat objektumfolyamokat is, amelyek mindegyike közvetett objektumok sorozatát tartalmazza.

#### kereszthivatkozási táblázat ####

A kereszthivatkozási táblázat olyan információkat tartalmaz, amelyek véletlenszerű hozzáférést tesznek lehetővé a fájlon belüli közvetett objektumokhoz, így nem kell a teljes fájlt elolvasni egy adott objektum megtalálásához. A táblázatnak minden közvetett objektumhoz egysoros bejegyzést kell tartalmaznia, amely megadja az objektum bájteltolását a fájl törzsében. (A PDF 1.5-től kezdve a kereszthivatkozási információk egy része vagy egésze kereszthivatkozási adatfolyamokban is szerepelhet.

#### Fájlelőzetes ####

A PDF-fájl előzetese lehetővé teszi a megfelelő olvasó számára, hogy gyorsan megtalálja a kereszthivatkozási táblázatot és bizonyos speciális objektumokat. A megfelelő olvasóknak a PDF-fájlt a végétől kell olvasniuk. A fájl utolsó sora csak a fájlvégi jelölőt tartalmazza, %%EOF. Az előző két sor soronként és sorrendben tartalmazza a startxref kulcsszót és a bájteltolást a dekódolt adatfolyamban a fájl elejétől az xref kulcsszó elejéig az utolsó kereszthivatkozási szakaszban.

### PDF objektumok ###

A PDF-fájl több különböző típusú objektumot tartalmaz, amelyek a következő típusúak

* Logikai értékek – a feltételes igaz vagy hamis érték
* Számok - Egész és valós értékek
* Strings – zárójelben szereplő karaktereket tartalmaz
* Nevek – előre / karakterrel kezdődnek, pl. a /ASomewhatLongerName eredménye az ASomewhatHosszabbnév
* Tömbök – A PDF támogatja az egydimenziós tömböket. A tömbök beágyazott elemként való használatával nagyobb dimenziójú tömbök hozhatók létre
* Szótárak - objektumok gyűjteménye kulcs-érték párként. Nulla bejegyzést tartalmazhat.
* Streamek - bájtok sorozatát jelenti, amely korlátlan hosszúságú is lehet
* Null Object – null értéket jelent

Más objektumok is lehetnek, például megjegyzések, amelyek a % jellel kerülnek bevezetésre, és 8 bites karaktereket tartalmazhatnak.

### Közvetett objektumok ###

A PDF-fájlban lévő bármely objektum közvetett objektumként címkézhető. A közvetett objektumok egyedi objektumazonosítót kapnak, amellyel más objektumok hivatkozhatnak rájuk. Az ezekre való kereszthivatkozások egy indextáblázatban vannak karbantartva, és az xref kulcsszóval vannak megjelölve, amely a törzset követi, és megadja az egyes közvetett objektumok bájteltolását a fájl elejétől számítva.

### Lineáris és nemlineáris PDF-elrendezések ###

A PDF-elrendezések a célalkalmazásoktól és egyéb tényezőktől függően Llnear és nemlineáris kategóriába sorolhatók.

Nem-lineáris – A nemlineáris PDF-fájlok kevesebb lemezterületet igényelnek, mint a lineáris PDF-fájlok. A dokumentum PDF-oldalai elszórtan helyezkednek el a PDF-fájlban, ezért a nemlineáris fájlok lassabbak a lineáris fájlokhoz képest.

Lineáris PDF – Az online PDF-megtekintőket célozva a lineáris PDF-fájlokat úgy készítik el, hogy lineárisan írják őket lemezre. Ehhez nincs szükség böngészőbővítményekre a teljes dokumentum betöltéséhez a megjelenítés előtt.

### Objektumok áttekintése ###

Mint említettük, a PDF törzse a fent említett objektumok gyűjteménye. A PDF nagyrészt PostScript alapú, a programozási nyelvek vezérlőfunkciói nélkül, mint például az if és a loop parancsok. A Postscript kód által kiadott parancsok grafikus tartalmak generálására a dokumentumban hivatkozott fájlok, grafikák vagy betűtípusok mellett összegyűjtik és tokenizálják. Mindezek a tartalmak egyetlen fájlba halmozódnak fel, ami komponált PostScript kimenetet eredményez.

#### Szöveg ####

A PDF-ben a szöveget szövegelemek képviselik, amelyek valójában betűtípusokból származó karakterjelekkel jelennek meg. A karakterjel egy grafikus alakzat, és minden grafikus manipulációnak, például koordináta-transzformációnak van kitéve. A legtöbb oldalleírásban a szöveg fontossága miatt a PDF magasabb szintű lehetőségeket biztosít a karakterjelek kényelmes és hatékony leírásához, kiválasztásához és megjelenítéséhez.

#### Grafika ####

A PDF tartalomfolyamokban használt grafikus operátorok a raszteres kimeneti eszközön reprodukálandó oldalak megjelenését írják le. A létesítmények mind nyomtató, mind kijelző alkalmazásokhoz használhatók. A grafikus operátorok hat fő csoportot alkotnak:

* A grafikus állapot operátorok manipulálják a grafikus állapotnak nevezett adatstruktúrát, azt a globális keretet, amelyen belül a többi grafikus operátor végrehajtja. A grafikus állapot tartalmazza az aktuális transzformációs mátrixot (CTM), amely a PDF tartalomfolyamon belül használt felhasználói térkoordinátákat kimeneti eszköz koordinátáira képezi le. Tartalmazza az aktuális színt, az aktuális vágási útvonalat és sok más olyan paramétert is, amelyek a festési operátorok implicit operandusai.
* Az útvonal-építő operátorok útvonalakat adnak meg, amelyek alakzatokat, vonalpályákat és különböző típusú régiókat határoznak meg. Tartalmaznak operátorokat egy új útvonal elindításához, vonalszegmensek és görbék hozzáadásához, valamint bezárásához.
* A pályafestő operátorok egy pályát színnel töltenek meg, körvonalat festenek rá, vagy vágási határként használják.
* Más festőoperátorok bizonyos önleíró grafikai objektumokat festenek. Ide tartoznak a mintaképek, a geometriailag meghatározott árnyékolások és a teljes tartalomfolyamok, amelyek viszont grafikus operátorok sorozatait tartalmazzák.
* A szöveges operátorok karakterjeleket választanak ki és jelenítenek meg a betűtípusokból (a betűtípusok leírása a szöveges karakterek megjelenítéséhez). Mivel a PDF a karakterjeleket általános grafikus alakzatként kezeli, sok szöveges operátor csoportosítható a grafikai állapot vagy a festés operátoraival. A karakterjelek és betűtípus-leírások kezeléséhez szükséges adatszerkezetek és mechanizmusok azonban kellően speciálisak.
* A megjelölt tartalom operátorai magasabb szintű logikai információkat társítanak a tartalomfolyamban lévő objektumokhoz. Ez az információ nem befolyásolja a tartalom megjelenített megjelenését; olyan alkalmazások számára hasznos, amelyek PDF-et használnak a dokumentumcseréhez.

## Hivatkozások ##

* [PDF fájlformátum: alapstruktúra](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF – Wikipédia](https://en.wikipedia.org/wiki/PDF)
* [PDF-referencia – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

