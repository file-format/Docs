{
  "date" : "2019-10-11",
  "keywords" :[ "tar fájl", "tar fájlformátum", "mi az a tar fájl", "fájl", "tar példa", "tar fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix archív fájlformátum",
  "description":"További információ arról, hogy mi az a Tar-fájl és az API-k, amelyek TAR-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TAR fájl?

A .tar kiterjesztésű fájlok Unix-alapú segédprogrammal létrehozott archívumok egy vagy több fájl összegyűjtésére. A rendszer több fájlt tömörítetlen formátumban tárol, és támogatja a fájlok és mappák archívumhoz való hozzáadását. A Unix TAR segédprogramja Command alapú, de az így létrehozott fájlokat a legtöbb fájlarchiváló rendszer szinte minden operációs rendszeren támogatja. Először 1979-ben hozta létre az AT&T Bell Laboratories, majd az idő múlásával a későbbi verziók is megjelentek.

## TAR fájlformátum

A TAR egy nyílt fájlformátum, amelynek teljes specifikációja elérhető a fejlesztők számára. Fájlszerkezetét a POSIX.1-1988-ban, majd később a POSIX.1-2001-ben szabványosították. A tar által létrehozott adatkészletek megőrzik a fájlrendszer paramétereiről szóló információkat, például:

* Név
* Időbélyegek
* Tulajdonjog
* Fájlhozzáférési engedélyek
* Directory Szervezet

A Tar fájlnak nincs varázsszáma. Egy sor blokkot tartalmaz, ahol minden blokk BLOCKSIZE bájtból áll.

Minden archivált fájlt egy fejléc blokk képvisel, amely leírja a fájlt, amit nulla vagy több blokk követ, amelyek megadják a fájl tartalmát. Az archív fájl végén két 512 bájtos blokk található, amelyek bináris nullákkal vannak feltöltve, mint fájlvégi jelző. Egy ésszerű rendszernek ilyen fájlvégjelzőt kell írnia az archívum végére, de nem szabad feltételeznie, hogy ilyen blokk létezik az archívum olvasása során. Különösen a GNU tar mindig figyelmeztet, ha nem találkozik vele.

A blokkok blokkolhatók a fizikai I/O műveletekhez. Minden n blokkból álló rekord (ahol az n-t a blocking-factor = 512-size opció tar-ra állítja) egyetlen "write()" művelettel íródnak. A mágnesszalagokon az ilyen írás eredménye egyetlen rekord. Archívum írásakor a blokkok utolsó rekordját teljes méretben kell megírni, a nulla blokk utáni blokkokkal pedig az összes nullát tartalmaz. Archívum olvasásakor egy ésszerű rendszernek megfelelően kell kezelnie azt az archívumot, amelynek utolsó rekordja rövidebb, mint a többi, vagy amely egy nulla blokk után szemetes rekordokat tartalmaz.

### Tar fejléc

A többi fájlfejléchez hasonlóan a tar fájlfejléc rekord metaadatokat tartalmaz egy fájlról, és az alábbi táblázatban látható.


|Mezőeltolás|Mezőméret (Bájt)|Mező
---|---|---|
|0|100|Fájlnév
|100|8|Fájl mód
|108|8|A tulajdonos numerikus felhasználói azonosítója
|116|8|A csoport numerikus felhasználói azonosítója
|124|12|Fájlméret bájtban (oktális alap)
|136|12|Utolsó módosítás ideje numerikus Unix időformátumban (oktális)
|148|8|A fejlécrekord ellenőrző összege
|156|1|Link jelző (fájltípus)
|157|100|A hivatkozott fájl neve

A fel nem használt mezők NUL bájttal vannak kitöltve. A fejléc 257 bájtból áll, amelyet NUL bájtokkal töltenek ki, hogy 512 bájtos rekordra töltsék ki.

## Referenciák ##

* [TAR – a Wikipedia által](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR alapformátum](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

