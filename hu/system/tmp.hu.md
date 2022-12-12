{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "kiterjesztés", "fájl", "formátum", "rendszer", "TMP-fájl", "TMP-dokumentumok", "TMP-fájlok", "ideiglenes fájl", "alkalmazás", "programok" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Ideiglenes fájlformátum",
  "description":"További információ a TMP fájlformátumról és az API-król, amelyek TMP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Mi az a TMP fájl? ##

A TMP-fájl egy szoftverprogram által létrehozott átmeneti biztonsági mentésre, tárolásra vagy más fájlrendszerre utal. Időnként láthatatlan fájlként jön létre, és gyakran megsemmisül a program bezárásakor. A TMP-fájlok felhasználhatók ideiglenes információk tárolására is, amíg egy új fájl készül.

## TMP fájlformátum ##

A TMP-fájl jellemzően nyers adatokból áll, amelyeket az anyagok egyik stílusból a másikba való átalakítási folyamatában használnak fel. A Microsoft Word és az Apple Safari két olyan alkalmazás, amely képes létrehozni és használni a TMP fájlformátumot.

A létrehozott TMP dokumentumokat elméletileg automatikusan el kell távolítani a program bezárásakor vagy a gép kikapcsolásakor. A gyakorlatban ez nem mindig van így. Ennek eredményeként, miközben a program dokumentumai között navigál, olyan átmeneti fájlokkal találkozhat, amelyeket a rendszer vagy más szoftver nem használ aktívan.

### Segéd memória ###

A virtuális memóriát operációs rendszerek használják, azonban a hatalmas mennyiségű információt felhasználó programoknak szükségük lehet ideiglenes dokumentumok létrehozására.

### Folyamatközi kommunikáció ###

A legtöbb operációs rendszer primitíveket biztosít a programok közötti adatátvitelhez, mint például a csövek, aljzatok vagy a fő memória, de a legegyszerűbb módszer a fájlok ideiglenes fájlba való átvitele, és a fogadó alkalmazásnak az ideiglenes fájl helyének tájékoztatása.


## Műszaki specifikáció ##

A megkülönböztető ideiglenes dokumentumnevek beszerzését általában operációs rendszerek és szoftverprogramok biztosítják.
Ideiglenes fájlok biztonságosan generálhatók POSIX rendszereken az mkstemp vagy tmpfile függvénytár funkcióval. Egyes rendszerek tartalmazzák a korábbi POSIX (mióta megszűnt) mktemp alkalmazást. Ezek a fájlok általában a szokásos ideiglenes könyvtárban találhatók Unix platformon a /TMP-ben, vagy a %TEMP%-ban (ez kifejezetten a bejelentkezésre vonatkozik) Windows-gépeken.

Amikor a program leáll vagy a dokumentum bezárul, a tmpfile-lel generált átmeneti fájl automatikusan törlődik. A GetTempFileName (Windows) vagy a tmpnam (POSIX) segítségével létrehozhat egy ideiglenes fájlnevet, amely hosszabb ideig tart, mint az azt létrehozó program.

## Hivatkozási szám

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
