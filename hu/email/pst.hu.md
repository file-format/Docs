{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Personal Information Store fájlformátum",
  "description":"További információ a PST-fájlformátumról és az API-król, amelyek PST-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PST fájl?

A .pst kiterjesztésű fájlok az Outlook Personal Storage Files (más néven Personal Storage Table) fájlok, amelyek különféle felhasználói információkat tárolnak. A felhasználói információkat különböző típusú mappákban tárolják, amelyek e-maileket, naptárelemeket, jegyzeteket, névjegyeket és számos más fájlformátumot tartalmaznak. A PST-fájlok offline e-mail-adatok archiválására szolgálnak, amelyek később betölthetők és megtekinthetők különböző alkalmazásokban.

## A PST fájlformátum specifikációi

A PST-fájlformátum [specifikációi](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) ingyenes és visszavonhatatlan ingyenes szabadalmi licencként érhető el a Microsofttól az Open Specification Promise keretében .

### A PST-formátumok típusa

A PST fájlformátumok két típusba sorolhatók a fájltípus kódolása alapján. Az ANSI-kódolású PST-fájlok régebbi fájlformátumok, és csak az Outlook 2002 és a korábbi verziók támogatják őket. Az ilyen fájlok maximális mérete 2 GB (2^^31^^ bájt), és nem támogatja a Unicode-ot. Egy modernebb, Unicode kódoláson alapuló fájlformátum eltávolítja a fájlméret-korlátozást, és elérheti az 50 GB-os maximális adatméretet.

### A PST-fájlformátum logikai felépítése

A PST fájlformátum alapja a B-Tree, amely az adatokat rendezve tartja, és lehetővé teszi a keresést, a szekvenciális hozzáférést, a beszúrásokat, törléseket stb. logaritmikus időben. A PST-fájlok általános szerkezete három rétegben van elrendezve.

![Logical layers of a PST file](/hu/email/PST-1.png "Logical layers of a PST file")

"Csomópont-adatbázis (NDB) Layer" - A csomóponti adatbázis-réteg a PST-fájl alsó szintjén található, és a csomópontok adatbázisát tartalmazza. Ezek a csomópontok valójában a PST fájlformátum alacsonyabb szintű tárolóhelyeit képviselik. Az NDB réteg fejlécekből, fájlallokációs információkból, blokkokból és BT-fákból (Node BTree és Block BTree) áll tárolási szempontból. Az NDB-réteg csomópontjai és blokkjai a Data BID-n keresztül kapcsolódnak össze, amely a csomópont-hivatkozás négy tulajdonságának egyike, azaz NID (csomópont-azonosító), szülő-NID, adat-BID (Block BID) és alcsomópont-BID.

Listák, táblázatok és tulajdonságok rétege - Az LTP-réteg az NDB-n felül a magasabb szintű fogalmak logikai megértését biztosítja. Az LTP réteg a többi elem mellett főként Property Context (PC) és Table Context (TC) elemekből áll. A PC a tulajdonságok gyűjteménye, míg a TC a tulajdonságok gyűjteményének kétdimenziós mátrixa és ezek jelenléte. A PC-k és TC-k hatékony megvalósítása, az LTP-réteg a következő kétféle adatstruktúrát használja az NDB csomóponton:

* Heap On Node (HN) – lehetővé teszi egy csomópont adatfolyamának kis, változó méretű töredékekre történő továbbosztását.
* BTree on Heap (BTH) – A BTH kényelmes és praktikus módot biztosít az adat PC-k közötti kereséshez, a fent leírtak BTH-ként vannak megvalósítva, ezért valósítják meg egy HN struktúrán belüli beépítéssel.

`Üzenetküldő réteg -` Magasabb szintű szabályok és üzleti logika a PST-fájlokkal való munkavégzéshez ezen a rétegen valósul meg. Ennek a rétegnek a logikai kimenete mappaobjektumok, üzenetobjektumok, mellékletobjektumok és tulajdonságok formájában jelenik meg, amelyet az LTP és NDB rétegek kombinálása tesz lehetővé. A PST-tartalom módosítása során betartandó szabályok és követelmények szintén ezen a rétegen vannak meghatározva.

### A PST-fájlformátum fizikai felépítése

A PST-fájlok magas szintű fájlszervezése az alábbi ábrán látható. Ez csak egy áttekintés a különböző fogalmakról a PST-fájl logikai elemeiből.

![Physical organization of the PST file format](/hu/email/PST-2.png "Physical organization of the PST file format")


#### PST fejléc információ

A PST-fájl HEADER szerkezete a fájl legelején található 0 eltolásnál. Metaadat-információkat tartalmaz a PST-fájlról és a ROOT-információkat a fent leírt NDB-réteg adatszerkezetek eléréséhez. A HEADER szerkezete eltér a PST fájlformátum Unicode és ANSI verzióiban.

A fejléc egy 4 bájtos varázsszóval kezdődik **!BDN**, amelyet bájtok képviselnek (0x21, 0x42, 0x44, 0x4E). Egy másik 2 bájtos mágikus szám, a **SM** (0x53, 0x4D) a fájl kezdetétől számított 8-as eltolásnál található. A verzióinformáció (ANSI vagy Unicode) a fájl elejétől számított 10-es eltolásban található. A hexadecimális érték (0x17) a Unicode PST-fájlt adja meg, míg a 0x0E vagy a 0x0F az ANSI fájlformátumot jelenti.

|Mező|Leírás
---|---|
|dwMagic (4 bájt)|A következőnek KELL lennie: "{0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bájt)|A 471 bájtnyi adat 32 bites CRC értéke a wMagicClienttől kezdve (0ffset 0x0008)
|wMagicClient (2 bájt)|KELL lennie "{ 0x53, 0x4D }".
|wVer (2 bájt)|Fájlformátumú verzió. Ennek az értéknek 14-nek vagy 15-nek KELL lennie, ha a fájl ANSI PST-fájl, és 23-nak KELL lennie, ha a fájl Unicode PST-fájl.
|wVerClient (2 bájt)|Kliens fájlformátumú verziója. A dokumentumban leírt formátumnak megfelelő verzió a 19. Az ezen a dokumentumon alapuló új PST-fájl létrehozóinak ezt az értéket 19-re KELL inicializálniuk.
|bPlatformCreate (1 bájt)|Ezt az értéket 0x01-re KELL állítani.
|bPlatformAccess (1 bájt)|Ezt az értéket 0x01-re KELL állítani.
|dwReserved (8 bájt)|
|bidUnused (csak 8 bájtos Unicode)|A Unicode PST fájlformátum létrehozásakor hozzáadásra került a nem használt kitöltés.
|bidNextP (Unicode: 8 bájt; ANSI: 4 bájt)|Következő oldal BID. Az oldalakon egy speciális számláló található a bidIndex értékek kiosztására. Az oldalak BID-jeinek bidIndex értéke ebből a számlálóból kerül kiosztásra.
|bidNextB (csak 4 bájtos ANSI): |Next BID. Ez az érték a monoton számláló, amely a következő kiosztott blokkhoz hozzárendelendő BID-t jelzi. A BID értékek 4-es lépésekben haladnak előre. További részletekért lásd a 2.2.2.2. szakaszt.
|dwUnique (4 bájt)|Ez egy monotonan növekvő érték, amely minden alkalommal módosul, amikor a PST-fájl HEADER szerkezete módosul. Ennek az értéknek az a feladata, hogy egyedi értéket adjon, és biztosítsa, hogy a HEADER CRC-k minden fejlécmódosítás után eltérőek legyenek.
|rgnid[]   (128 bájt)|Rögzített tömb 32 NID-ből, amelyek mindegyike megfelel a 32 lehetséges NID_TYPE egyikének (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_MESSAGE_)
|qwUnused (8 bájt)|Felhasználatlan terület; nullára KELL állítani. Csak Unicode PST fájlformátum.
|root (Unicode: 72 bájt; ANSI: 40 bájt)|ROOT struktúra (2.2.2.5. szakasz).
|dwAlign (4 bájt)|Fel nem használt igazítási bájtok; nullára KELL állítani. Csak Unicode PST fájlformátum.
|rgbFM (128 bájt)|Elavult FMap. Ezt már nem használják, és 0xFF-el KELL kitölteni. Az olvasóknak figyelmen kívül KELL hagyniuk ezeknek a bájtoknak az értékét.
|rgbFP (128 bájt)|Elavult FPMap. Ezt már nem használják, és 0xFF-el KELL kitölteni. Az olvasóknak figyelmen kívül KELL hagyniuk ezeknek a bájtoknak az értékét.
|bSentinel (1 bájt) | 0x80-ra KELL állítani.
|bCryptMethod (1 bájt)|Azt jelzi, hogy a PST-fájlban lévő adatok hogyan vannak kódolva. Az előre meghatározott értékek egyikére KELL állítani (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbFenntartva (2 bájt)| Fenntartott; nullára KELL állítani.
|bidNextB (8 bájt)|A következő elérhető BID értéket jelzi. Csak Unicode PST fájlformátum.
|bidNextB (CSAK Unicode: 8 bájt)|Next BID. Ez az érték a monoton számláló, amely a következő kiosztott blokkhoz hozzárendelendő BID-t jelzi. A BID értékek 4-es lépésekben haladnak előre. További részletekért lásd a 2.2.2.2. szakaszt.
|dwCRCFull (4 bájt)|A wMagicClienttől a bidNextB-ig terjedő 516 bájtnyi adat 32 bites CRC értéke. Csak Unicode PST fájlformátum.
|ullReserved (8 bájt)|Fenntartva; nullára KELL állítani. Csak ANSI PST fájlformátum.
|dwReserved (4 bájt)|Fenntartva; nullára KELL állítani. Csak ANSI PST fájlformátum.
|rgbFenntartva2 (3 bájt)|
|bFenntartva (1 bájt) |
|rgbReserved3 (32 bájt) |

### Adat védelem ###

A biztonság kedvéért a PST-fájlok jelszóval is védhetők, amihez a betöltő alkalmazásnak jelszót kell alkalmaznia a megtekintés előtt. A PST-fájlhoz alkalmazott jelszó az üzenettárolóban tárolódik. Ez azonban nem biztosít erős adatvédelmet, mivel a jelszó a rendelkezésre álló eszközökkel eltávolítható. Ezenkívül a felhasználó által megadott jelszó nem szerepel a kódolási és dekódoló titkosítási algoritmusok kulcsában. Így semmi haszna nincs a jogosulatlan felek által hozzáférhetõ adatok védelmének. A jelszó tárolása az eredeti karakterlánc CRC-32 hash-jeként szintén gyenge adatvédelmi módszert jelent a brute force megközelítéssel szemben.

## Hivatkozások ##

* [Outlook Personal Folders (.pst) fájlformátum](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [A személyes mappa fájlformátumának specifikációi](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

