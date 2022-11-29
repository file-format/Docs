{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Handheld Device Markup Language File",
  "description":"Läs mer om HDML-filformat och API:er som kan skapa och öppna HDML-filer.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Vad är en HDML fil?

En fil med tillägget .hdml (Handheld Device Markup Language) är ett märkningsspråk för att skapa webbsidor för bärbara elektroniska enheter som handdatorer, smartphones och informationsskärmsapparater. HDML sägs vara en förlängning av språket [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML liknar HTML men för trådlösa och handhållna enheter som har små skärmar som PDA, mobiltelefoner och så vidare. Det ersattes med WML för vilket det fungerade som ett viktigt inflytande.

## HDML-filformat - Mer information

HDML är ett märkningsspråk för handhållna enheter som är baserat på märkningstaggar som liknar HTML. HDML skickades till W3C för standardisering men det blev aldrig en standard. Dess filformatspecifikationer finns dock tillgängliga på [W3-webbplatsen](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) för referens. [syntax för HDML-språk](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) är tillgänglig för utvecklarens referens och kan användas för exempelutveckling av applikationer.

## HDML-element

Följande är en upplysning av element som tillhandahåller körtidsmiljö för HDML och kallas användaragenten.

|Element|Beskrivning|
---|---|
|Kort|Detta är den grundläggande byggstenen i HDML, och visar och låter användaren interagera med informationskort. |
|Däck|HDML-kort är grupperade i kortlekar. Ett HDML-kort liknar en HTML-sida genom att det identifieras av URL [RFC1738] och är den enhet av innehåll som begärs från en server och cachelagras av användaragenten.|
|Actions|Actions kan vara av PREV, SOFT1-SOFT8 och HELP-typ. Dessa är abstrakta och stöds i användargränssnittet på ett användaragentspecifikt sätt.|
|Aktiviteter|En aktivitet är som en grupp relaterade kort som utför en logisk funktion. Dessa kan sträcka sig över ett eller flera däck. HDML-navigerings- och tillståndsmodellen är uppbyggd kring aktiviteter.|
|Historikbaserad navigering|Användaragenten upprätthåller en historik över de kort som visas för användaren. Varje kort som nås läggs till i korthistoriken. Användaragenten låter användaren enkelt navigera tillbaka till föregående kort i historiken.|

## Referenser

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML-specifikationer - W3-skolor](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

