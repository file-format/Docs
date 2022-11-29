{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Filformat", "Öppna", "Läs", "Skapa", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om HPGL-filformat och API:er som kan skapa och öppna HPGL-filer.",
  "title" :"HPGL-filformat - Lär dig av filformatsexperter!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Vad är en HPGL fil?

En HPGFL-fil (Hewlett-Packard Graphics Language) innehåller instruktionsuppsättningar för plotterstyrning av utvecklad av HP. HP plottrar använder den här filen för att rita och skriva ut vektor- och rasterinnehåll på papperet.

### HPGL-kommando

Ett HPGL-kommando består av följande.
* En kommandosektion av alfabetet med två tecken
* En parametersektion
* Terminator sektion

Varje parameter i filen måste delas med en separator vid flera parametrar.

### HPGL-kommandoexempel

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinatsystem

Koordinatsystem består av 2-dimensionella mätindikatorer för att lokalisera vilken specifik plats som helst. HPGL använder både plotterkoordinatsystem och användarkoordinatsystem för detta ändamål.

#### Plotterkoordinatsystem

Detta koordinatsystem används för att plotta ritningar baserade på plotterrörelse. En typisk XY-enhet med minsta plotterrörelse är 0,025 mm. Det möjliga utbudet av ritningar ändras med plottertyper.

#### Användarkoordinatsystem

Användarspecificerat koordinatsystem kan ställas in med hjälp av skala och ursprung. Dessa konverteras till plotterkoordinater med hjälp av IP-kommandot och SC-kommandot. Plottersystemkoordinater används som standard om denna konvertering inte utförs.

## HPGL filformat
HPGL-filer är i ASCII-format (textfil) och börjar med några installationskommandon. Detta ställer in vissa parametrar för plottern för plottning. En typisk HPGL-fil ser ut som följer.

|Kommando|Betydning
---|---|
|IN;|initiera, starta ett plottningsjobb|
|IP;|ställ in skalningspunkterna (P1 och P2) till deras standardpositioner|
|SP1;|välj penna 1|
|PU0,0;|lyft upp pennan och flytta till startpunkten för nästa åtgärd|
|PD100,0,100,100,0,100,0,0;|lägg ner pennan och flytta till följande platser (rita en ruta runt sidan)|
|PU50,50;|Pen upp och flytta till X,Y koordinater 50,50|
|CI25;|rita en cirkel med radien 25|
|SS;|välj standardteckenuppsättningen|
|DT*,1;|ställ textavgränsaren till asterisken och skriv inte ut dem (1:an, som betyder "sant")|
|PU20,80;|lyft pennan och flytta till 20,80|
|LBHello World*;|rita en etikett|

## Referenser
* [HPGL av Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL Referensguide](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

