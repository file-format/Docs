{
  "date" : "2021-08-31",
  "keywords" :[ "xbe fájl", "xbe fájlformátum", "mi az xbe fájl", "fájl", "xbe példa", "xbe fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az XBE fájlformátumról és az API-król, amelyek XBE fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"XBE - iOS alkalmazáscsomag fájl",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Mi az XBE fájl?
Az .xbe kiterjesztésű fájl egy Xbox videojáték-lemezről futtatható alkalmazás. Az XBE fájlok az Xbox rendszerben végrehajtott fő fájlok, és általában nem szabad megnyitni őket számítógépen, de PC-n Xbox emulációs program segítségével megnyithatók. Ezeket a fájlokat általában játékfejlesztők hozzák létre, majd a Microsoft aláírja őket. A fájl szerkezete hasonló a Windows PE fájljaihoz, de néhány fontos változtatás az XBox beállításai szerint történik, hogy futtatható legyen az XBoxon.

## XBE fájlformátum
Az XBE fájl képfejlécből, szakaszfejlécek gyűjteményéből, tanúsítványból, szál helyi tárolási adataiból, könyvtárverziók gyűjteményéből, Microsoft bittérképből, valamint a kódot és az erőforrásokat tartalmazó szakaszokból áll.

### Képfejléc
A képfejléc tartalmazza azokat az információkat, amelyek elmagyarázzák, hogy a végrehajtható fájl többi összetevője hol található a fájlban, és hogyan kell a futtatható fájlt kezelni és betölteni.

### TLS-tábla
A TLS-tábla minden olyan információt tartalmaz, amelyre az XBE-nek szüksége van a szálhelyi tároló megfelelő beállításához. Alapvetően egyedi a PE32 fájlokban található TLS-könyvtárban, és onnan közvetlenül másolható. Ez a táblázat elhagyható, ha az XBE fájl nem használ szálhelyi tárolót, és a képfejléc megfelelő mezője nullára van állítva.

| Offset | Méret | Név | Leírás |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Nyers adatok indítása | Abszolút (azaz nem RVA) cím a programkép TLS változóadatainak kezdőpontjában. |
| 0x0004 | 0x0004 | Nyers adatok vége | Abszolút (azaz nem RVA) cím a programkép TLS-változóadatainak végének. |
| 0x0008 | 0x0004 | Az index címe | A TLS Index változó abszolút (azaz nem RVA) címe. |
| 0x000C | 0x0004 | A visszahívások címe | A null-végződésű TLS visszahívási függvénytáblázat abszolút (azaz nem RVA) címe. |
| 0x0010 | 0x0004 | Nulla kitöltés mérete | A nyers adatokat követő bájtok száma, amelyeket nullára kell állítani a memóriában. |
| 0x0014 | 0x0004 | Jellemzők | Leírja az igazítást. |

### Tanúsítvány

Egy tanúsítvány kötelező minden Xbox futtatható fájlhoz, amely információkat tartalmaz a címekről:
 


- A tanúsítvány létrehozásának időpontja és dátuma
- Címazonosító
- Cím neve
- Alternatív címazonosítók
- Engedélyezett médiatípusok, amelyekről a futtatható fájl futtatható (HD, DVD, CD stb.)
- Játék régió
- Játék értékelések
- Lemezszám
- Verzió
- A System Linkhez használt LAN kulcs nyers adatok
- Aláírási kulcs nyers adatok (a mentési játékok aláírására használják)
- Alternatív aláírási kulcsok
- A tanúsítvány eredeti mérete
- Online szolgáltatás neve (nem szerepel a korai futtatható fájlokban)
- Futási idejű biztonsági jelzők (nem jelennek meg a korai végrehajtható fájlokban)
 


### Engedélyezett médiatípusok
Médiatípusok, amelyekről a futtatható fájl futtatható. A következő értékek ismertek:
| Médiatípus | Érték |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Szakaszok
A szakaszokat a szakaszfejlécek fejezik ki. A szakaszfejlécek közvetlenül a tanúsítvány után kezdődnek, és információkat tartalmaznak arról, hogy a fájlban hol találhatók a tényleges szakaszok. Legalább két szakasz mindig jelen van egy Xbox futtatható fájlban:


- .szöveg


- .rdata


## Hivatkozások



* [Xbe – XBox Executable](https://xboxdevwiki.net/Xbe)


