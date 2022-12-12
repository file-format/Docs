{
  "date" : "2021-06-14",
  "keywords" :[ "NAPLÓ", "kiterjesztés", "naplófájl", "naplófájl formátum", "adatbázisfájl típusa", "adatbázisfájl formátum", "mi az a naplófájl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a LOG fájlformátumról és az API-król, amelyek LOG fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"NAPLÓ - naplófájl formátum",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Mi az a LOG fájl?
A .log kiterjesztésű fájl az egyszerű szövegek listáját tartalmazza időbélyeggel. Általában bizonyos tevékenységek részleteit a szoftverek vagy operációs rendszerek naplózzák, hogy segítsenek a fejlesztőknek vagy a felhasználóknak nyomon követni, mi történik egy adott időszakban. A felhasználók könnyen szerkeszthetik ezeket a fájlokat bármilyen szövegszerkesztővel. Általában a hibajelentéseket vagy a bejelentkezési tevékenységeket az operációs rendszer naplózza, de más szoftverek vagy webszerverek is generálnak naplófájlokat a látogatók nyomon követésére és a sávszélesség-használat figyelésére.

## LOG fájl formátum
A LOG fájlformátum rögzíti az operációs rendszerben előforduló tipikus eseményeket, a kommunikációs szoftverek különböző felhasználói közötti üzeneteket vagy bármely más szoftver futtatását. Egyszerűen azt mondhatjuk, hogy bizonyos üzenetek bizonyos időbélyegekkel egy LOG fájlba kerülnek naplózásra. Néhány gyakran használt kifejezés a naplózásra:
### Eseménynaplók
Rögzíti a rendszer végrehajtása során bekövetkezett eseményeket, hogy nyomon kövesse és megértse a rendszer tevékenységét, valamint diagnosztizálja a problémákat. Fontosak az összetett rendszerek tevékenységeinek azonosításában, jellemzően a nagyon kevés felhasználói interakciót igénylő alkalmazások esetében.
### Tranzakciós naplók
Szinte minden adatbázisrendszer karbantartja a tranzakciós naplót, amelyet általában nem szánnak ellenőrzési nyomvonalnak a későbbi elemzésekhez, és nem is olvashatók az ember számára. Ezek a naplók csak a meglévő adatok változásait rögzítik, hogy lehetővé tegyék az adatbázis helyreállítását az összeomlások vagy egyéb adathibák után, és az adatok konzisztens állapotban maradjanak. Ezért az adatbázisrendszerek általában általános eseménynaplókkal és tranzakciós naplókkal is rendelkeznek.
### Üzenetnaplók
Az Internet Relay Chat (IRC), az azonnali üzenetküldő (IM) programok, a csevegési funkcióval rendelkező peer-to-peer fájlmegosztó kliensek és a többszereplős játékok (különösen az MMORPG-k) által mentett szöveges kommunikációt üzenetnaplóknak nevezzük. Ezeket a naplókat általában egyszerű szöveges fájlokba menti a rendszer, de az IM és VoIP kliensek (pl. Skype) HTML-fájlokba menthetik őket, hogy megkönnyítsék az olvasást vagy engedélyezzék a titkosítást.
### Szervernaplók
A kiszolgálónapló valójában egy naplófájl, amely tartalmazza azon tevékenységek listáját, amelyeket maga a kiszolgáló végzett és hozott létre vagy tart fenn automatikusan. Általában ezek a fájlok nem érhetők el az általános internetfelhasználók számára, csak a webmester vagy egy internetes szolgáltatás más adminisztrátora számára.



## Referenciák ##

* [Naplófájl – Wikipédia](https://en.wikipedia.org/wiki/Log_file)

