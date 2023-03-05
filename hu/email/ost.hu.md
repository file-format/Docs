{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook Storage File Format",
  "description":"További információ az OST fájlformátumról és az API-król, amelyek OST fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az OST fájl?

Az OST vagy Offline Storage Files a felhasználó postafiók-adatait képviseli offline módban a helyi gépen, amikor regisztrált az Exchange Server-re a Microsoft Outlook használatával. A Microsoft Outlook első használatakor automatikusan létrejön, amikor csatlakozik a szerverhez. A fájl létrehozása után az adatok szinkronizálódnak az e-mail szerverrel, így offline állapotban is elérhetők lesznek, ha megszakad az e-mail szervertől. Az OST-fájlok a postafiók elemeit, például e-maileket, névjegyeket, naptárinformációkat, jegyzeteket, feladatokat és más hasonló adatokat használhatnak fel. A felhasználók a szerverrel való kapcsolat hiányában is létrehozhatnak e-maileket és egyéb adatelemeket OST fájlban, de ezek nem lesznek szinkronizálva a szerverrel. A kapcsolat létrejötte után a helyi fájl ismét szinkronizálásra kerül a szerverrel, így a szerver és a helyi másolat azonos információszinten van.

## OST fájlformátum

Az OST (Offline Storage Table) és a [PST](/hu/email/pst/) (Personal Storage Table) fájlformátum a személyes mappafájl (PFF) formátumból áll, amely megfelel a felhasználói e-mailek, névjegyek és találkozók tárolásának. A PFF-fájlban lévő adatok kis-végi formában vannak tárolva, az összes dátumot és időpontot FILETIME-ként ábrázolva UTC-ben. Az [MS-PST] kétféle PFF-et határoz meg:

* 32 bites ANSI formátum
* 64 bites Unicode formátum

A Microsofttól elérhető PST-fájlformátum [specifikáció](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) az OST-fájlformátumra is alkalmazható ingyenes és visszavonhatatlan szabadalmi licensz az Open Specification Promise révén. A következő megkülönböztethető elemekből áll:

* Fle fejléc
* Fájlfejléc adatok
* Index ág csomópont
* Index levél csomópont
* (Fájl) eltolási index
* (Tétel) leíró index
* Helyi leírók
* Cikktáblázat típusa

### Fejléc információ

Az OST fájl HEADER szerkezete a fájl legelején található 0 eltolásnál. Metaadat-információkat tartalmaz az OST fájlról és a ROOT információkat a fent leírt NDB Layer adatstruktúrák eléréséhez. A HEADER szerkezete eltér az OST fájlformátum Unicode és ANSI verzióiban.

A fejléc egy 4 bájtos varázsszóval kezdődik **!BDN**, amelyet bájtok képviselnek (0x21, 0x42, 0x44, 0x4E). Egy másik 2 bájtos mágikus szám, a **SM** (0x53, 0x4D) a fájl kezdetétől számított 8-as eltolásnál található. A verzióinformáció (ANSI vagy Unicode) a fájl elejétől számított 10-es eltolásban található. A hexadecimális érték (0x17) az Unicode OST fájlt adja meg, míg a 0x0E vagy 0x0F az ANSI fájlformátumot jelenti.

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
|bidUnused (csak 8 bájtos Unicode)|A Unicode PST-fájlformátum létrehozásakor hozzáadásra került a nem használt kitöltés.
|bidNextP (Unicode: 8 bájt; ANSI: 4 bájt)|Következő oldal BID. Az oldalakon egy speciális számláló található a bidIndex értékek kiosztására. Az oldalak BID-jeinek bidIndex értéke ebből a számlálóból kerül kiosztásra.
|bidNextB (csak 4 bájtos ANSI): |Next BID. Ez az érték a monoton számláló, amely a következő kiosztott blokkhoz hozzárendelendő BID-t jelzi. A BID értékek 4-es lépésekben haladnak előre. További részletekért lásd a 2.2.2.2. szakaszt.
|dwUnique (4 bájt)|Ez egy monotonan növekvő érték, amely minden alkalommal módosul, amikor a PST-fájl HEADER szerkezete módosul. Ennek az értéknek az a feladata, hogy egyedi értéket adjon, és biztosítsa, hogy a HEADER CRC-k minden fejlécmódosítás után eltérőek legyenek.
|rgnid[](128 bájt)|Rögzített tömb 32 NID-ből, amelyek mindegyike megfelel a 32 lehetséges NID_TYPE egyikének (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_MESSAGE_)
|qwUnused (8 bájt)|Felhasználatlan terület; nullára KELL állítani. Csak Unicode PST fájlformátum.
|root (Unicode: 72 bájt; ANSI: 40 bájt)|ROOT struktúra (2.2.2.5. szakasz).
|dwAlign (4 bájt)|Fel nem használt igazítási bájtok; nullára KELL állítani. Csak Unicode PST fájlformátum.
|rgbFM (128 bájt)|Elavult FMap. Ezt már nem használják, és 0xFF-el KELL kitölteni. Az olvasóknak figyelmen kívül KELL hagyniuk ezeknek a bájtoknak az értékét.
|rgbFP (128 bájt)|Elavult FPMap. Ezt már nem használják, és 0xFF-el KELL kitölteni. Az olvasóknak figyelmen kívül KELL hagyniuk ezeknek a bájtoknak az értékét.
|bSentinel (1 bájt) | 0x80-ra KELL állítani.
|bCryptMethod (1 bájt)|Azt jelzi, hogy a PST-fájlban lévő adatok hogyan vannak kódolva. Az előre meghatározott értékek egyikére KELL állítani (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbFenntartva (2 bájt)| Fenntartott; nullára KELL állítani.
|bidNextB (8 bájt)|A következő elérhető BID értéket jelzi. Csak Unicode PST fájlformátum.
|bidNextB (CSAK Unicode: 8 bájt)|Következő BID. Ez az érték a monoton számláló, amely a következő kiosztott blokkhoz hozzárendelendő BID-t jelzi. A BID értékek 4-es lépésekben haladnak előre. További részletekért lásd a 2.2.2.2. szakaszt.
|dwCRCFull (4 bájt)|A wMagicClienttől a bidNextB-ig terjedő 516 bájtnyi adat 32 bites CRC értéke. Csak Unicode PST fájlformátum.
|ullReserved (8 bájt)|Fenntartva; nullára KELL állítani. Csak ANSI PST fájlformátum.
|dwReserved (4 bájt)|Fenntartva; nullára KELL állítani. Csak ANSI PST fájlformátum.
|rgbFenntartva2 (3 bájt)|
|bFenntartva (1 bájt) |
|rgbReserved3 (32 bájt) |

## Hivatkozások

* [Outlook Personal Folders (.ost) fájlformátum](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [A személyes mappa fájlformátumának specifikációi](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

