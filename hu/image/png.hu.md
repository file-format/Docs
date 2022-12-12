{
  "date" : "2019-10-11",
  "keywords" :[ "png fájl", "png fájl formátum", "mi az a png fájl", "fájl", "png példa", "png fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG fájlformátum - raszteres képfájl",
  "description":"További információ a PNG fájlformátumról és az API-król, amelyek PNG-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PNG fájl?

A **PNG** (Portable Network Graphics) fájl egy raszteres képfájl formátum, amely veszteségmentes tömörítést használ. Ezt a fájlformátumot a Graphics Interchange Format ([GIF](/hu/image/gif/)) helyettesítésére hozták létre, és nincs szerzői jogi korlátozása. A PNG fájlformátum azonban nem támogatja az animációkat. A PNG fájlformátum támogatja a veszteségmentes képtömörítést, amely népszerűvé teszi a felhasználók körében. Az idő múlásával a PNG az egyik széles körben használt képfájlformátummá fejlődött.

## A PNG fájlformátum rövid története

A PNG fájlformátum létrehozásának fő oka a szabadalmaztatott tömörítési algoritmus, a Lempel-Ziv-Welch volt, amelyet a GIF fájlformátumban használtak. Ez az egyéb GIF-korlátozásokkal együtt szükségessé tette a [**GIF**](/hu/image/gif/) fájlformátum cseréjét. Az első javaslat és név a PNG fájlformátumra 1995 januárjában érkezett. A PNG fájlformátumokkal kapcsolatos legfontosabb események az alábbiakban találhatók:

* 1996. október: Kiadták a PNG specifikációk 1.0-s verzióját, amely később [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083 néven jelent meg. 1996 októberében ugyanez a W3C ajánlás lett.
* 1998. december: Megjelent az 1.1-es verzió, néhány apró változtatással és három új darab hozzáadásával.
* 1999. augusztus: Kiadták az 1.2-es verziót, egy plusz darabbal.
* 2003. november: A PNG nemzetközi szabvány lett (ISO/IEC 15948:2003). A PNG ezen verziója csak kis mértékben tér el az 1.2-es verziótól, és nem ad hozzá új darabokat.
* 2004. március: ISO/IEC 15948:2004

## A GIF és a PNG funkcionális összehasonlítása

A PNG fájlformátumot egyszerűnek és hordozhatónak, jogilag tehermentesnek, cserélhetőnek, rugalmasnak és robusztusnak tervezték. Az alábbi táblázat felsorolja azokat a GIF-szolgáltatásokat, amelyeket az új szolgáltatások mellett a PNG-fájlformátum örökölt.

|Funkció|GIF|PNG|
---|---|---|
|Indexszínes képek akár 256 színben|Igen|Igen|
|A streaming támogatása|Igen|Igen|
|Átláthatóság|Igen|Igen|
|Kiegészítő információ|Igen|Igen|
|Hardver- és platformfüggetlenség|Igen|Igen|
|Hatásos|Igen|Igen|
|Truecolor képek legfeljebb 48 bit/pixel|Nem|Igen|
|Maximum 16 bit/pixel szürkeárnyalatos képek|Nem|Igen|
|Teljes alfa-csatorna (általános átlátszósági maszkok)|Nem|Igen|
|Kép gammainformációi|Nem|Igen|
|Megbízhatóság|Nem|Igen|
|Gyorsabb kezdeti prezentáció|Nem|Igen|

## PNG fájl szerkezet

Szinte minden operációs rendszer támogatja a PNG fájlok megnyitását. Például a Microsoft Windows Viewer képes PNG-fájlok megnyitására, mivel az operációs rendszer alapértelmezés szerint rendelkezik a telepítés részeként elérhető támogatással. A PNG-fájl egy PNG "aláírásból" áll, amelyet egy //chunks// sorozat követ.

### PNG fájl fejléc

A PNG-fájl első nyolc bájtja mindig a következő (tizedes) értékeket tartalmazza:

{{{137 80 78 71 13 10 26 10 }}}

Ez az aláírás azt jelzi, hogy a fájl többi része egyetlen PNG-képet tartalmaz, amely egy IHDR-darabbal kezdődő és egy IEND-darabbal végződő darabokból áll.

### Darabok ###

Minden darab négy részből áll:

**Hossz:** 4 bájtos előjel nélküli egész szám, amely megadja a bájtok számát a csonk adatmezőjében. A hossz csak az adatmezőt számolja, önmagát, a darabtípus kódját vagy a CRC-t nem. A nulla érvényes hosszúság. Bár a kódolóknak és dekódolóknak a hosszt előjel nélküliként kell kezelniük, értéke nem haladhatja meg a 231 bájtot.

**Csonk típusa:** 4 bájtos darab típuskód. A leírás és a PNG-fájlok vizsgálatának megkönnyítése érdekében a típuskódok csak nagy- és kisbetűket tartalmazhatnak ASCII-betűket (AZ és az, vagy 65-90 és 97-122 tizedesjegy). A kódolóknak és dekódolóknak azonban a kódokat rögzített bináris értékként kell kezelniük, nem karakterláncként. Például nem lenne helyes az IDAT típuskódot a betűk EBCDIC megfelelőivel ábrázolni. A darabtípusok további elnevezési konvencióit a következő szakasz tárgyalja.

**Chunk Data:** A csonk típusának megfelelő adatbájtok, ha vannak ilyenek. Ez a mező nulla hosszúságú lehet.

**CRC:** Egy 4 bájtos CRC (Cyclic Redundancy Check) a csonk előző bájtjaira számítva, beleértve a darab típuskódját és a csonk adatmezőit, de nem tartalmazza a hosszmezőt. A CRC mindig jelen van, még az adatokat nem tartalmazó daraboknál is.

A csonk adathossza tetszőleges számú bájt lehet a maximumig; ezért az implementátorok nem feltételezhetik, hogy a darabok a bájtoknál nagyobb határokon vannak igazítva.

A darabok bármilyen sorrendben megjelenhetnek, az egyes darabtípusokra vonatkozó korlátozások függvényében. (Egy figyelemreméltó megkötés, hogy az IHDR-nek először, az IEND-nek pedig utoljára kell megjelennie; így az IEND-csonk a fájlvégi jelölőként szolgál.) Több azonos típusú darab is megjelenhet, de csak akkor, ha az adott típushoz kifejezetten engedélyezett.

#### Részlettípusok

A csonktípusok **kritikus** és **kiegészítő** csonkokba vannak sorolva a Csonktípushoz rendelt 4 bájtos kis- és nagybetűk közötti ASCII-érték alapján. Minden megvalósításnak meg kell értenie és sikeresen elő kell írnia a szabványos kritikus darabokat. Az érvényes PNG-képnek tartalmaznia kell egy IHDR-darabot, egy vagy több IDAT-darabot és egy IEND-darabot.

### Tömörítés

A 0-s PNG-tömörítési módszer (az egyetlen tömörítési módszer, amelyet jelenleg PNG-hez definiáltak) a deflate/felfújó tömörítést határozza meg, legfeljebb 32768 bájtos csúszóablakkal. A deflate tömörítés egy LZ77 származék, amelyet zip, gzip, pkzip és kapcsolódó programokban használnak. Széleskörű kutatásokat végeztek szabadalommentes státuszának alátámasztására. A zlib adatfolyamon belüli tömörített adatok blokkok sorozataként vannak tárolva, amelyek mindegyike nyers (tömörítetlen) adatokat, rögzített Huffman-kódokkal kódolt LZ77-tömörített adatokat vagy egyéni Huffman-kódokkal kódolt LZ77-tömörített adatokat jelenthet. Az utolsó blokkban található jelölőbit az utolsó blokkként azonosítja, lehetővé téve a dekódoló számára, hogy felismerje a tömörített adatfolyam végét.

#### Tömörítés előtti szűrés

Előtömörítési szűrőket alkalmaznak a képadatok optimális tömörítésre való előkészítésére. A PNG szűrőmódszer öt alapvető szűrőtípust határoz meg a következők szerint:

|Szűrő típusa|Név|Becsült érték|
---|---|---|
|0|Nincs|A pásztázási vonal módosítás nélkül kerül továbbításra|
|1|Sub|Az egyes bájtok különbségét és az előző képpont megfelelő bájtjának értékét továbbítja.|
|2|Felfelé|A Fel() szűrő pont olyan, mint a Sub() szűrő, azzal a különbséggel, hogy a közvetlenül az aktuális pixel feletti képpont, nem pedig csak attól balra van prediktorként.|
|3|Átlagos|Az Átlag() szűrő a két szomszédos képpont (bal és felett) átlagát használja a pixel értékének előrejelzéséhez.|
|4|Paeth|A Paeth() szűrő a három szomszédos pixel egyszerű lineáris függvényét számítja ki (balra, fent, balra fent), majd a számított értékhez legközelebb eső szomszédos pixelt választja prediktornak.|

A szűrési algoritmusok a "bájtokra" vonatkoznak, nem a pixelekre, függetlenül a kép bitmélységétől vagy színtípusától. A szűrési algoritmusok a scanline által alkotott bájtsorozaton dolgoznak. Ha a kép alfa-csatornát tartalmaz, az alfa-adatokat ugyanúgy szűrjük, mint a képadatokat.

Amikor a kép soros soros, a soros soros minta minden egyes lépését a rendszer független képként kezeli szűrés céljából. A szűrők az áthaladás során ténylegesen továbbított pixelek által alkotott bájtsorozatokon dolgoznak, és az "előző pásztázási vonal" az ugyanabban a lépésben korábban továbbított, nem pedig a teljes képen szomszédos. Vegye figyelembe, hogy az egy lépésben továbbított részkép mindig téglalap alakú, de kisebb szélessége és/vagy magassága, mint a teljes kép. A szűrés nem kerül alkalmazásra, ha ez az alkép üres.

## Referenciák ##

* [PNG – Kezdőlap](http://www.libpng.org/pub/png/)

