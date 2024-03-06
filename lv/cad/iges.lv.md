{
  "date": "2020-03-16",
  "keywords": [
"IGES fails",
"Faila formāts",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par IGES faila formātu un API, kas var izveidot un atvērt IGES failus.",
  "title": "IGES faila formāts",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-lvs"
}
},
  "lastmod": "2020-07-28"
}

## Kas ir IGES fails?

Fails ar paplašinājumu .iges tiek izmantots, lai apmainītos ar dizaina informāciju starp datorizētās projektēšanas (CAD) lietojumprogrammām. IGES apzīmē Initial Graphics Exchange Specifications. Informācija, ar kuru tiek apmainīta, izmantojot IGES, ietver shēmas diagrammu, stiepļu rāmi, brīvas formas virsmu vai cietās modelēšanas attēlojumus. IGES atrod savu pielietojumu tradicionālajos inženiertehniskajos rasējumos, modeļu analīzē un ražošanas funkcijās. Formāts var apmainīties gan ar 2D, gan 3D dizaina informāciju starp CAD programmām. IGES failus var atvērt ar vairākām CAD lietojumprogrammām, piemēram, Autodesk un CADSoftTools ABViewer. Ir pieejamas arī vairākas API, lai programmatiski atvērtu un konvertētu IGES failus.

## IGES faila formāts

IGES faili ir ASCII teksta formātā, un tos var atvērt jebkurā teksta redaktorā, lai skatītu faila saturu. Teksta informācija IGES failā ir attēlota Hollerith formātā. Kopējā IGES failā var būt tūkstošiem rindu, kas attēlo 2D vai 3D informāciju, ar kuru var apmainīties saskaņā ar šo formātu. IGES fails ir sadalīts piecās sadaļās, kas apzīmētas ar īpašo lielo burtu 73. slejā. Šīs sadaļas ir sadaļas Sākt (S), Globālais (G), Datu ievade (D), Parametru dati (P) un Izbeigt (T). Datu ievades un parametru datu sadaļas parasti tiek saīsinātas attiecīgi DE un PD.

### IGES faila galvene

Sadaļās Sākt un Globālajā ir ietverta pamatinformācija par:
 * Faila nosaukums un tā avots
 * Sadaļas Parametru dati norobežotāji
 * Faila autors un cita vispārīga informācija.

Sākuma un globālās sadaļas no Wikipedia parauga dokumenta ir šādas.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Datu ievades (DE) un parametru datu (PD) sadaļa

#### Datu ievades sadaļa
IGES fails sastāv no vairākām entītijām, kas satur informāciju par IGES faila formāta pamatdatiem. Entītija satur informāciju par dažādiem IGES datu formāta elementiem un tiek izmantota zīmēšanai. Biežāk izmantotās entītijas ir:
 * Apļveida loks
 * Saliktā līkne
 * Koniskā loka
 * Lidmašīna
 * Līnija

Tie ir tikai daži, un IGES ir aptuveni 150 dažādu entītiju. Katru entītiju identificē ar tipa numuru, piemēram:
 * APĻA LOKA (100. tips)
 * LINE (110. tips)

##### Entītijas rekvizīti

Katrai deklarētajai vienībai ir šādas īpašības.

