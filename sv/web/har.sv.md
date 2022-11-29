{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Fil", "Tillägg", "Filformat", "Filtillägg", "JSON", "Arkivfil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP-arkivfilformat",
  "description" :"Din filformatsguide för att lära dig vad en HAR-fil och API:er är som kan skapa och öppna HAR-fil.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Vad är HAR fil?

En fil med .har ([HTTP](/sv/web/http/) Archive)-fil är en HTTP-arkivfil som lagrar sessionsdata som överförs över många webbläsare (som Chrome, Safari, IE, Firefox, etc.) i [JSON] (/sv/web/json/) filformat. Datan som överförs över internet mellan servern och klienten (i det här fallet användarens webbläsare) innehåller HTTP-begäran och svarsrubriker som lagras i HAR-filen. Den innehåller vidare detaljerad information om prestandadata om webbsidor som laddas i webbläsaren. HAR-filer kan öppnas i vilken textredigerare som helst som Notepad på Microsoft Windows OS och TextEdit på Apple MacOS.

## HAR-filformat - Mer information

HAR-filer lagrar sessionsinformation i vanlig textfil med det populära JSON-formatet. Specifikationerna för HAR-filformat har tagits fram av Web Performance Group i World Web Consortium (W3C) men kunde inte publiceras. Det definierade dock framgångsrikt ett arkivformat för HTTP-transaktioner.

Förutom att övervaka överföringen av förfrågnings- och svarsinformation, används HAR-filer av utvecklare för att logga webbläsarens prestanda när det gäller sidladdningshastighet, innehållsladdningslängd, innehåll laddat, sökfrågor som körs för att få svar från webbläsaren och många andra .

## Varför använda HAR-filer?

HAR-filer kan vara till hjälp för att förbättra en webbplatss prestanda genom att utvärdera långa laddningstider, sidrenderingstider och svarstider. HAR-filer kan analyseras för att hitta sådana problem och lösa eventuella problem med webbplatsen för att förbättra prestandan.

## Hur genererar man HAR-fil?

Så, hur genererar man en HAR-fil? Tja, detta beror på vilken typ av webbläsare du använder för att generera en HAR-fil. I den här guiden listar vi stegen för webbläsaren Google Chrome. Metoder för att generera HAR-filer med Safari, Firefox, etc. kan enkelt sökas på internet och följas.

### Steg för att generera HAR-fil med Google Chrome

Följande steg kan utföras på en webbsida där problem uppstår.

1. Öppna webbsidan i Google chrome där problemet inträffade.
1. Öppna utvecklarverktyget (inspektera element).
1. Gå till vänster om panelen för att starta filinspelningen. Det finns en liten rund röd knapp i det här avsnittet.
1. Klicka på "Rensa ikonen" för att radera alla loggposter som sparats i webbläsaren.
1. För att spara innehållet du vill ha som visas ovan, högerklicka och klicka på "Spara som HAR-fil"

## Referenser

* [HAR-filformat - Wikipedia](https://en.wikipedia.org/wiki/HAR_(filformat))

