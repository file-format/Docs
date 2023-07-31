{
  "date" : "2019-10-11",
  "keywords" :[ "chm", "chm-fil", "chm-filformat", "chm-filtyp", "fil", "typ", "vad är en chm-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Compiled HTML Help File Format",
  "description" :"Läs mer om vad som är en CHM-fil och API:er som kan skapa och öppna dem.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är CHM fil?

CHM-filformatet representerar Microsofts **[HTML](/sv/web/html/)** hjälpfil som består av en samling HTML-sidor. Den tillhandahåller ett index för snabb åtkomst till ämnena och navigering till olika delar av hjälpdokumentet. CHM-filen kan sökas efter innehåll via det medföljande sökalternativet. CHM är Microsoft Proprietary online hjälpfilformat som ofta används för programvarudokumentation. Dessutom används den i flera andra applikationer som utbildningsguider, interaktiva böcker och elektroniska nyhetsbrev. De flesta moderna Microsoft Development-miljöer stöder generering av CHM-dokumentation från information som finns tillgänglig i applikationen.

Den unika förmågan hos CHM-filformat att implementera en kombinerad innehållsförteckning och index gör det distinkt från andra vanliga HTML-sidor. Den genererade CHM-filen är relativt liten i storlek och kan därför enkelt distribueras med mjukvarupaket. Hjälpverktyget HTML Help Workshop tillhandahåller ett lättanvänt system för att skapa och hantera hjälpprojekt och deras relaterade filer. CHM-filer kan innehålla text, bilder och hyperlänkar; kan visas i en webbläsare; används av Windows och andra program som en onlinehjälplösning.

## CHM filformat

Den slutliga formen av genererad CHM-fil beror på hur hjälpsystemet är utformat och om det är avsett för en applikation eller en webbplats. En CHM-fil stöder datakomprimering med LZX-komprimering för att generera de komprimerade HTML-filerna. Den har den inbyggda sökmotorn för snabb sökning av innehåll tillsammans med möjligheten att slå samman flera .CHM-filer. En CHM-fil består av en uppsättning HTML-filer, en länkad innehållsförteckning och en indexfil.

### HTML-filer

Oavsett om du skapar hjälpämnen för distribution med ett program eller på webben, skapas dokumenten du skapar med ett speciellt formateringsspråk som kallas HTML (Hypertext Markup Language). HTML-ämnefiler har filnamnstillägget .htm eller .html.

Även om varje hjälpämne eller webbsida du skapar verkar vara ett dokument med text, grafik eller animerade bilder, är .htm-filer faktiskt textdokument som har speciella HTML-formateringskoder. Dessa koder, som kallas taggar, talar om för en webbläsare hur varje sida ska visas. Endast texten som visas i ett ämne eller en webbsida finns faktiskt i .htm-filen. Eventuell grafik, ljud, animerade bilder eller andra element som visas är separata filer som din HTML-fil pekar på. Webbläsaren kopierar eller laddar ner grafik, ljud eller andra element när den ser taggarna som säger åt den att göra det.

### Innehållsförteckning (TOC)
Hjälpinnehållsförteckningen (.hhc)-filen är en HTML-fil som innehåller ämnestitlarna för din innehållsförteckning. När en användare öppnar innehållsförteckningen i en kompilerad hjälpfil (eller på en webbsida) och klickar på en ämnesrubrik, öppnas HTML-filen som är kopplad till den titeln.

### Indexfil
Indexfilen (.hhk) är en HTML-fil som innehåller indexposterna (sökord) för ditt index. När en användare öppnar indexet i en kompilerad hjälpfil eller på en webbsida och klickar på ett nyckelord, öppnas HTML-filen som är kopplad till nyckelordet.

## HTML Hjälpkomponenter

HTML-hjälpen består av flera komponenter. Dessa inkluderar följande:

* `HTML Help Workshop`: ett hjälpverktyg med ett lättanvänt grafiskt gränssnitt för att skapa projektfiler, HTML-ämnesfiler, innehållsfiler, indexfiler och allt annat du behöver för att sätta ihop ett onlinehjälpsystem eller en webbplats .
* `HTML Help ActiveX-kontroll`: ett litet, modulärt program som används för att infoga hjälpnavigering och sekundära fönsterfunktioner i en HTML-fil.
* `The HTML Help Viewer`: ett fullt fungerande och anpassningsbart trepanelsfönster där onlinehjälpämnen kan visas.
* `Microsoft HTML Help Image Editor`: ett online-grafikverktyg för att skapa skärmdumpar; och för att konvertera, redigera och visa bildfiler.
* `The HTML Help Java Applet`: ett litet, Java-baserat program som kan användas istället för en ActiveX-kontroll för att infoga hjälpnavigering i en HTML-fil.
* `Det körbara programmet HTML Help`: programmet som visar och kör hjälp när du klickar på en kompilerad hjälpfil.
* `HTML-hjälpkompilatorn`: programmet som kompilerar projekt, innehåll, index, ämne och andra filer till en kompilerad hjälpfil.
* `The HTML Help Authoring Guide`: en onlineguide utformad för att hjälpa författare att använda HTML-hjälpen för att designa ett hjälpsystem. Guiden innehåller också en komplett HTML-hjälpreferens för utvecklare och en HTML-taggreferens för författare.

## Referenser

* [Microsoft HTML-hjälp](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

