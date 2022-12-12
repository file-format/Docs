{
  "date" : "2019-10-11",
  "keywords" :[ "psd file", "psd file format", "What is a psd file", "file", "psd example", "psd file extension", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop képfájl formátum",
  "description":"További információ a PSD-fájlformátumról és az API-król, amelyek PSD-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PSD fájl?

A PSD, a Photoshop Document az Adobe Photoshop natív fájlformátumát képviseli, amelyet a grafikai tervezéshez és fejlesztéshez használnak. A PSD-fájlok képrétegeket, korrekciós rétegeket, rétegmaszkokat, megjegyzéseket, fájlinformációkat, kulcsszavakat és más Photoshop-specifikus elemeket tartalmazhatnak. A Photoshop-fájlok alapértelmezett kiterjesztése .PSD, maximális magasságuk és szélességük 30 000 pixel, hosszuk pedig két gigabájt.

## A PSD fájlformátum specifikációi ##

A PSD-fájlban lévő adatok big endian byte sorrendben tárolódnak. Ez azt jelenti, hogy fel kell cserélni a rövid és hosszú egész számokat, amikor Windows platformon olvas vagy ír. A Photoshop fájlformátum öt nagy részre oszlik. Sok hosszjelzővel rendelkezik, amelyek segítségével egyik szakaszról a másikra léphet. A hosszjelölőket általában bájtokkal töltik ki, hogy a legközelebbi 2 vagy 4 bájtos intervallumra kerekítsék. Az öt fő rész a következő:

* Fájl fejléc
* Színmód adatok
* Képforrások
* Réteg és maszk információ
* Képadatok

A megfelelőség érdekében az adatokat a szakasz összes ilyen mezőjébe kell írni, mivel a Photoshop megpróbálhatja beolvasni a teljes részt. Ez azt is jelenti, hogy a fájlba írás közben az átugrott mezőkbe nullákat kell írni. A hosszúsággal határolt szakaszok hosszmezőjét kell használni annak eldöntésére, hogy mikor kell leállítani az olvasást. A legtöbb esetben a hosszmező a következő bájtok számát jelzi, nem a rekordok számát. A fájl olvasása közben a következő pontokat kell megjegyezni.

* A "Length" oszlopban lévő értékek minden táblázatban bájtban vannak megadva.
* Minden Unicode karakterláncként definiált érték a következőkből áll:
* 4 bájt hosszúságú mező, amely a karakterláncban lévő karakterek számát jelzi (nem bájtokat).
* Unicode-értékek karakterlánca, karakterenként két bájt.

### Fájlfejléc ###

A fájl fejléce tartalmazza a kép alapvető tulajdonságait.

|Hosszú|Leírás
---|---|
|4|Aláírás: mindig egyenlő: '8BPS' . Ne próbálja meg beolvasni a fájlt, ha az aláírás nem egyezik ezzel az értékkel.
|2|Verzió: mindig egyenlő 1-gyel. Ne próbálja meg beolvasni a fájlt, ha a verzió nem egyezik ezzel az értékkel. (~*~*PSB~*~* verzió a 2.)
|6|Fenntartva: nullának kell lennie.
|2|A képen látható csatornák száma, beleértve az alfa-csatornákat. A támogatott tartomány 1 és 56 között van.
|4|A kép magassága pixelben. A támogatott tartomány 1 és 30 000 között van.
|4|A kép szélessége pixelben. A támogatott tartomány 1 és 30 000 között van.
|2|Mélység: a bitek száma csatornánként. A támogatott értékek az 1, 8, 16 és 32.
|2|A fájl színmódja. A támogatott értékek a következők: Bitmap # 0; Szürkeárnyalatos # 1; Indexelt # 2; RGB # 3; CMYK # 4; Többcsatornás # 7; Duotone # 8; 9. labor.

### Színmód adatszakasz ###

A színmód adatrész a következőképpen épül fel:


|Hosszú|Leírás
---|---|
|4|A következő színadatok hossza
|változó|A színadatok

A színmód adatai csak a Fájlfejléc szakasz módmezőjében meghatározott indexelt színekhez és duótónusokhoz érhetők el. Az összes többi mód esetében ezt a szakaszt 4 bájtos nullázott értékek képviselik. Indexelt színes képek esetén a hossz 768, és a színadatok a kép színtáblázatát tartalmazzák, nem átlapolt sorrendben. A Duotone képek esetében a színadatok tartalmazzák a duoton specifikációt (amelynek formátuma nincs dokumentálva). Más alkalmazások, amelyek olvasnak Photoshop fájlokat, képesek a kéttónusú képet szürke képként kezelni, és a fájl olvasása és írása során csak megőrzik a kéttónusú információkat.

### Képforrások szakasz ###

A fájl harmadik része képforrásokat tartalmaz. Egy hosszúságú mezővel kezdődik, amelyet egy sor erőforrásblokk követ.


|Hosszú|Leírás
---|---|
|4|A képforrás szakasz hossza. A hossza nulla lehet.
|Változó|Képforrások (Képerőforrás-blokkok)

A képforrások a képekkel társított nem képpontos adatok tárolására szolgálnak, például a toll eszközútvonalai. Erőforrásblokkoknak nevezik őket, mert olyan adatokat tartalmaznak, amelyeket a Photoshop korai verzióiban a Macintosh erőforrásában tároltak. A kép-erőforrás blokkok alapvető felépítése a következő:


|Hosszú|Leírás
---|---|
|4|Aláírás: '8BIM'
|2|Az erőforrás egyedi azonosítója. A kép-erőforrás-azonosítók a Photoshop által használt erőforrás-azonosítók listáját tartalmazzák.
|Változó|Név: Pascal karakterlánc, kitömve, hogy a méret egyenletes legyen (a null név két 0 bájtból áll)
|4|A következő erőforrásadatok tényleges mérete
|Változó|Az erőforrásadatok, az egyes erőforrástípusokról szóló szakaszokban leírtak szerint. Párnázott, hogy a mérete egyenletes legyen.

A képforrások több szabványos azonosítószámot használnak.

### Réteg- és maszkinformáció ###

A Photoshop-fájl negyedik része a rétegekről és maszkokról tartalmaz információkat, például a rétegek számát, a rétegekben lévő csatornákat, a keverési tartományokat, a korrekciós réteg gombjait, az effektusrétegeket és a maszk paramétereit. Ha nincsenek rétegek vagy maszkok, ezt a szakaszt egy nullázott 4 bájtos mező képviseli. Különös figyelmet kell fordítani a szakaszok hosszára a szakasz olvasása során a nullázott értékek miatt. A réteg és maszk rész elrendezése a következő:


|Hosszú|Leírás
---|---|
|4|A réteg és a maszk információs szakaszának hossza. (A PSB hossza 8 bájt.)
|Változó|Réteg információ
|Változó|Globális rétegmaszk információ
|Variable|Cimkézett blokkok sorozata, amelyek különféle típusú adatokat tartalmaznak.

#### Réteg információ ####

A következő táblázat a réteginformációk magas szintű szervezését mutatja be.


|Hosszú|Leírás
---|---|
|4|A réteg információs szakaszának hossza, 2 többszörösére kerekítve. (A PSB hossza 8 bájt.)
|2|Rétegszám. Ha ez negatív szám, akkor abszolút értéke a rétegek száma, és az első alfa csatorna tartalmazza az összevont eredmény átlátszósági adatait.
|Változó|Információ az egyes rétegekről. A Rétegrekordok című rész leírja ezen információk felépítését az egyes rétegekre vonatkozóan.
|Változó|Csatorna képadatok. Minden réteghez egy vagy több képadatrekordot tartalmaz. A rétegek ugyanabban a sorrendben vannak, mint a réteginformációban

### Képadatok ###

A képpontok adatait a fájl Képadatok része tartalmazza. Az adatok elrendezése az Image Data részben síkbeli sorrendben történik, azaz először az összes piros adatot, majd az összes zöld adatot stb. Minden sík letapogatási sorrendben kerül tárolásra, pad bájtok nélkül. A képadatok szakasz formátumban van elrendezve. az alábbi táblázat szerint.

|Hosszú|Leírás
---|---|
|2|Tömörítési módszer: *0 = Nyers képadatok * 1 = RLE tömörítés A képadatok az összes letapogatási sor (sorok * csatornák) bájtszámával kezdődnek, és minden egyes szám két bájtos értékként kerül tárolásra. Az RLE tömörített adatok következnek, minden egyes letapogatási sor külön-külön tömörítve. Az RLE-tömörítés ugyanaz a tömörítési algoritmus, amelyet a Macintosh ROM-rutin PackBits és a TIFF-szabvány is használ. *2 = ZIP előrejelzés nélkül *3 = ZIP előrejelzéssel.
|Változó|A képadatok. Síkrend = RRR GGG BBB stb.

## Hivatkozások ##

* [PSD fájlformátum specifikációi – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Adobe Photoshop fájlformátum](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

