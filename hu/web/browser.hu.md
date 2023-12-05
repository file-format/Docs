{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BÖNGÉSZŐfájl - ASP.NET böngésződefiníciós fájlformátum",
  "description":"További információ a BROWSER fájlformátumról és az API-król, amelyek BROWSER fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browser"
}
},
  "lastmod" : "22023-06-06"
}

## Mi az a BROWSER fájl?

Az ASP.NET webalkalmazások egy .browser kiterjesztésű fájlt használnak a webböngészők képességének és konfigurációjának meghatározására. Információkat tartalmaz a böngésző képességeiről, korlátairól és jellemzőiről. Ezek a jellemzők segítik az ASP.NET keretrendszert, hogy felismerje a kérelmező böngészőt, és ennek megfelelően mutassa be a weboldalt a felhasználóknak.

## BÖNGÉSZŐ Fájlformátum

A BROWSER definíciós fájlokat az ASP.NET alkalmazás használja a böngésző képességeinek meghatározására. Az ebben a fájlban található információkat a szerver használja fel jelölések és egyéb erőforrások generálására, amelyek kompatibilisek a kérelmező böngészővel.

A BROWSER fájlok egyszerű szöveges fájlformátumban kerülnek mentésre. A BROWSER fájlokat olyan szövegszerkesztőkkel nyithatja meg, mint a Notepad, Notepad++, Apple TextEdit és Visual Studio IDE.

### A BROWSER fájlformátum fájlstruktúrája

A BROWSER definíciós fájlok hierarchikus struktúrát használnak. Minden .browser fájl tartalmaz egy XML jelölést, amely egy adott böngésző vagy böngészőcsoport képességeit és szolgáltatásait tartalmazza. Ezek a részletek magukban foglalják az olyan jellemzőket, mint az ügynökkarakterlánc, a verziószámok és az olyan technológiák támogatása, mint a JavaScript, a CSS vagy más HTML-elemek. E böngésződefiníciós fájlok használatával az ASP.NET fejlesztői a különböző böngészők képességei alapján testreszabják a felhasználói élményt.

## Hivatkozások

* [Fájlok használata ASP.NET-weboldalakon](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)



