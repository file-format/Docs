{
  "date" : "2019-10-11",
  "keywords" :[ "aex","aex-fil", "filformat", "filtyp", "vad är en aex-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AEX - Alpha Five Compiled Global Functions File",
  "description" :"Lär dig veta vad en AEX-fil och API:er är som kan skapa och öppna AEX-filer.",
  "linktitle" : "AEX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-07"
}

## Vad är en AEX fil?

En AEX-fil (med .aex-tillägg) är en kompilerad [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) fil som innehåller kompilerad programkod för globala funktioner. Den kan användas i webbapplikationer genom att anropa dem från [.a5w](/sv/web/a5w/)-sidor på serversidan. AEX-filer laddades och avlastades genom att anropa funktionerna a5w_load_aex respektive a5w_unload_aex från A5W-filer. Men i en ny implementering läses dessa filer in i minnet genom att inkludera i filen a5_application.5i. Xbasic programmeringsspråk används av programvaran Alpha Anywhere för utveckling av mobil- och webbapplikationer.

## AEX-filformat - Mer information

AEX-filer sparas på skiva i binärt filformat och innehåller kompilerad kod av funktioner skrivna i Xbasic. Xbasic script-kommandosatser bestämmer strukturen och flödet av exekvering, inklusive att utföra eller stoppa en upprepad åtgärd, eller att välja mellan två eller flera steg baserat på förhållandena. [Xbasic Language Reference](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) kan konsulteras för detaljerad information om det.

## Referenser

* [Alpha Five](https://www.alphasoftware.com/)
* [Alpha Five Documentation](https://documentation.alphasoftware.com/documentation/pages/index.html)
* [Xbasic Guide](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)

