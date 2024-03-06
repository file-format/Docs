{
  "date" : "2019-10-11",
  "keywords" : [ "vsdm file", "vsdm file format", "what is a vsdm file", "file", "vsdm example", "vsdm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDM — Microsoft Visio zīmēšanas faila formāts",
  "description":"Uzziniet par VSDM faila formātu un API, kas var izveidot un atvērt VSDM failus.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm-lv",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas ir VSDM fails?

Faili ar paplašinājumu .vsdm ir zīmēšanas faili, kas izveidoti, izmantojot programmu Microsoft Visio, kas atbalsta makro. VSDM faili ir OPC/XML rasējumi, kas ir līdzīgi VSDX, bet arī nodrošina iespēju palaist makro, kad fails tiek atvērts. Makro ir lietotāja definētas darbības/soļi, kas izstrādāti programmā Visual Basic for Applications (VBA) un kurus var izmantot, lai veiktu atkārtotus uzdevumus. VSDM faila formāts tika ieviests līdz ar Microsoft Visio 2013 palaišanu. Visio faili tiek izmantoti, lai izveidotu zīmējumus, kas satur vizuālus objektus, blokshēmas, UML diagrammas, informācijas plūsmu, organizācijas diagrammas, programmatūras diagrammas, tīkla izkārtojumu, datu bāzes modeļus, objektu kartēšanu un citus. līdzīga informācija. Failus, kas ģenerēti, izmantojot Visio, var arī eksportēt dažādos failu formātos, piemēram, [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) un citos.

## VSDM faila formāts

VSDM faili ir balstīti uz atvērtā iepakojuma konvencijām un XML, un izstrādātāji var gūt labumu no šī formāta, iemācoties strādāt ar šiem failiem programmatiski. Formāts pārmanto daudzas no tām pašām XML struktūrām, kas ir tās daļas no Visio XML zīmējuma faila formāta (.vdx). Sadarbspēja ar Visio failiem ir ievērojami palielināta, jo trešās puses programmatūra var manipulēt ar Visio failiem faila formāta līmenī.

Katrs Visio fails tiek saukts par pakotni, kurā ir citi faili vai daļas. Pakotnes daļa var būt XML fails, attēls vai pat VBA risinājums. Pakotnē esošās daļas var iedalīt dokumenta un attiecību daļās.

### Dokuments ###

Dokumenta daļās ir ietverts faktiskais Visio faila saturs un metadati, piemēram, faila nosaukums, pirmā lapa un visas tajā esošās formas un pat formu datu savienojumi. Attēli un teksta faili pakotnē tiek uzskatīti par dokumenta daļām.

### Attiecības ###

Visio faila attiecību daļas tiek glabātas mapē \_rels, un tajās ir aprakstīts, kā pakotnes daļas ir saistītas ar katru. Tas arī nodrošina faila struktūru. Atsevišķs XML dokuments izmanto elementu vecāku/attēlu attiecības, lai noteiktu entītiju savstarpējo saistību. Derīgs Visio 2013 faila formāts satur pareizo daļu kopu, un pakotnē ir ietvertas attiecības starp daļām.

Attiecību daļas ir XML dokumenti, kas apraksta attiecības starp dažādām pakotnes dokumenta daļām. Tie definē saistību starp diviem vienumiem: norādīto avotu (ko nosaka attiecību faila nosaukums un atrašanās vieta) un norādīto mērķa dokumenta daļu. Piemēram, attiecību daļas tiek izmantotas, lai aprakstītu, kuri formu šabloni ir saistīti ar failu, kā lapas ir saistītas ar failu un viena ar otru vai kā attēli un objekti ir saistīti ar konkrētu lapu.

## Atsauces Nr.

* [Ievads par Visio faila formātu](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


