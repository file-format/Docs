{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz fájl", "usdz fájlformátum", "fájlformátum", "3d", "usdz fájl letöltése"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ – univerzális jelenetleíró ZIP formátum",
  "description":"További információ az USDZ fájlformátumról és az USDZ-fájlok megnyitására és létrehozására alkalmas API-król.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Mi az az USDZ fájl?

Az .usdz formátumú fájl egy tömörítetlen és titkosítás nélküli ZIP-archívum az [USD](/hu/3d/usd/) (Universal Scene Description) fájlformátumhoz, amely más formátumú fájlokat (például textúrákat és animációkat) tartalmaz, valamint a beágyazott proxykat tartalmazza. az archívumot, és közvetlenül futtatja őket az USD futási idővel, kicsomagolás nélkül. Az USDZ fájlok olyan csomagok, amelyek kialakítása egy csomag új Ar-szintű absztrakcióján alapul. Az Usdz-t az IANA regisztrálta, és a modell médiatípus-nevével, valamint a vnd.usd+zip altípusnévvel rendelkezik, részletei pedig az [IANA regisztrációs oldalán](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ fájlformátum

Az USDZ-fájlok a ZIP-fájlformátumon alapulnak, amelyek az egyes fájlokat a tárolójában archiválják. Ez lehetővé teszi, hogy a vevőoldal egyszerűen kicsomagolja a tartalmat, és a normál USD jelenetleíró fájlokat használja a munkához és az ellenőrzéshez. Szinte minden operációs rendszer beépített támogatást nyújt a ZIP fájlformátumokhoz, és ha ezt az archiválási formátumot választja bármely egyéni módszer helyett, az USDZ fájlok egyszerű szállítási protokollként használhatók.

### ZIP megkötések

Az USDZ fájlformátum a ZIP fájlformátumot használja "tömörítés" és "titkosítás" nélkül. Ennek célja a tervezés két követelménynek volt megfelelni:

* A memóriába már betöltött csomagok esetén vagy egyetlen fájlként a lemezen az API USD-ben érhető el a képen belüli adatok eléréséhez
* Nincs szükség a fájlok lemezre történő kibontására vagy több halom tárhely lefoglalására

Az USDZ esetében mindkét követelmény teljesül, mivel a legtöbb képformátum önmagában is lehetővé teszi a belső tömörítési sémákat, ami kompakt fájlméretet eredményez.

### Elrendezési követelmények

Az USDZ csomagok megkövetelik a fájlok csomagon belüli elrendezését, hogy az egyes fájlok adatainak a csomag elejétől számított 64 bájt többszörösével kell kezdődniük. A csomagnak azonban egy natív [USD](/hu/3d/usd/) fájllal kell kezdődnie, ha a csomagot egyszerű hivatkozással célozzuk meg. Ebben az esetben az első USD-fájlt alapértelmezett rétegnek nevezzük. Azok az ügyfelek, akik "streamelhető tartalmat" szeretnének szállítani, érdemes más elrendezési korlátokat is figyelembe venni.

## USDZ fájl letöltése
Mivel az usdz fájlok más kiváló minőségű képekkel és usd fájlokkal vannak tele, nagyobb lemeztárhelyet foglalhatnak el. Itt egy egyszerű és kisebb USDZ példafájlt talál letöltésre:

- [Sample.usdz](../sample.usdz)

## Hivatkozások

* [USDZ fájlformátum specifikációi](https://openusd.org/release/spec_usdz.html)
