{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD fájl – ASP.NET webkezelő fájlformátum",
  "description" :"További információ arról, hogy mi az AXD fájl és az API-k, amelyek AXD fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Mi az AXD fájl?

Az AXD fájl egy webbeállítási fájl, amelyet az ASP.NET beágyazott erőforráskérelmeinek kezelésére és lekérésére használnak. Utasításokat tartalmaz a beágyazott erőforrások, például képek, JavaScript ([.JS](/hu/web/js/)) és [.CSS](/hu/web/css/) fájlok visszanyerésére. Az AXD fájlokat erőforrások kliensoldali oldalakba való beillesztésére használják. Ez lehetővé teszi az ügyféloldalak számára, hogy szabványos módon hozzáférjenek ezekhez az erőforrásokhoz a szerveren.

## AXD fájlformátum

Az AXD fájlok bináris fájlokként vannak tárolva a szerver oldalon. Az ASP.NET-ben található webkezelő fájlokra utal, amelyek olyan összetevők, amelyek válaszokat generálnak a webszervernek küldött kérésekre. Az AXD fájlok egyéni feldolgozást hajtanak végre, mielőtt az ügyféloldali oldalkérések alapján generálják a választ. Ezeket általában **WebResource.axd** fájlként menti a rendszer.

### Mi az a WebResource.axd fájl?

A legtöbb ASP.NET projekt az AXD fájlokat WebResource.axd fájlként menti, amely lehetővé teszi az ügyféloldali oldalak számára az összeállításba beágyazott erőforrások letöltését. Ha a WebResources.axd kezelő nincs gyorsítótárban, hibakeresési módban futtatja az alkalmazás lassú teljesítményt tapasztalhat.

## Hivatkozások

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

