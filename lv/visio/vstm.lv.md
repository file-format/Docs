{
  "date" : "2019-10-11",
  "keywords" : [ "vstm file", "vstm file format", "what is a vstm file", "file", "vstm example", "vstm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTM — Microsoft Visio veidnes faila formāts",
  "description":"Uzziniet par VSTM failu formātu un API, kas var izveidot un atvērt VSTM failus.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm-lv",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas ir VSTM fails?

Faili ar paplašinājumu VSTM ir veidņu faili, kas izveidoti ar Microsoft Visio un atbalsta makro. Atšķirībā no VSDX failiem, faili, kas izveidoti no VSTM veidnēm, var palaist makro, kas izstrādāti Visual Basic for Applications (VBA) kodā. Var izveidot veidnes failu, lai nodrošinātu dokumenta pamatiestatījumus, kurus var izmantot turpmāku dokumentu ģenerēšanai ar šiem iestatījumiem. Visio faili tiek izmantoti, lai izveidotu rasējumus, kas satur vizuālus objektus, blokshēmas, UML diagrammas, informācijas plūsmu, organizatoriskās diagrammas, programmatūras diagrammas, tīkla izkārtojumu, datu bāzes modeļus, objektu kartēšanu un citu līdzīgu informāciju. Failus, kas ģenerēti, izmantojot Visio, var arī eksportēt dažādos failu formātos, piemēram, PNG, BMP, PDF un citos.

## Faila formāts ##

VSTM faili ir balstīti uz Open Packaging Conventions un XML, un izstrādātāji var gūt labumu no šī formāta, iemācoties strādāt ar šiem failiem programmatiski. Formāts pārmanto daudzas no tām pašām XML struktūrām, kas ir tās daļas no Visio XML zīmējuma faila formāta (.vdx). Sadarbspēja ar Visio failiem ir ievērojami palielināta, jo trešās puses programmatūra var manipulēt ar Visio failiem faila formāta līmenī.

Katrs Visio fails tiek saukts par pakotni, kurā ir citi faili vai daļas. Pakotnes daļa var būt XML fails, attēls vai pat VBA risinājums. Pakotnē esošās daļas var iedalīt dokumenta un attiecību daļās.

### Dokuments ###

Dokumenta daļās ir ietverts faktiskais Visio faila saturs un metadati, piemēram, faila nosaukums, pirmā lapa un visas tajā esošās formas un pat formu datu savienojumi. Attēli un teksta faili pakotnē tiek uzskatīti par dokumenta daļām.

### Attiecības ###

Visio faila attiecību daļas tiek glabātas mapē _rels, un tajās ir aprakstīts, kā pakotnes daļas ir saistītas ar katru. Tas arī nodrošina faila struktūru. Atsevišķs XML dokuments izmanto elementu vecāku/attēlu attiecības, lai noteiktu entītiju savstarpējo saistību. Derīgs Visio 2013 faila formāts satur pareizo daļu kopu, un pakotnē ir ietvertas attiecības starp daļām.

Attiecību daļas ir XML dokumenti, kas apraksta attiecības starp dažādām pakotnes dokumenta daļām. Tie definē saistību starp diviem vienumiem: norādīto avotu (ko nosaka attiecību faila nosaukums un atrašanās vieta) un norādīto mērķa dokumenta daļu. Piemēram, attiecību daļas tiek izmantotas, lai aprakstītu, kuri formu šabloni ir saistīti ar failu, kā lapas ir saistītas ar failu un viena ar otru vai kā attēli un objekti ir saistīti ar konkrētu lapu.

## Atsauces Nr.

* [Ievads par Visio faila formātu](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


