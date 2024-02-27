{
  "date": "2020-03-16",
  "keywords": [
"IGES fil",
"Filformat",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om IGES filformat og API'er, der kan oprette og åbne IGES filer.",
  "title": "IGES filformat",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-das"
}
},
  "lastmod": "2020-07-28"
}

## Hvad er en IGES fil?

En fil med filtypenavnet .iges bruges til at udveksle designoplysninger mellem computerstøttet design (CAD) applikationer. IGES står for Initial Graphics Exchange Specifications. Informationer, der udveksles ved hjælp af IGES, omfatter kredsløbsdiagram, wireframe, freeform overflade eller solide modelleringsrepræsentationer. IGES finder sine anvendelser i traditionelle tekniske tegninger, modelanalyse og produktionsfunktioner. Formatet kan udveksle både 2D- eller 3D-designoplysninger mellem CAD-programmer. IGES-filer kan åbnes med flere CAD-applikationer såsom Autodesk og CADSoftTools ABViewer. Der er også flere tilgængelige API'er til at åbne og konvertere IGES-filer programmatisk.

## IGES filformat

IGES-filer er i ASCII-tekstformat og kan åbnes i enhver teksteditor for at se indholdet af filen. Tekstinformation i en IGES-fil er repræsenteret i Hollerith-format. En almindelig IGES-fil kan indeholde tusindvis af linjer til at repræsentere 2D- eller 3D-informationen, der kan udveksles i henhold til dette format. En IGES-fil er opdelt i fem sektioner, angivet med det specifikke store bogstav i den 73. kolonne. Disse sektioner er 'Start' (S), 'Global' (G), 'Data Entry' (D), 'Parameter Data' (P) og 'Terminate' (T) sektioner. Sektionerne Data Entry og Parameter Data er almindeligvis forkortet til henholdsvis DE og PD.

### IGES-filoverskrift

Start- og Globalsektionerne indeholder grundlæggende oplysninger om:
 * Navnet på filen og dens kilde
 * Afgrænsningstegn for afsnittet Parameterdata
 * Forfatteren af filen og andre generelle oplysninger.

Start- og Globalsektioner fra eksempeldokumentet på Wikipedia er som følger.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Dataindtastning (DE) og Parameter Data (PD) sektion

#### Dataindtastningssektion
En IGES-fil består af flere entiteter, der indeholder oplysningerne om de grundlæggende data i IGES-filformatet. En enhed indeholder information om forskellige elementer i et IGES-dataformat og bruges til tegning. Mere almindeligt anvendte enheder omfatter:
 * Cirkulær bue
 * Sammensat kurve
 * Keglebue
 * Fly
 * Linje

Dette er blot nogle få, og der er omkring 150 forskellige enheder i IGES. Hver enhed er identificeret med et typenummer såsom:
 * CIRKULÆR bue(type 100)
 * LINE (Type 110)

##### Enhedsegenskaber

Hver deklarerede enhed har følgende egenskaber.

|Feltnavn|Beskrivelse|
---|---|
|Entity Type |Dette er den type enhed, der beskrives. For eksempel beskriver 116 en punkt-entitet.|
|PD pointer |Dette angiver placeringen af disse entitetsdata i Parameter Data sektionen. Denne placering er simpelthen linjenummeret inde i PD-sektionen, der har den første linje af denne enhedsdata.|
|Struktur |Nul eller pointer til definitionsenhed. Ikke relevant for de fleste enheder|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Intet mønster angivet (standard) * 1 Solid * 2 Stiplet * 3 Phantom * 4 Centerline * 5 Stiplet|
|Niveau| Angiver niveauer, der skal knyttes til denne enhed. Tillader entitet at blive vist på mere end ét niveau|
|Se| Angiver visningsmuligheder. Disse er: 0 Angiver lige synlighed og karakteristika i alle visninger. Standardmarkør til View-entiteten (Type 410), som den kan ses fra Reference a View Visible Associativity-entitet (Type 402, Form 3)
|Transformation Matrix pointer| Refererer til en transformationsmatrixentitet (Type 124) eller er nul som standard (ingen transformation)|
|Label Display Associativity| Refererer til en etiketvisningsassociativitet (type 402, formular 5), som definerer, hvordan enhedsetiketten vises.|
|Statusnummer| Indeholder fire sektioner af to numre. 1-2: Blank status. Enten 00 for normal eller 01 for blanked. 3-4: Underordnet enhedsomskifter: er 00 for uafhængig, 01 for fysisk afhængig, 02 for logisk afhængig og 03 for begge. 5-6: Entity Use flag: er enten 00 for geometri, 01 for annotation, 02 for definition, 03 for Other, 04 for Logical, 05 for 2D parametrisk og 06 for konstruktionsgeometri. Endelig er 7-8 hierarkiet, hvor 00 angiver global top-down (brug denne enheds karakteristika), 01 er global defer (brug ikke denne enheds karakteristika), og 02 er brug hierarkiegenskab (brug Hierarchy Entity (Type 406, Formular) 10)at bestemme karakteristika ved hierarkisk gruppering).|
|Sekvensnummer| Specificeret af D#, hvor # er linjenummeret for denne sektion (ikke fra toppen af filen). Dette bruges også til at pege på denne dataindtastningsenhed.|
|Enhedstype| det er angivet to gange pr. enhedsfortegnelse|
|Linjevægt nummer| Angiver tykkelse ved visning af enhed. Mindste er 1, 0 er standard|
|Farvenummer| Angiver enhedsfarven. Tilladte heltalsværdier er: 0 Ingen farve (standard) 1 Sort 2 Rød 3 Grøn 4 Blå 5 Gul 6 Magenta 7 Cyan 8 Hvid|
|Parameterlinjetællernummer| Angiver antallet af linjer, som denne enhed optager i Parameter Data Section|
|Formularnummer| Angiver formen eller repræsentationen af denne enhed. Ændrer, hvordan parameterdata fortolkes. Standard er 0|
|Reserveret felt| Ikke brugt|
|Reserveret felt| Ikke brugt|
|Enhedsmærke| Applikationsspecificeret identifikator- retfærdiggjort|
|Underskriftsnummer| Numerisk kvalifikation for enhedsetiketten. Begge danner tilsammen en unik identifikator for entiteten|
|Sekvensnummer Se ovenfor. |Dette vil være D#+1, da hver enhed er angivet på to linjer.|

#### Parameter Data Sektion
Sektionen Dataindtastninger efterfølges af sektionen Parameterdata. Den lister dataene for hver respektive post og lister parametrene for objektet baseret på de afgrænsningstegn, der er angivet i den globale sektion (normalt kommaer for at adskille parametre og et semikolon for at afslutte listen).


## Referencer
 * [IGES af WikiPedia](https://en.wikipedia.org/wiki/IGES)

