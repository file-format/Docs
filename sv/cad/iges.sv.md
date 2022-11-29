{
  "date" : "2020-03-16",
  "keywords" :[ "IGES-fil", "Filformat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om IGES-filformat och API:er som kan skapa och öppna IGES-filer.",
  "title" :"IGES filformat",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Vad är en IGES fil?

En fil med tillägget .iges används för att utbyta designinformation mellan datorstödd design (CAD)-applikationer. IGES står för Initial Graphics Exchange Specifications. Information som utbyts med IGES inkluderar kretsschema, trådram, friformsyta eller solida modelleringsrepresentationer. IGES hittar sina tillämpningar i traditionella tekniska ritningar, modellanalys och tillverkningsfunktioner. Formatet kan utbyta både 2D- eller 3D-designinformation mellan CAD-program. IGES-filer kan öppnas med flera CAD-applikationer som Autodesk och CADSoftTools ABViewer. Det finns också flera API:er tillgängliga för att öppna och konvertera IGES-filer programmatiskt.

## IGES filformat

IGES-filer är i ASCII-textformat och kan öppnas i valfri textredigerare för att se innehållet i filen. Textinformation i en IGES-fil representeras i "Hollerith"-format. En vanlig IGES-fil kan innehålla tusentals rader för att representera 2D- eller 3D-informationen som kan utbytas enligt detta format. En IGES-fil är uppdelad i fem sektioner, betecknade med den specifika versaler i den 73:e kolumnen. Dessa sektioner är "Start" (S), "Global" (G), "Data Entry" (D), "Parameter Data" (P) och "Terminate" (T) sektioner. Datainmatnings- och parameterdatasektionerna förkortas vanligtvis DE respektive PD.

### IGES-filhuvud

Avsnitten Start och Global innehåller grundläggande information om:
* Namn på filen och dess källa
* Avgränsare för avsnittet Parameterdata
* Författare till filen och annan allmän information.

Start- och Globala avsnitt från exempeldokumentet på Wikipedia är som följer.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Som kan ses innehåller startfältet läsbara beskrivningar av filen, och min har några tecken i kolumnerna 1-72, med raden som slutar med avsnittshuvudet och avsnittsradnumret. Det måste finnas minst en rad i startsektionen. Den globala sektionen innehåller förbearbetningsdata. Den måste också finnas i filen och sluta med formatet G000000#.

### Datainmatning (DE) och Parameter Data (PD) sektion

#### Datainmatningssektion
En IGES-fil består av flera enheter som innehåller informationen om grunddata för IGES-filformatet. En entitet innehåller information om olika element i ett IGES-dataformat och används för ritning. Mer vanligt använda enheter inkluderar:
* Cirkelbåge
* Sammansatt kurva
* Konisk båge
* Plan
* Linje

Dessa är bara några och det finns cirka 150 olika enheter i IGES. Varje enhet identifieras med ett typnummer som:
* CIRKULÄR BÅGE(Typ 100)
* LINE (Typ 110)

##### Entitetsegenskaper

Varje deklarerad enhet har följande egenskaper.

|Fältnamn|Beskrivning|
---|---|
|Entitetstyp |Detta är den typ av enhet som beskrivs. Till exempel beskriver 116 en punktenhet.|
|PD-pekare |Detta anger platsen för denna enhetsdata i avsnittet Parameterdata. Denna plats är helt enkelt radnumret inuti PD-sektionen som har den första raden av denna enhetsdata.|
|Struktur |Noll eller pekare till definitionsenhet. Ej tillämpligt för de flesta enheter|
|Linjeteckensnittsmönster| Nummer eller pekare till linjetypsnittsmönsterenhet. Tal betyder: * 0 Inget mönster specificerat (standard) * 1 Heldragen * 2 Streckad * 3 Fantom * 4 Mittlinje * 5 Prickade|
|Nivå| Anger nivåer som ska associeras med denna enhet. Tillåter att entitet visas på mer än en nivå|
|Visa| Anger visningsalternativ. Dessa är: 0 Indikerar lika synlighet och egenskaper i alla vyer. Standardpekare till View-entiteten (Typ 410) som den kan ses från Reference a View Visible Associativity-entitet (Typ 402, Form 3)
|Transformationsmatrispekare| Refererar till en transformationsmatrisentitet (typ 124) eller är noll som standard (ingen transformation)|
|Label Display Associativity| Refererar till en Label Display Associativity (Typ 402, Form 5) som definierar hur enhetsetiketten visas.|
|Statusnummer| Innehåller fyra sektioner med två nummer. 1-2: Tom status. Antingen 00 för normal eller 01 för blank. 3-4: Underordnad enhetsomkopplare: är 00 för oberoende, 01 för fysiskt beroende, 02 för logiskt beroende och 03 för båda. 5-6: Enhetsanvändningsflagga: är antingen 00 för geometri, 01 för anteckning, 02 för definition, 03 för Annat, 04 för logisk, 05 för 2D-parametrisk och 06 för konstruktionsgeometri. Slutligen är 7-8 hierarkin, där 00 indikerar globalt uppifrån och ned (använd denna entitets egenskaper), 01 är global defer (använd inte denna entitets egenskaper) och 02 är use hierarchy property (använd Hierarchy Entity (Typ 406, Form) 10)för att bestämma egenskaper hos hierarkisk gruppering).|
|Sekvensnummer| Specificeras av D#, där # är radnumret för denna sektion (inte från toppen av filen). Detta används också för att peka på denna datainmatningsenhet.|
|Enhetstyp| det anges två gånger per enhetslista|
|Linjeviktsnummer| Anger tjocklek när entitet visas. Minsta är 1, 0 är standard|
|Färgnummer| Anger enhetsfärgen. Tillåtna heltalsvärden är: 0 Ingen färg (standard) 1 Svart 2 Röd 3 Grön 4 Blå 5 Gul 6 Magenta 7 Cyan 8 Vit|
|Parameter Rad Antal Antal| Anger antalet rader som denna enhet tar upp i Parameter Data Section|
|Formnummer| Indikerar formen eller representationen av denna enhet. Ändrar hur parameterdata tolkas. Standard är 0|
|Reserverat fält| Ej använd|
|Reserverat fält| Ej använd|
|Enhetsetikett| Applikationsspecificerad identifierare- rättighet motiverad|
|Subscript Number| Numerisk kvalificerare för enhetsetiketten. Båda bildar tillsammans en unik identifierare för entiteten|
|Sekvensnummer Se ovan. |Detta blir D#+1, eftersom varje enhet är specificerad på två rader.|

#### Parameter Data Sektion
Avsnittet Datainmatningar följs av avsnittet Parameterdata. Den listar data för varje respektive post och listar parametrar för entiteten baserat på de avgränsare som anges i avsnittet Global (vanligtvis kommatecken för att separera parametrar och ett semikolon för att avsluta listningen).


## Referenser
* [IGES av WikiPedia](https://en.wikipedia.org/wiki/IGES)

