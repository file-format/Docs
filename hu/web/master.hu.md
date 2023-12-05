{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER File - ASP.NET Master Page File Format",
  "description" :"További információ a MASTER fájlformátumról és a MASTER fájlok létrehozásához és megnyitásához szükséges API-król.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Mi az a MASTER fájl?

A MASTER fájl egy ASP.NET-el létrehozott weblapsablon-fájl. Kiindulási pontként szolgál több olyan oldal létrehozásához, amelyek elrendezése és beállításai megegyeznek a MASTER fájléval. A sablon MASTER fájl tartalmazza a fejléc, a navigációs menük, a lábléc, a betűtípus és a stílusinformációk beállításait. A MASTER fájl használatával gyorsan hozhat létre több weboldalt.

A MASTER fájlt a Microsoft Visual Studio 2022 és újabb verziójával nyithatja meg.

## MASTER fájlformátum - További információ

A MASTER fájl létrehozása és mentése HTML fájlformátumban történik, és hasonló bármely más weboldal fájlhoz. Szerkeszthető és nem szerkeszthető részekre van felosztva. A szerkeszthető szakaszok azok, amelyek a felhasználói igényeknek megfelelően módosíthatók. A nem szerkeszthető részek szürkén jelennek meg, amikor a MASTER fájlt megnyitják a Microsoft Visual Studio programban.

A mesteroldalak két részből állnak, azaz magából a mesteroldalból és egy vagy több tartalomoldalból.

### MESTER oldal

A mesteroldal .master kiterjesztéssel rendelkezik, és az ASP.NET-ben készült. Előre meghatározott elrendezéssel rendelkezik, amely statikus szöveget, HTML-címkéket és szerveroldali vezérlőket tartalmaz. A közönséges .aspx oldalakon a @ Page direktíva használatos. .master fájlok esetén ezt a @ Master direktíva váltja fel.

### Tartalmi oldalak

A tartalomoldal a mesteroldal helyőrző vezérlőinek tartalmát képviseli. Ezek .aspx oldalak, amelyek valójában a mesteroldal mögötti kódot jelentik. A tartalmi oldalak a @ Page direktívával vannak kötve egy MasterPageFile attribútum hozzáadásával, amely a mesteroldalra mutat, és az alábbiak szerint használható.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Hivatkozások

* [ASP.NET Master Pages Overview](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

