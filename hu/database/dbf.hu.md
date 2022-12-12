{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extension", "dbf file", "dbf file format", "Database File Type", "Database File Format", "What is a dbf file", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DBF fájlformátumról és az API-król, amelyek DBF fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DBF - dBase Database File",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Mi az a DBF fájl?
A .dbf kiterjesztésű fájl egy adatbázis-fájl, amelyet a **dBASE** nevű adatbázis-kezelő rendszeralkalmazás használ. Kezdetben a dBASE adatbázis neve Project Vulcan volt; **Wayne Ratliff** indította el 1978-ban. A DBF fájltípust 1983-ban vezették be a dBASE II-vel. Több adatrekordot rendez tömb típusú mezőkkel. Az **xBase** adatbázisszoftver, amely a fájlformátumok széles skálájával való kompatibilitása miatt népszerű; támogatja a DBF fájlokat is.

## DBF fájlformátum
A DBF fájlformátum a dBASE adatbázis-kezelő rendszerhez tartozik, de lehet, hogy kompatibilis az xBase vagy más DBMS szoftverekkel. A dbf fájl kezdeti verziója egy egyszerű táblázatból állt, amelyhez adatokat lehetett hozzáadni, módosítani, törölni vagy kinyomtatni az ASCII karakterkészlet használatával. Az idő múlásával a .dbf javult, és további fájlokat adtak hozzá az adatbázis-rendszer szolgáltatásainak és képességeinek bővítése érdekében.

A modern dBASE-ban a DBF fájl egy fejlécből, az adatrekordokból és az EOF (Fájl vége) jelölőből áll.

- A fejléc információkat tartalmaz a fájlról, például a rekordok számát és a rekordokban használt mezők típusát.
- A nyilvántartások a tényleges adatokat tartalmazzák.
- A fájl végét egyetlen bájt jelöli, 0x1A értékkel.

### Fájlfejléc
A dBase fájlfejléc elrendezése a következő táblázatban látható:

| Byte | Tartalom | Jelentése |
---|---|---|
| 0 | 1 bájt | Érvényes dBASE DOS fájlhoz; A 0-2 bit a verziószámot, a 3-as bit a dBASE DOS-jegyzetfájl jelenlétét, a 4-6 bitek egy SQL-tábla jelenlétét jelzik, a 7-es bit bármely memofájl jelenlétét jelzi (akár dBASE m PLUS, akár dBASE DOS) |
| 1–3 | 3 bájt | Az utolsó frissítés dátuma; formátumban YYMMDD |
| 4–7 | 32 bites szám | Rekordok száma az adatbázisfájlban |
| 8–9 | 16 bites szám | A fejlécben lévő bájtok száma |
| 10–11 | 16 bites szám | A rekord bájtok száma |
| 12–13 | 2 bájt | Fenntartott; töltse ki 0 |
| 14 | 1 bájt | Hiányos tranzakciót jelző jelző[1. megjegyzés] |
| 15 | 1 bájt | Titkosítási jelző[2. megjegyzés] |
| 16–27 | 12 bájt | Fenntartva a dBASE for DOS számára többfelhasználós környezetben |
| 28 | 1 bájt | Gyártási .mdx fájl jelző; 1, ha van éles .mdx fájl, 0, ha nincs |
| 29 | 1 bájt | Nyelvi illesztőprogram-azonosító |
| 30–31 | 2 bájt | Fenntartott; töltse ki 0 |
| 32–n [3. jegyzet][4. jegyzet] | egyenként 32 bájt | mezőleírók tömbje (a leírók elrendezését lásd alább) |
| n + 1 | 1 bájt | 0x0D, mint a mezőleíró tömblezáró |

- Az ISMARKEDO funkció ellenőrzi ezt a jelzőt (a TRANSACTION BEÁLLÍTÁSA 1-re állítja, END TRANSACTION és ROLLBACK visszaállítja 0-ra).
- Ha ez a jelző 1-re van állítva, az Adatbázis titkosítva üzenet jelenik meg.
- A mezők maximális száma 255.
- n a mezőleíró tömb utolsó bájtját jelenti.

### Mezőleíró tömb
A mezőleírók elrendezése dBASE-ban:

| Byte | Tartalom | Jelentése |
---|---|---|
| 0–10 | 11 bájt | Mezőnév ASCII-ben (nullával kitöltve) |
| 11 | 1 bájt | Mezőtípus. Megengedett értékek: C, D, F, L, M vagy N (a jelentéseket lásd a következő táblázatban) |
| 12–15 | 4 bájt | Fenntartva |
| 16 | 1 bájt | A mező hossza binárisan (maximum 254 (0xFE)). |
| 17 | 1 bájt | A mező decimális száma binárisan |
| 18–19 | 2 bájt | Munkaterület azonosító |
| 20 | 1 bájt | Példa |
| 21–30 | 10 bájt | Fenntartva |
| 31 | 1 bájt | Gyártási MDX mezőjelző; 1, ha a mező tartalmaz indexcímkét az éles MDX-fájlban, 0, ha nincs |

### Adatbázis rekordok
Minden rekord törlési (1 bájtos) jelzővel kezdődik. A mezők mezőelválasztók nélküli rekordokba vannak csomagolva. Minden terepi adat ASCII. A mező típusától függően az alkalmazás további korlátozásokat ír elő. Íme a dBase mezőtípusai:

| Mezőtípus | Mnemonikus | Mit fogad el |
-------|-----|----|
| C | Karakter | Bármilyen ASCII-szöveg (a mező hosszáig szóközökkel kitömve) |
| D | Dátum | Számok és egy karakter a hónap, a nap és az év elválasztására (belül 8 számjegyben tárolva ÉÉÉÉHHNN formátumban) |
| F | Lebegőpontos | -, ., 0–9 (jobbra igazítva, szóközzel kitömve) |
| L | Logikai | Y, y, N, n, T, t, F, f vagy ? (inicializálatlan állapotban) |
| M | Jegyzet | Bármilyen ASCII-szöveg (belső 10 számjegyként tárolva, amely egy .dbt blokkszámot jelent, jobbra igazítva, szóközökkel kitömve) |
| N | Numerikus | -, ., 0–9 (jobbra igazítva, szóközzel kitömve) |









## Referenciák ##

* [.dbf - Wikipédia](https://en.wikipedia.org/wiki/.dbf)

