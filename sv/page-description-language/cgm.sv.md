{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "Fil Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CGM-filformat",
  "description":"Läs mer om CGM-filformat och API:er som kan skapa och öppna CGM-filer.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är en CGM fil? ##

Computer Graphics Metafile (CGM) är gratis, plattformsoberoende, internationell standardmetafilformat för lagring och utbyte av vektorgrafik (2D), rastergrafik och text. CGM använder ett objektorienterat tillvägagångssätt och många funktionsbestämmelser för bildproduktion. CGM använder dessa objektorienterade egenskaper för att omforma grafiska element för att återge en bild. En metafil innehåller nödvändig information som definierar andra filer. I CGM innehåller en textbaserad källfil alla grafiska element som senare kan kompileras till en binär fil. I grund och botten är CGM ett sätt att underlätta 2D-grafiskt datautbyte, oberoende av någon speciell plattform eller enhet.

CGM-formatet tillhandahåller olika element för att utföra funktioner och betecknar objekt för att justera geometriska primitiver och grafisk information. Även om CGM har ersatts av andra format för att visa grafik på webbsidor eftersom det inte stöds väl av webbsidor, är det fortfarande mycket populärt bland industriella, flygtekniska och andra tekniska applikationer. Även om World Wide Web Consortium har utvecklat WebCGM, ett alternativt tillvägagångssätt för användning av CGM på webben. Den primära CGM-implementeringen var en illustration av sekvensen av grundläggande operationer för det grafiska kärnsystemet (GKS). Det har inte anammats särskilt mycket i professionell design men har till stor del ersatts av andra format som DXF och SVG.

## Historik ##

CGM visade sig vara en internationell standard 1987 (ISO 8632-1987) och antogs även som en nationell standard i Storbritannien av BSI och USA av ANSI. Efter ett antal ändringar 1991 släpptes en reviderad standard för CGM 1992 (ISO 8632:1992). 2001 utvecklade World Wide Web Consortium WebCGM med förbättrad förmåga att användas med webbsidorna. 2007 släpptes den andra versionen av WebCGM och den tredje versionen släpptes 2010 med förbättrade möjligheter.

## CGM-filformat ##

Datorgrafik-metafiler är i grunden en databas för grafisk information och tillhandahåller medel för insamling, lagring och överföring av grafisk data. Följaktligen måste det finnas en grafisk systemkomponent för att skapa databasen samtidigt som exekveringen av en applikation i ett metafilformat. I de flesta fall är denna komponent Metafile-generatorn. Vid sidan av det finns ett behov av ytterligare en komponent som kan hämta, tolka och rendera grafisk data i en metafil. Detta behov tillgodoses genom närvaron av en metafiltolk. Följande figur representerar den grafiska metafilens arbetsmiljö.

Förhållandet mellan CGM och andra komponenter i ett typiskt grafiksystem illustreras i ovanstående figur. Det framgår också av figuren att metafilens funktion inte är beroende av den slutliga enhetens utdata.

Generellt finns det två kategorier av metafiler: **sektionsfångst** och **bildfångst**. Den primära funktionen för bildfångstmetafil är att fånga enhetsoberoende, flera bilddefinitioner. Medan session capture använder metafiler systemgränssnittet för att fånga utdatadialogen i ett grafiskt system. CGM tillhör kategorin statiska bildfångstmetafiler. CGM tillhandahåller ett välorganiserat arrangemang av komponenter med en tvånivåstruktur.

1. Metafilbeskrivning
1. En pool av logiskt oberoende bilder

Varje bild är en samling bildbeskrivningar och en bildkropp inklusive en bilddefinition. metafil descriptor definierar beskrivande information som lika gäller alla bilder av den metafilen. Denna information hjälper tolken att korrekt analysera en metafil och känna igen de resurser som krävs för korrekt rendering av en bild. Även om bildbeskrivningen också omsluter den beskrivande informationen kan den bara känna igen bilden där deskriptorn finns. I detta filformat är varje bilddefinition fristående och logiskt suverän. De är oberoende av alla andra bilddefinitioner i en fil. Direkt efter tolkningen av meta-deskriptorn kan bilder nås och tolkas slumpmässigt. Ändring i tillståndet för tidigare bilder har ingen effekt på deras efterföljare. Detta bildoberoende är en annan framträdande egenskap hos CGM.CGM består av koordinatutrymme som är 2D kartesiska koordinater som kallas virtuella enhetskoordinater och kan representeras genom nummer eller precision som representerar räckvidden och granulariteten. CGM specificerar både det direkta urvalet av färger och indexbaserat urval. I det förstnämnda består färgspecifikationen av en RGB-trippel medan senare anger färgspecifikationen ett index till en färgtabell.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
