{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "XSL Formatting Objects", "File", "Extension", "File Format", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Läs mer om XSLFO-filformat och API:er som kan skapa och öppna XSLFO-filer.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är en XSL-FO fil? ##

XSL-FO (XSL Formatting Objects) är ett kraftfullt formatmallsspråk för formatering av XML-dokument. Semantiken för den avgränsade formen av papper och tryck uttrycks av XSL-FO när dimensionerna är fixerade. I motsats till HTML, som representerar semantiken för den obegränsade formen av ett webbläsarfönster med variabla dimensioner. XML-dokumenten formaterade av XSL-FO används mest för att generera PDF-filer. XSL (Extensible Stylesheet Language) är en uppsättning funktionskomplett W3C-teknik avsedd att utforma för formatering och utbyte av XML-dokument och XSL-FO-del av detta språk. XSLT och XPath är också andra delar av XSL.

Det föreslås att XML-dokument först ska transformeras till XSL-FO, PDF är ett exempel på detta kriterium. I PDF renderas resultaten med XSLTfirst och sedan XSL-FO-formaterare. På detta sätt kan XML-dokument formateras slumpmässigt. Även om XSL-FO drar fördel av att använda egenskaper för Cascading Style Sheet (CSS) och utöka dem där det är nödvändigt för det verkliga formatet, innehåller det tillhandahållandet av sidmallar som kallas sidmaster i XSL-FO-terminologin. XSL-FO tillhandahåller även formatering för ganska sofistikerade dokument och stöder indexgenerering.

## Historik och grundläggande begrepp ##

I januari 2012 uppdaterades arbetsutkastet för XSL-FO förra gången, och i november 2013 hade dess arbetsgrupp stängts. En XSL-formatmall specificerar presentationen av en klass av XML-dokument genom att beskriva hur en instans av klassen omvandlas till ett XML-dokument som använder formateringsordförrådet. XSL-FO är ett integrerat presentationsspråk och har inga semantiska markeringar som används i HTML. Dessutom lagrar detta språk all dokumentets data i sig själv, till skillnad från CSS som ändrar standardinställningarna för ett externt HTML- eller XML-dokument.

De allmänna kriterierna för att använda XSL-FO är att användaren skriver ett dokument på ett XML-språk istället för att skriva i FO. Därefter sker en XSLT-transform. Denna XSLT-transform är ansvarig för konverteringen av XML till XSL-FO. Så snart XSL-FO-dokumentet genereras, överlämnas det sedan till en applikation som kallas en FO-processor. FO-behandlare är ansvariga för att omvandla detta dokument till ett läsbart såväl som ett utskrivbart dokument. PDF-filer eller PS är exempel på den vanligaste produktionen av XSL-FO. Men det betyder inte att FO-processorn bara kan producera dessa två typer av format som utdata. Vissa FO-processorer kan mata ut i RTF-filerna eller till och med ett fönster kan visas i användarens GUI, detta fönster visar sidans sekvens och dess innehåll.

Ett XSL-FO-dokument skiljer sig från en PDF eller en PS i den meningen att det i slutändan inte definierar textlayouten på olika sidor. Kanske stilar det sidorna och bestämmer platserna för att visa innehållet. Dessutom organiserar en FO-processor texten inom de gränser som anges av FO-dokumentet. Denna specifikation tillåter till och med olika FO-processorer att bete sig i enlighet med de resulterande skapade sidorna. Ett exempel på sådant beteende är avstavning, få FO-processorer kan avstava ord för att spara utrymme när en radbrytning, medan vissa processorer inte väljer det här alternativet. Det beror på processorerna att välja olika avstavningsalgoritmer som matchar deras krav. Dessa avstavningsalgoritmer kan vara mycket enkla eller kanske mer komplexa. I vissa situationer sanktionerar XSL-FO-specifikationen uttryckligen FO-processorer, en viss grad av val i sammanhanget till layouten.

Denna variation mellan FO-processorer genererar varierande resultat, som processorer ofta förblir obekymrade över. Eftersom den allmänna fokusen för XSL-FO är att producera pagade/tryckta dokument. XSL-FO-dokument själva fungerar vanligtvis som mellanhänder, deras huvudsakliga funktion är att generera antingen PDF-filer eller ett dokument som kan skrivas ut som utdata som ska distribueras. I HTML/CSS eller XSL-FO indikerar distribution av PDF-filen som slutresultat snarare än att mata in formateringsspråket att mottagare förblir opåverkade av den resulterande mångsidigheten som skapas på grund av skillnader mellan tolkarna av formateringsspråk. Å andra sidan är det uppenbart att det inte finns något enkelt sätt att ett dokument kan uppfylla mottagarnas olika behov, t.ex. variabel sidstorlek eller önskad teckenstorlek, eller skräddarsydda för sida eller utskrift.

## XSLFO-filformat ##

SL-FO-dokument är i grunden XML-dokument, men de följer inget schema. I stället följer SL-FO-dokument den syntax som definieras i specifikationen för deras eget språk. Det finns två avsnitt som krävs i varje XSL-FO-dokument:

1. En sektion som anger en lista över märkta sidlayouter.
1. En sektion med alla detaljer om dokumentdata, med markering, som bestämmer visningen av innehåll på olika sidor genom olika sidlayouter.

Sidans egenskaper nämns i sidlayouterna, som kan definiera organisationen för texten, för att följa konventionerna för det specifika språket. Dessutom definieras sidans storlek, deras marginaler och sidornas sekvenser (som sanktionerar olika egenskaper för de udda och jämna sidorna) av sidlayouterna.

Datadelen av dokumentet är uppdelad i en serie flöden, där varje flöde är kopplat till en sidlayout. Flödena bifogar en lista med block i dem. Den här listan med block kan innehålla inline-markeringsfunktioner eller en lista med textdata, eller kanske båda samtidigt. Marginaler på dokumentet kan också visa sidnummer eller kapitelrubriker. Funktionaliteten för både block och inline-element förblir densamma som i CSS, men vissa utfyllnads- och marginalregler är olika mellan FO och CSS.

Sidorienteringsriktningen är helt specificerad för förlängning av block och inlines, vilket gör att FO-dokument fungerar på andra språk än engelska. Språket i FO-specifikationen använder orden start och slut snarare än vänster och höger för vägbeskrivning. XSL-FO:s grundläggande innehållsmarkering och kaskadregler är hämtade från CSS. XSL-FO:s språk överensstämmer med följande specifikationer.

## Flera kolumner ##

En sida kan ha flera kolumner och block och kan sträcka sig från en kolumn till en annan som standard. Flera sidor tillåts ha olika bredd och antal kolumner. Alla FO-egenskaper följer gränserna för en sida med flera kolumner.

### Listor ###

En XSL-FO-lista upprättas av två uppsättningar block ordnade kind för käke. Konceptuellt, i en lista, indikerar ett block till vänster ett nummer, en punkt eller en textsträng, medan det högra blocket kan fungera som förväntat. Numreringen av XSL-FO-listor görs vanligtvis av XSLT.

### Tabeller ###

En FO-tabell liknar en HTML/CSS-tabell. Användaren kan välja rader med data, stilinformation, bakgrundsfärg för varje enskild cell. Genom att använda distinkt stilinformation har användaren privilegiet att välja den första raden som en tabellrubrik. FO-processorn kan explicit informeras om utrymmesspecifikationen för varje kolumn, eller för att automatiskt anpassa texten i tabellen.

### Indexering ###

XSL-FO 1.1 har funktioner som hjälper till att generera ett index genom att referera till korrekt markerade element.

### Fördelar ###

* Lämplig för innehållsbaserad publicering
* Enkel användning
* Låg kostnad

## Referenser ##

* [Vad är XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL-formateringsobjekt](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

