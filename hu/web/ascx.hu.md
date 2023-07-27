{
  "date" : "2019-10-11",
  "keywords" :[ "ascx", "ascx fájl", "ascx fájlformátum", "ascx fájltípus", "fájl", "típus", "mi az ascx fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX fájlformátum",
  "description" :"További információ az ASCX-fájlokról és az API-król, amelyek ASCX-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az ASCX fájl?

Az .ascx kiterjesztésű fájl egy felhasználói vezérlő, amelyet a weboldalak újrafelhasználható összetevőjeként használnak. Bármely ASP-webhelyen hivatkozhat rá, ha a vezérlőmezőből az oldalra húzza. Az ASCX felhasználói vezérlők központi forrásként adódnak hozzá a projekthez, így a felhasználói vezérlésben bekövetkezett bármilyen változás az egész webhelyen megjelenik. Ellentétben az ASMX fájlokkal, amelyek az interneten keresztül 2 objektumon belüli kommunikáció mechanizmusát határozzák meg, az ASCX fájlok felhasználói vezérlők az oldalakba vagy webhelyekbe való beágyazáshoz.

## ASCX fájlformátum

Az ASCX fájlok egyszerű szöveges formátumban íródnak, és kódot használhatnak olyan funkciók mögött, mint például az .ascx.cs végződésű weboldalak. A felhasználói vezérlők jelölőkódja a @Control direktívával kezdődik, amint az a következő példában látható.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Ez a webes felhasználói vezérlő számos oldalon újra felhasználható, például oldallábban, fejlécben vagy valamilyen webhelynavigációban. A webes felhasználói vezérlők minden más vezérlőhöz hasonlóan olyan tulajdonságokkal, módszerekkel és eseményekkel rendelkeznek, amelyek hasznossá teszik vizuális viselkedésük beállításában.

### Példa felhasználói vezérlők regisztrálására a web.config fájlban

Annak érdekében, hogy több oldalon egyetlen felhasználói vezérlőt használhasson, a webes vezérlő regisztrálható a web.config fájlban. Ez lehetővé teszi az egész webhely ellenőrzését ahelyett, hogy minden oldalon külön-külön regisztrálna. A következő példakód meghatározza, hogyan kell regisztrálni egy webes vezérlőt a web.config fájlban, hogy láblécként jelenjen meg a teljes webhelyen.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Hivatkozások

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX felhasználói vezérlés](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

