{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM-fil - Handheld Device Markup Language File",
  "description":"Läs mer om HDM-filformat och API:er som kan skapa och öppna HDM-filer.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Vad är en HDM fil?

En HDM-fil är en webbsidesfil för märkningsspråk som skapas i Handheld Device Markup Language (HDML). Den innehåller uppmärkningstaggar som liknar språket [HTML](/sv/web/html/), men är designat för handhållna elektroniska enheter som smartphones och handdatorer. [HDML-filformatsspecifikationerna](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) skickades till W3C för standardisering men kunde inte bli en standard. HDM baseras på [HDML](/sv/web/hdml/) filformatspecifikationer som finns tillgängliga på W3s webbplats.

## HDM-filformat - Mer information

HDM-filen består av uppmärkningstaggar som renderas till visuellt utformade webbplatser på handhållna enheter. HDM-filer kopieras till enheter som använder HDTP-protokollet (Handheld Device Transport Protocol) istället för HTTP-protokollet som används för HTML-sidor.

## HDML-filelement

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

