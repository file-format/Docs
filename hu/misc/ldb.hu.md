{
"dátum": "2023-04-20",
  "keywords": [
"ldb fájl",
"mi az ldb fájl",
"milyen információt tartalmaz az ldb",
"mi a célja az ldb fájlnak",
"ldb kiterjesztés",
"fájl",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LDB fájlformátum - Microsoft Access Lock File",
  "description":"Ismerje meg az LDB formátumot és milyen információkat tartalmaz.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Mi az LDB fájl?

Az LDB-fájl a Microsoft Access által használt zárfájl, amely megakadályozza, hogy több felhasználó egyidejűleg szerkeszthesse ugyanazt az adatbázist. Amikor a felhasználó megnyit egy Access-adatbázist, az Access létrehoz egy megfelelő LDB-fájlt ugyanabban a könyvtárban, mint az adatbázis. Ez a fájl információkat tartalmaz arról, hogy kik használják jelenleg az adatbázist, és milyen rekordokat szerkesztenek.

Az LDB fájlt a Microsoft Access automatikusan létrehozza az adatbázis megnyitásakor, és törli az adatbázis bezárásakor. Fontos megjegyezni, hogy az LDB fájlt soha nem szabad kézzel törölni, mert ez problémákat okozhat az adatbázisban.

Ha problémákat tapasztal a Microsoft Access adatbázissal, az egyik lehetséges megoldás az, hogy megpróbálja törölni az adatbázishoz társított LDB fájlt. Ezzel felold minden olyan zárolást, amely akadályozhatja az adatbázis elérését. Mielőtt azonban ezt megkísérelné, mindenképpen készítsen biztonsági másolatot az adatbázisról, mivel az LDB-fájl törlése adatvesztést vagy -sérülést okozhat, ha nem megfelelően végzi el.

## LDB fájlformátum - További információ

A Microsoft Access egyik LDB-fájlja információkat tartalmaz azokról a felhasználókról, akik éppen hozzáférnek az adatbázishoz, például felhasználónevüket, számítógépnevüket és bejelentkezési idejüket. Az LDB fájl információkat tartalmaz az adatbázisban elhelyezett zárolásokról is, például, hogy melyik felhasználó mely rekordokat szerkeszti.

Itt található az LDB fájlban található információtípusok részletes listája:

- **Felhasználónév** - annak a felhasználónak a neve, aki éppen hozzáfér az adatbázishoz
- **Számítógép neve** - annak a számítógépnek a neve, amelyről a felhasználó hozzáfér az adatbázishoz
- **Bejelentkezési idő** - az az időpont, amikor a felhasználó először megnyitotta az adatbázist
- **Rekordzárak** - információ arról, hogy melyik felhasználó mely rekordokat szerkeszti éppen
- **Objektumzárak** - információ arról, hogy melyik felhasználó mely adatbázis-objektumokat (például táblákat, űrlapokat vagy jelentéseket) szerkeszti éppen
- **Kapcsolódási információ** - Információ arról, hogy a felhasználó hogyan csatlakozik az adatbázishoz (például, hogy helyi vagy hálózati kapcsolatot használ-e)

Az LDB-fájlban található információkat a Microsoft Access arra használja fel, hogy megakadályozza, hogy több felhasználó egymással ütköző módosításokat hajtson végre ugyanabban az adatbázisban. Amikor a felhasználó egy másik felhasználó által már zárolt rekordot vagy objektumot próbál meg szerkeszteni, a Microsoft Access üzenetet jelenít meg, amely jelzi, hogy az objektum már használatban van. Az LDB fájl frissül, amikor a felhasználók megnyitják és bezárják az adatbázist, és módosítják a zárolt objektumokat.

## Hivatkozások
* [Mi az LDB-fájl?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

