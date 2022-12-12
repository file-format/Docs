{
  "date" : "2019-10-11",
  "keywords" :[ "asp", "asp fájl", "asp fájlformátum", "asp fájltípus", "fájl", "típus", "mi az asp fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Active Server Pages File Format",
  "description" :"További információ arról, hogy mi az ASP-fájl és az API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ASP fájl?

Az ASP az Active Server Pages rövidítése, amely egy fejlesztői keretrendszer weboldalak létrehozásához. Lehetővé teszi, hogy egy belső szerver számítógépes kódot hajtson végre a webes kérések kiszolgálása érdekében. Amikor egy ASP-fájlra vonatkozó kérést generál a webböngésző, a szerver beolvassa a fájlt, és végrehajtja a benne lévő kódot/szkriptet, hogy létrehozza a **[HTML](/hu/web/html/)** eredményt, amelyet visszaküld a böngésző a megjelenítéshez.

A HTML-oldalakkal ellentétben, amelyek a kiszolgáló által kiszolgált statikus oldalak, az ASP-fájlok futás közben dinamikus tartalmat generálnak, amely adatbázisból származó adatokra vonatkozó kéréseket tartalmazhat. Az ASP-oldalak általában az .asp kiterjesztést használják a .html helyett. Mivel az ASP fájlon belüli kód/szkript a szerver oldalon fut le, a kérelmező böngésző nem láthatja a kiszolgált oldal felépítéséhez használt kódot. Minden modern böngésző képes megjeleníteni az eredményeként generált oldalakat. A Microsoft technológiára épülő ASP-vel készült oldalak a Microsoft Internet Information Services (IIS) szerverein kerülnek tárolásra.

## Az ASP fájlformátum rövid története
Az ASP csak néhány átdolgozáson ment keresztül, míg felváltotta az ASP.NET, amely egy modernebb és hatékonyabb módja a szerveroldali oldalak fejlesztésének és kezelésének. Az Internet Information Services (IIS) mellett alapértelmezés szerint az ASP támogatása is benne van. Az ASP három különböző verzióban jelent meg, mindegyikben fejlesztésekkel.

* Az ASP 1.0 1996 decemberében jelent meg az IIS 3.0 részeként
* Az ASP 2.0 1997 szeptemberében jelent meg az IIS 4.0 részeként
* Az ASP 3.0 2000 novemberében jelent meg az IIS 5.0 részeként

## ASP funkcionális objektumok

Az ASP-fájlok szerveroldali objektumokat használnak a felhasználói kérések feldolgozására és a felhasználók számára megjelenítendő kimeneti oldalak létrehozására. Minden objektum gyűjteményekkel, tulajdonságokkal és módszerekkel rendelkezik a kérések és válaszok feldolgozásához. Ezek az objektumok a következők:

### Objektum kérése

Amikor egy böngésző egy oldalt kér a szervertől, azt kérésnek nevezzük. A Request objektum arra szolgál, hogy információkat kapjon a látogatótól.

### Válaszobjektum

Az ASP Response objektum arra szolgál, hogy kimenetet küldjön a felhasználónak a szerverről.

### Szerverobjektum

Az ASP Server objektum a kiszolgáló tulajdonságainak és metódusainak elérésére szolgál. Lehetővé teszi az adatbázisokhoz (ADO) való kapcsolódást, a fájlrendszert és a kiszolgálóra telepített összetevők használatát.

### Munkamenet objektum

A munkamenet objektum olyan, mint egy kapcsolat a felhasználó böngészője, amely oldalt kér a szervertől, és maga a szerver között. Ez az ASP által létrehozott és a felhasználó számítógépére küldött cookie-val érhető el. A Session objektum információkat tárol egy felhasználói munkamenetről, illetve módosítja a beállításokat. Az információk egy munkamenetben tárolódnak. Az objektumok egy alkalmazás összes oldalán meg vannak osztva. A munkamenet-változókban tárolt általános információk a név, az azonosító és a beállítások. A kiszolgáló minden új felhasználóhoz új Session objektumot hoz létre, és a munkamenet lejártakor megsemmisíti a Session objektumot.

### Alkalmazásobjektum

Az Alkalmazás objektum olyan információkat tartalmaz, amelyeket az alkalmazás számos lapja használni fog (például adatbázis-kapcsolati információkat). Az információ bármely oldalról elérhető. Az információk egy helyen is módosíthatók, és a változások automatikusan minden oldalon megjelennek. Az Application objektum a változók tárolására és elérésére szolgál bármely oldalról, akárcsak a Session objektum.

### ASPERror objektum

Az ASPERror objektumot az ASP 3.0-ban valósították meg, és elérhető az IIS5-ben és későbbiekben. Az ASPERror objektum az ASP-oldalak parancsfájljaiban előforduló hibák részletes információinak megjelenítésére szolgál.

**Megjegyzés:** Az ASPERror objektum a Server.GetLastError meghívásakor jön létre, így a hibainformációk csak a Server.GetLastError metódussal érhetők el.

## Hivatkozások

* [ASP – W3C](https://www.w3schools.com/asp/default.asp)
* [Egyszerű ASP-oldalak létrehozása](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

