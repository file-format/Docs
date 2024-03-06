{
  "date" : "2019-10-11",
  "keywords" : [ "vstx file", "vstx file format", "what is a vstx file", "file", "vstx example", "vstx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTX — Microsoft Visio faila formāts",
  "description":"Uzziniet par VSTX faila formātu un API, kas var izveidot un atvērt VSTX failus.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx-lv",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas ir VSTX fails?

Faili ar .vstx paplašinājumiem ir zīmēšanas veidņu faili, kas izveidoti ar Microsoft Visio 2013 un jaunāku versiju. Šie VSTX faili nodrošina sākuma punktu Visio rasējumu izveidei, kas saglabāti kā [.VSDX](/visio/vsdx/) faili ar noklusējuma izkārtojumu un iestatījumiem. Parasti Visio faili tiek izmantoti, lai izveidotu rasējumus, kas satur vizuālus objektus, blokshēmas, UML diagrammas, informācijas plūsmu, organizatoriskās diagrammas, programmatūras diagrammas, tīkla izkārtojumu, datu bāzes modeļus, objektu kartēšanu un citu līdzīgu informāciju. Failus, kas ģenerēti, izmantojot Visio, var arī eksportēt dažādos failu formātos, piemēram, [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) un citos. Programmas, kas atver VSTX failus, ietver Microsoft Visio operētājsistēmai Windows un Mac, kas ļauj atvērt šos failus apskatei un rediģēšanai. Tas arī ļauj konvertēt Visio failu formātus uz vairākiem citiem formātiem.

# VSTX faila formāts #

X faila paplašinājumā attiecas uz OpenOffice faila formātu, ko Microsoft ieviesa kā [ZIP](/compression/zip/) arhīva faila formātu, lai aizstātu iepriekš atbalstītos bināro failu formātus. Tādējādi VSTX faili ir balstīti uz OpenOffice specifikāciju XML faila formātu, atšķirībā no [.VST](/visio/vst/) faila formāta, kas ir binārā formātā.

VSDX faili ir balstīti uz atvērtā iepakojuma konvencijām un XML, un izstrādātāji var gūt labumu no šī formāta, iemācoties strādāt ar šiem failiem programmatiski. Formāts pārmanto daudzas no tām pašām XML struktūrām, kas ir tās daļas no Visio XML zīmējuma faila formāta (.vdx). Sadarbspēja ar Visio failiem ir ievērojami palielināta, jo trešās puses programmatūra var manipulēt ar Visio failiem faila formāta līmenī.

Daži citi failu tipi, kas ietver Visio 2013 faila formātu, ietver:

* .vsdm (zīmējums ar iespējotu Visio makro)

* .vssx (Visio trafarets)

* .vssm (Visio makro iespējots trafarets)

* .vstx (Visio veidne)

* .vstm (Visio makro iespējota veidne)


Visio 2013 faila formāts zem pārsega izmanto strukturētus līdzekļus, lai saglabātu lietojumprogrammu datus kopā ar saistītajiem resursiem arhīvā, piemēram, [ZIP](/compression/zip/). ZIP failu var izvilkt, izmantojot jebkuru standarta ekstrakcijas utilītu, ja tajā ir arī cita veida faili. Varat vienkārši aizstāt .VSTX faila paplašinājumu ar .ZIP programmā Windows Explorer, lai skatītu VSTX faila saturu.

Katrs Visio fails tiek saukts par pakotni, kurā ir citi faili vai daļas. Pakotnes daļa var būt XML fails, attēls vai pat VBA risinājums. Pakotnē esošās daļas var iedalīt dokumenta un attiecību daļās.

### Dokuments ###

Dokumenta daļās ir ietverts faktiskais Visio faila saturs un metadati, piemēram, faila nosaukums, pirmā lapa un visas tajā esošās formas un pat formu datu savienojumi. Attēli un teksta faili pakotnē tiek uzskatīti par dokumenta daļām.

### Attiecības ###

Visio faila attiecību daļas tiek glabātas mapē _rels, un tajās ir aprakstīts, kā pakotnes daļas ir saistītas ar katru. Tas arī nodrošina faila struktūru. Atsevišķs XML dokuments izmanto elementu vecāku/attēlu attiecības, lai noteiktu entītiju savstarpējo saistību. Derīgs Visio 2013 faila formāts satur pareizo daļu kopu, un pakotnē ir ietvertas attiecības starp daļām.

Attiecību daļas ir XML dokumenti, kas apraksta attiecības starp dažādām pakotnes dokumenta daļām. Tie definē saistību starp diviem vienumiem: norādīto avotu (ko nosaka attiecību faila nosaukums un atrašanās vieta) un norādīto mērķa dokumenta daļu. Piemēram, attiecību daļas tiek izmantotas, lai aprakstītu, kuri formu šabloni ir saistīti ar failu, kā lapas ir saistītas ar failu un viena ar otru vai kā attēli un objekti ir saistīti ar konkrētu lapu.

## Atsauces Nr.

* [Ievads par Visio faila formātu](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


