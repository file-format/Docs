{
"datum": "2023-05-09",
  "keywords": [
"pc3-fil",
"vad är en pc3-fil",
"hur man skapar en pc3-fil i AutoCAD",
"vilket är formatet på pc3-filen",
"vad innehåller pc3-filen",
"fil",
"pc3 filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "PC3-filformat - AutoCAD-plotterkonfigurationsfil",
  "description":"Läs mer om PC3-format och API:er som kan skapa och öppna PC3-filer.",
"linktitle": "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3",
      "parent": "cad"
}
},
"lastmod": "2023-05-09"
}

## Vad är en PC3 fil?

En PC3-fil i AutoCAD är en plotterkonfigurationsfil som innehåller skrivar- eller plotterinställningar för användning i programvara.

När du skapar en ny plotterkonfiguration lagrar AutoCAD all nödvändig information om skrivaren eller plottern i en PC3-fil. Detta inkluderar saker som pappersstorlekar, marginaler, upplösning och andra inställningar som är specifika för skrivaren eller plottern du använder.

Du kan använda PC3-filen för att enkelt ställa in och konfigurera en skrivare eller plotter i AutoCAD. För att använda PC3-filen, välj den från listan över tillgängliga plotterkonfigurationer i dialogrutan Plot.

Du kan också skapa anpassade PC3-filer genom att ändra inställningarna för befintliga PC3-filer eller genom att skapa en ny PC3-fil från början med Plotter Manager i AutoCAD.

## Hur skapar man en PC3-fil i AutoCAD?

För att skapa plotterkonfigurationsfil (PC3) i AutoCAD, följ dessa steg:

1. **Öppna Plotter Manager:** Skriv "PLOTTERMANAGER" på kommandoraden eller gå till "Output"-fliken på menyfliksområdet och välj "Plotter Manager" från "Plot"-panelen.
2. **Klicka på "Add-A-Plotter Wizard":** Detta kommer att starta en guide som guidar dig genom processen att skapa en ny plotterkonfigurationsfil.
3. **Välj plottertillverkare och modell:** Guiden kommer att uppmana dig att välja tillverkare och modell för din skrivare eller plotter från listan. Om din skrivare eller plotter inte finns i listan kan du välja "Den här datorn" och bläddra efter drivrutinsfilen.
4. **Välj en port:** Välj den port som din skrivare eller plotter är ansluten till. Om du är osäker, kontrollera dokumentationen som följde med din skrivare eller plotter.
5. **Ange plotterkonfiguration:** Guiden uppmanar dig att ange olika inställningar för din plotter, såsom pappersstorlek, upplösning och färgdjup. Se till att ställa in dessa alternativ korrekt för din specifika skrivare eller plotter.
6. **Spara plotterkonfiguration:** När du har angett alla inställningar kommer guiden att uppmana dig att ge din nya plotterkonfiguration ett namn. Detta skapar en ny PC3-fil i den mapp som anges av guiden.
7. **Använd den nya plotterkonfigurationen:** För att använda den nya plotterkonfigurationen i AutoCAD, gå till dialogrutan "Plot", välj din nya plotterkonfiguration från listan över tillgängliga plotterkonfigurationer och ställ sedan in din plot som vanliga.

Det är allt! Du har nu skapat en ny plotterkonfigurationsfil (PC3) i AutoCAD som du kan använda för att skriva ut eller plotta dina ritningar.

## Vilket är formatet på PC3-filen?

PC3-filformatet är ett proprietärt filformat som används av Autodesks AutoCAD-programvara. Den innehåller konfigurationsinställningar för specifik plotter eller skrivare, inklusive pappersstorlek, färgdjup, upplösning och andra alternativ.

PC3-filen lagras vanligtvis i mappen "Plotter Configuration" i AutoCADs installationskatalog och den kan enkelt delas mellan användare eller datorer för att säkerställa konsekventa utskrifts- och plottningsinställningar.

PC3-filen är i huvudsak en textfil som innehåller XML-data, vilket är ett maskinläsbart format för att lagra och utbyta data. Du kan visa och redigera innehållet i PC3-filen med hjälp av textredigerare eller XML-redigerare, men det rekommenderas att du använder Plotter Manager i AutoCAD för att göra ändringar i plotterkonfigurationen, eftersom detta kommer att säkerställa att inställningarna är korrekt formaterade och kompatibla med programvaran.

## Vad innehåller PC3-filen?

En PC3-fil i AutoCAD innehåller skrivar- eller plotterkonfigurationsinställningar som är specifika för en viss enhet eller drivrutin. Dessa inställningar används av AutoCAD för att skriva ut eller plotta dina ritningar korrekt och för att säkerställa att de ser ut som du tänkt dig.

Här är några av inställningarna som kan lagras i en PC3-fil:

- **Pappersstorlek:** Detta anger storleken på papper som kommer att användas för utskrift eller plottning, som A4, Letter eller Custom.
- **Plot area:** Detta anger den del av ritningen som kommer att plottas, till exempel hela layouten eller bara ett specifikt fönster.
- **Plotskala:** Det här anger skala för vilken ritning ska skrivas ut eller plottas, till exempel 1:100 eller 1/4"=1'-0".
- **Linjevikt:** Detta anger tjockleken på linjerna i ritningen, vilket påverkar hur de kommer att se ut när de skrivs ut eller plottas.
- **Färgdjup:** Detta anger antalet färger som kommer att användas för utskrift eller plottning, till exempel svartvitt eller fullfärg.
- **Upplösning:** Detta anger upplösning vid vilken ritning kommer att skrivas ut eller plottas, vilket påverkar hur skarp och detaljerad den kommer att se ut.
- **Andra alternativ:** Det finns många andra alternativ som kan ställas in i PC3-filer, såsom utskriftskvalitet, orientering, marginaler, skuggning och mer.

Genom att skapa och använda PC3-fil som innehåller korrekta inställningar för just din skrivare eller plotter kan du säkerställa att dina ritningar skrivs ut eller plottas korrekt och med jämn kvalitet.

## Referenser
* [PC3 i AutoCAD](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)

