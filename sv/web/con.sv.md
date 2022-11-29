{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON File - Concept Application Source File Format",
  "description" :"Läs mer om vad som är en CON-fil och API:er som kan skapa och öppna CON-filer.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Vad är en CON fil?

En CON-fil är en källkodsfil för applikationer utvecklade för **Concept Application Server**. Den används för att skriva applikationer för utbyte av data mellan servern och användaren. CON-filer som finns på servern är tillgängliga med en webbläsare förutsatt att Concept Client är installerad på användarsidan. Koncept Application server är en webbserver med småskaligt programmeringsspråk som kan ha en [SQL](/sv/database/sql/) subset databasmotor (TinDB).

CON-filer kan öppnas/köras med RadGs Concept Application Server.

## CON-filformat - Mer information

CON-filer finns på servern och nås via webbläsaren på användarmaskinen. Konceptet [URLs](/sv/web/url/) skiljer sig från vanliga HTTP-webbadresser och börjar med **concept://**.

### CON Fil URL Exempel

En CON-fil som finns på Concept Application Server kan nås via webbläsare med hjälp av webbadresser som:

```
concept://domain.server.com/web_application/main.con.
```
## Referenser

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