|Lauka nosaukums|Apraksts|
---|---|
|Entītijas veids |Šis ir aprakstītās entītijas veids. Piemēram, 116 apraksta punkta entītiju.|
|PD rādītājs |Tas norāda šo entītiju datu atrašanās vietu sadaļā Parametru dati. Šī vieta ir vienkārši rindas numurs PD sadaļā, kurā ir šī entītijas datu pirmā rinda.|
|Struktūra |Nulle vai rādītājs uz definīcijas entītiju. Nav piemērojams lielākajai daļai entītiju|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Nav norādīts raksts (noklusējums) * 1 Nepārtraukts * 2 Pārtraukts * 3 Fantoma * 4 Viduslīnija * 5 Punktēta|
|Līmenis| Norāda līmeņus, kas jāsaista ar šo entītiju. Ļauj entītijai parādīties vairāk nekā vienā līmenī|
|Skatīt| Norāda skatīšanas opcijas. Tie ir: 0 Norāda vienādu redzamību un raksturlielumus visos skatos. Noklusējuma rādītājs uz entītiju Skats (410. tips), ko var skatīt no atsauces uz skata redzamās asociācijas entītiju (402. tips, 3. veidlapa)
|Transformācijas matricas rādītājs| Atsaucas uz transformācijas matricas entītiju (124. tips) vai pēc noklusējuma ir nulle (bez transformācijas)|
|Etiķetes attēlojuma saistība| Atsauces uz etiķetes attēlojuma asociativitāti (402. tips, 5. veidlapa), kas nosaka, kā tiek parādīta entītijas etiķete.|
|Statusa numurs| Satur četras divu skaitļu sadaļas. 1-2: tukšs statuss. Vai nu 00, lai atbilstu normālam vai 01, lai izslēgtu. 3-4: pakārtotās entītijas slēdzis: ir 00 neatkarīgiem, 01 fiziski atkarīgiem, 02 loģiski atkarīgiem un 03 abiem. 5-6: entītijas izmantošanas karodziņš: ir vai nu 00 ģeometrijai, 01 anotācijai, 02 definīcijai, 03 citam, 04 loģiskam, 05 2D parametram un 06 konstrukcijas ģeometrijai. Visbeidzot, 7-8 ir hierarhija, kur 00 apzīmē globālu no augšas uz leju (izmantojiet šīs entītijas īpašības), 01 ir globālā atlikšana (neizmantojiet šīs entītijas raksturlielumus) un 02 ir izmantot hierarhijas rekvizītu (izmantojiet hierarhijas entītiju (tips 406, forma). 10)noteikt hierarhiskās grupēšanas pazīmes).|
|Secības numurs| Norāda ar D#, kur # ir šīs sadaļas rindas numurs (nevis no faila augšdaļas). To izmanto arī, lai norādītu uz šo datu ievades entītiju.|
|Entītijas veids| tas ir norādīts divas reizes katrā entītijas sarakstā|
|Līnijas svara numurs| Norāda biezumu, parādot entītiju. Mazākais ir 1, 0 ir noklusējuma|
|Krāsu numurs| Norāda entītijas krāsu. Atļautās veselo skaitļu vērtības ir: 0 Bez krāsas (noklusējums) 1 Melns 2 Sarkans 3 Zaļš 4 Zils 5 Dzeltens 6 Fuksīns 7 Ciāna 8 Balts|
|Parameter Line Count Number | Norāda rindu skaitu, ko šī entītija aizņem parametru datu sadaļā|
|Veidlapas numurs| Norāda šīs entītijas formu vai atveidojumu. Maina parametru datu interpretāciju. Noklusējums ir 0|
|Rezervēts lauks| Nav lietots|
|Rezervēts lauks| Nav lietots|
|Entity Label| Lietojumprogrammas norādītais identifikators- tiesības pamatots|
|Apakšraksta numurs| Entītijas etiķetes skaitliskais kvalifikators. Abi kopā veido unikālu entītijas identifikatoru|
|Secības numurs Skatīt iepriekš. |Tas būs D#+1, jo katra entītija ir norādīta divās rindās.|

#### Parametru datu sadaļa
Datu ievades sadaļai seko sadaļa Parametru dati. Tajā ir norādīti katra attiecīgā ieraksta dati un entītijas parametri, pamatojoties uz norobežotājiem, kas norādīti sadaļā Globālais (parasti ar komatiem, lai atdalītu parametrus, un ar semikolu, lai beigtu sarakstu).


## Atsauces
 * [IGES no WikiPedia](https://en.wikipedia.org/wiki/IGES)

