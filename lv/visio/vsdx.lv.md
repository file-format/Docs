{
  "date" : "2019-10-11",
  "keywords" : [ "vsdx file", "vsdx file format", "what is a vsdx file", "file", "vsdx example", "vsdx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDX",
  "description":"Uzziniet par VSDX failu formātu un API, kas var izveidot un atvērt VSDX failus.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx-lv",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas ir VSDX fails?

Faili ar paplašinājumu .vsdx ir Microsoft Visio faila formāts, kas ieviests no Microsoft Office 2013. Tas tika izstrādāts, lai aizstātu bināro faila formātu [.VSD](/visio/vsd/), ko atbalsta vecākas Microsoft Visio versijas. To atbalsta arī visio pakalpojumi programmā Microsoft SharePoint Server 2013, un publicēšanai SharePoint Server nav nepieciešams starpnieka faila formāts. Visio faili tiek izmantoti, lai izveidotu rasējumus, kas satur vizuālus objektus, blokshēmas, UML diagrammas, informācijas plūsmu, organizatoriskās diagrammas, programmatūras diagrammas, tīkla izkārtojumu, datu bāzes modeļus, objektu kartēšanu un citu līdzīgu informāciju. Failus, kas ģenerēti, izmantojot Visio, var arī eksportēt dažādos failu formātos, piemēram, [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) un citos.

## Faila formāts ##

VSDX faili ir balstīti uz atvērtā iepakojuma konvencijām un XML, un izstrādātāji var gūt labumu no šī formāta, iemācoties strādāt ar šiem failiem programmatiski. Formāts pārmanto daudzas no tām pašām XML struktūrām, kas ir tās daļas no Visio XML zīmējuma faila formāta (.vdx). Sadarbspēja ar Visio failiem ir ievērojami palielināta, jo trešās puses programmatūra var manipulēt ar Visio failiem faila formāta līmenī.

Daži citi failu tipi, kas ietver Visio 2013 faila formātu, ietver:

* .vsdm (zīmējums ar iespējotu Visio makro)

* .vssx (Visio trafarets)

* .vssm (Visio makro iespējots trafarets)

* .vstx (Visio veidne)

* .vstm (Visio makro iespējota veidne)


Visio 2013 faila formāts zem pārsega izmanto strukturētus līdzekļus, lai saglabātu lietojumprogrammu datus kopā ar saistītajiem resursiem arhīvā, piemēram, [ZIP](/compression/zip/). ZIP failu var izvilkt, izmantojot jebkuru standarta ekstrakcijas utilītu, ja tajā ir arī cita veida faili. Varat vienkārši aizstāt .vsdx faila paplašinājumu ar .zip programmā Windows Explorer, lai skatītu VSDX faila saturu.

Katrs Visio fails tiek saukts par pakotni, kurā ir citi faili vai daļas. Pakotnes daļa var būt XML fails, attēls vai pat VBA risinājums. Pakotnē esošās daļas var iedalīt dokumenta un attiecību daļās.

### Dokuments ###

Dokumenta daļās ir ietverts faktiskais Visio faila saturs un metadati, piemēram, faila nosaukums, pirmā lapa un visas tajā esošās formas, un pat formu datu savienojumi. Attēli un teksta faili pakotnē tiek uzskatīti par dokumenta daļām.

### Attiecības ###

Visio faila attiecību daļas tiek glabātas mapē \_rels, un tajās ir aprakstīts, kā pakotnes daļas ir saistītas ar katru. Tas arī nodrošina faila struktūru. Atsevišķs XML dokuments izmanto elementu vecāku/attēlu attiecības, lai noteiktu entītiju savstarpējo saistību. Derīgs Visio 2013 faila formāts satur pareizo daļu kopu, un pakotnē ir ietvertas attiecības starp daļām.

Attiecību daļas ir XML dokumenti, kas apraksta attiecības starp dažādām pakotnes dokumenta daļām. Tie definē saistību starp diviem vienumiem: norādīto avotu (ko nosaka attiecību faila nosaukums un atrašanās vieta) un norādīto mērķa dokumenta daļu. Piemēram, attiecību daļas tiek izmantotas, lai aprakstītu, kuri formu šabloni ir saistīti ar failu, kā lapas ir saistītas ar failu un viena ar otru vai kā attēli un objekti ir saistīti ar konkrētu lapu.

## Atsauces Nr.

* [Ievads par Visio faila formātu](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


