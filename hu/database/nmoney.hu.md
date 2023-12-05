{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az NMONEY fájlformátumról és az API-król, amelyek NMONEY fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"NMONEY fájl - Denaro-fiók fájlformátum",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Mi az a NMONEY fájl?

Az NMONEY fájl egy pénzügyi adattároló adatbázisfájl, amely a pénzügyi tranzakciók nyomon követését tartalmazza. A Nickvision fejlesztette ki, és a Nickvision Denaro szoftverben használták, amely egy személyes pénzügyi szoftveralkalmazás. A NOMONEY fájlban tárolt adatok tartalmazzák a számla jóváírási és terhelési tranzakcióit.

A NOMONEY fájlok a [Github](https://github.com/NickvisionApps/Denaro) alkalmazással nyithatók meg.

## A Denaro Software-ről

A Denarót eredetileg a [Nickvision](https://nickvision.org/) fejlesztette ki termékként, amelyet később a [Github]-on tárolt nyílt forráskódú szoftveralkalmazássá alakítottak át (https://github.com/NickvisionApps/Denaro) . Azóta az alkalmazást csak a Githubon módosították és frissítették. Az alkalmazást C# nyelven fejlesztették ki a Windows UI-ban, a Windows App SDK-val (a jelenlegi WinUI 3 verzióval).

### A Denaro által kínált szolgáltatások

* Egyszerre több fiókot is kezelhet a legnépszerűbb és legismertebb lapfelületén
* A tranzakciók szűrése típus, csoport vagy dátum szerint
* Ismételje meg a tranzakciókat, például a számlákat, amelyek minden hónapban előfordulnak
* Pénz átutalása egyik számláról a másikra
* Exportálja az adatokat egy fiókból CSV-fájlként, és importáljon CSV-, OFX- vagy QIF-fájlt, hogy tranzakciókat adjon hozzá egy fiókhoz

## Denaro fájlformátum - További információ

A Denaro fájlok bináris fájlformátumban kerülnek a lemezre. A pénzügyi adatok adatbázisfájlként vannak tárolva **.SQLITE3** fájlformátumban. Az SQLITE egy könnyű SQL adatbázisfájl, amelyet az SQLite szoftverrel hoztak létre. Önálló adatbázis-motort biztosít, amely képes teljes körű és rendkívül megbízható adatbázis biztosítására. Az SQLite adatbázisfájlok segítségével gazdag tartalom osztható meg a rendszerek között, egyszerűen cserélve ezeket a fájlokat a hálózaton keresztül. SQLite-összerendelések léteznek olyan programozási nyelvekhez, mint a C, [C#](/hu/programing/cs/), [C++](/hu/programing/cpp/), [Java](/hu/programing/java/), [PHP](/hu/programing/ php/), és még sokan mások.

## Hivatkozások

* [Nickvision](https://nickvision.org/)
* [NIckVision – Github](https://github.com/NickvisionApps/Denaro)

