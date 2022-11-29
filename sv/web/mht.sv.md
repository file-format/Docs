{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "mht fil", "mht filformat", "mht filtyp", "fil", "typ", "vad är en mht fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML-filformat",
  "description" :"Läs mer om MHT-filformat och API:er för att skapa och öppna MHT-filer.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Vad är en MHT fil?

En fil med filtillägget .mht är ett MIME-aktiverat arkiveringsfilformat som innehåller olika typer av data i en enda fil. Den kan lagra data som text, bilder, sidstil i form av [CSS](/sv/web/css/)-filer, JavaScript och andra resurser som inbäddade resurser i den. MHT-filer, med MIME-typ message/rfc822, kapslar in allt innehåll i en HTML-fil som en enda arkivfil för lagring vid arkivering på lagringsenheter. Programvaror som Microsoft Word låter dig konvertera dina WORD-dokument till MHT genom att exportera som MHT-fil. MHT-filer kan öppnas med populära webbläsare som Microsoft Internet Explore och Google Chrome.

## MHT filformat

Precis som [MHTML](/sv/web/mhtml/) är MHT också en MIME-inkapsling av aggregerade HTML-dokument. Dokumentinnehåll i ett MHT-dokument såsom inline-bilder, stilmallar, applets, etc. är MIME-kodade där dessa är länkade till en rotresurs via URI:er. E-postklienter som Microsoft Outlook lagrar e-postmeddelanden (vanligtvis [EML](/sv/email/eml/)) i MHT-filformat. Fullständiga specifikationer för MHT-filformat finns i [RFC 822](https://tools.ietf.org/html/rfc822) och kan hänvisas till för utveckling av programvaruapplikationer som kan bearbeta MHT-filer.

## Skillnaden mellan MHT och MHTML

När du sparar en onlinesida ombeds användaren att bestämma sig för vilken typ av filformat inom vilket onlinesidan måste sparas i det ursprungliga systemet. Vanligtvis blir användaren förvirrad mellan märkningsspråk och MHTML-filformat. De märker att det är jobbigt att se att filformatet är sundare mellan dessa.

När en användare bestämmer sig för att undvika att slösa bort en onlinesida som märkningsspråk, bildas en mapp som innehåller flera filer för olika innehåll på sidan, dvs. helt olika filers områdesenhet skapad för text, grafik, applets etc. Å andra sidan sparas onlinesidan som MHTML skapar en fil för hela onlinesidan. Alla delar av sidan tillsammans med grafik, länkar och alternativa filer områdesenhet inbäddade i en fil.

Naturligtvis är det enkelt att hantera MHT- eller MHTML-filer eftersom filen, som kan skyddas och delas helt enkelt via e-post. Emellertid kan markeringsspråksfilernas områdesenhet under risken för informationsförlust som förlust eller radering av ens en fil göra att hela markup language-mappen är värdelös för användaren.

## Referenser

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

