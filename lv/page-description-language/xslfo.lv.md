{
  "date": "2019-10-11",
  "keywords": [
"XSLFO",
"XSL formatēšanas objekti",
"Fails",
"Pagarinājums",
"Faila formāts",
"Paplašināma stila lapu valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "Uzziniet par XSLFO faila formātu un API, kas var izveidot un atvērt XSLFO failus.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslf-lvo"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir XSL-FO fails? ##

XSL-FO (XSL formatēšanas objekti) ir jaudīga stila lapu valoda XML dokumentu formatēšanai. Papīra un drukas ierobežotās formas semantiku izsaka XSL-FO, kad izmēri ir fiksēti. Atšķirībā no HTML, kas attēlo pārlūkprogrammas loga neierobežotās formas semantiku ar mainīgiem izmēriem. XSL-FO formatētie XML dokumenti galvenokārt tiek izmantoti PDF failu ģenerēšanai. XSL (Extensible Stylesheet Language) ir ar funkcijām pilnu W3C tehnoloģiju kopums, kas paredzēts XML dokumentu un šīs valodas XSL-FO daļas formatēšanai un apmaiņai. XSLT un XPath ir arī citas XSL daļas.

Tiek ierosināts XML dokumentus vispirms pārveidot par XSL-FO, PDF ir šī kritērija piemērs. PDF formātā rezultāti tiek renderēti, izmantojot XSLTfirst un pēc tam XSL-FO formatētāju. Šādā veidā XML dokumentus var formatēt nejauši. Lai gan XSL-FO izmanto priekšrocības, ko sniedz kaskādes stila lapas (CSS) rekvizītu izmantošana un to paplašināšana, kur vien tas ir nepieciešams reālajam formātam, tajā ir nodrošinātas lappušu veidnes, ko XSL-FO terminoloģijā sauc par lapu šabloniem. XSL-FO nodrošina arī diezgan sarežģītu dokumentu formatējumu un atbalsta indeksu ģenerēšanu.

## Vēsture un pamatjēdzieni ##

2012. gada janvārī pēdējo reizi tika atjaunināts XSL-FO darba projekts, un 2013. gada novembrī tā darba grupa tika slēgta. XSL stila lapa nosaka XML dokumentu klases prezentāciju, aprakstot, kā klases gadījums tiek pārveidots par XML dokumentu, kurā tiek izmantota formatēšanas vārdnīca. XSL-FO ir integrēta prezentācijas valoda, un tai nav semantisko marķējumu, kas tiek izmantots HTML. Turklāt šī valoda visus dokumenta datus saglabā sevī, pretēji CSS, kas maina ārējā HTML vai XML dokumenta noklusējuma iestatījumus.

XSL-FO lietošanas vispārīgie kritēriji ir tādi, ka lietotājs raksta dokumentu XML valodā, nevis raksta FO. Pēc tam notiek XSLT transformācija. Šī XSLT transformācija ir atbildīga par XML konvertēšanu uz XSL-FO. Tiklīdz XSL-FO dokuments ir ģenerēts, tas tiek nodots lietojumprogrammai, ko sauc par FO procesoru. FO apstrādātāji ir atbildīgi par šī dokumenta pārveidošanu par lasāmu, kā arī izdrukājamu dokumentu. PDF faili vai PS ir visizplatītākās XSL-FO izvades piemēri. Bet tas nenozīmē, ka FO procesors var radīt tikai šos divu veidu formātus kā izvadi. Daži FO procesori var izvadīt RTF failus vai pat logs var parādīties lietotāja GUI, šajā logā tiek parādīta lapas secība un to saturs.

XSL-FO dokuments atšķiras no PDF vai PS tādā nozīmē, ka tas galu galā nenosaka teksta izkārtojumu dažādās lapās. Iespējams, tas veido lapu stilus un nosaka vietas, kur rādīt saturu. Turklāt FO procesors sakārto tekstu FO dokumentā norādītajās robežās. Šī specifikācija pat ļauj dažādiem FO procesoriem rīkoties atbilstoši izveidotajām lapām. Šādas darbības piemērs ir defise, daži FO procesori var defisēt vārdus, lai ietaupītu vietu, kad līnija tiek pārtraukta, savukārt daži procesori šo opciju neatlasa. Tas ir atkarīgs no procesora, lai izvēlētos dažādus defisēšanas algoritmus, kas atbilst viņu prasībām. Šie defisēšanas algoritmi var būt ļoti vienkārši vai sarežģītāki. Dažās situācijās XSL-FO specifikācija skaidri nosaka FO procesorus, zināmā mērā izvēloties izkārtojuma kontekstu.

Šīs atšķirības starp FO procesoriem rada atšķirīgus rezultātus, par kuriem procesori bieži vien neuztraucas. Tā kā XSL-FO galvenā uzmanība tiek pievērsta lappušu/drukātu dokumentu ražošanai. XSL-FO dokumenti paši parasti darbojas kā starpnieki, to galvenā funkcija ir ģenerēt vai nu PDF failus, vai dokumentu, ko var izdrukāt kā izplatāmo rezultātu. Izmantojot HTML/CSS vai XSL-FO, PDF kā gala rezultāta izplatīšana, nevis formatēšanas valodas ievadīšana, norāda, ka uztvērējus neietekmē radītā daudzpusība, kas rodas formatēšanas valodas tulku atšķirību dēļ. No otras puses, ir skaidrs, ka nav viegla ceļa, kā dokuments var apmierināt dažādas saņēmēju vajadzības, piemēram, mainīgs lapas izmērs vai vēlamais fonta lielums, vai pielāgošana lapai vai izdrukai.

## XSLFO faila formāts ##

SL-FO dokumenti būtībā ir XML dokumenti, taču tie neatbilst nevienai shēmai. Tā vietā SL-FO dokumenti ievēro sintakse, kas noteikta viņu valodas specifikācijā. Katrā XSL-FO dokumentā ir nepieciešamas divas sadaļas:

1. Sadaļa, kurā norādīts lapu izkārtojumu saraksts ar etiķetēm.
1. Sadaļa ar visu dokumenta datu detaļām, ar marķējumu, kas nosaka satura attēlošanu dažādās lapās, izmantojot dažādus lapu izkārtojumus.

Lapas rekvizīti ir minēti lappušu izkārtojumos, kas var definēt teksta organizāciju, lai tā atbilstu konkrētās valodas konvencijām. Turklāt lapas izmēru, to piemales un lappušu secības (kas nosaka dažādus nepāra un pāra lapu rekvizītus) nosaka arī lapu izkārtojumi.

Dokumenta datu daļa ir sadalīta plūsmu sērijās, kur katra plūsma ir saistīta ar lapas izkārtojumu. Plūsmas ietver tajās esošo bloku sarakstu. Šajā bloku sarakstā var būt iekļautas iezīmēšanas funkcijas vai teksta datu saraksts, vai arī abas vienlaikus. Uz dokumenta malām var būt arī lappušu numuri vai nodaļu virsraksti. Gan bloku, gan iekļauto elementu funkcionalitāte paliek tāda pati kā CSS, tomēr daži polsterējuma un piemales noteikumi atšķiras starp FO un CSS.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Vairākas kolonnas ##

Lapā var būt vairākas kolonnas un bloki, un pēc noklusējuma tā var paplašināties no vienas kolonnas uz otru. Vairākām lapām ir atļauts atšķirīgs platums un kolonnu skaits. Visi FO raksturlielumi atbilst vairāku kolonnu lapas ierobežojumiem.

### Saraksti ###

XSL-FO sarakstu veido divi bloku komplekti, kas sakārtoti pa žokļa kauliem. Konceptuāli sarakstā bloks kreisajā pusē norāda skaitli, aizzīmi vai teksta virkni, savukārt labās puses bloks var darboties, kā paredzēts. XSL-FO sarakstu numerāciju parasti veic XSLT.

### Tabulas ###

FO tabula ir līdzīga HTML/CSS tabulai. Lietotājs var izvēlēties datu rindas, stila informāciju, fona krāsu katrai atsevišķai šūnai. Izmantojot atšķirīgu stila informāciju, lietotājam ir tiesības izvēlēties pirmo rindu kā tabulas galvenes rindu. FO procesors var būt skaidri informēts par katras kolonnas vietas specifikāciju vai automātiski ietilpināt tekstu tabulā.

### Indeksēšana ###

XSL-FO 1.1 ir funkcijas, kas palīdz ģenerēt indeksu, atsaucoties uz pareizi iezīmētiem elementiem.

### Ieguvumi ###

* Piemērots satura publicēšanai

* Lietošanas ērtums

* Lēts


## Atsauces Nr.

* [Kas ir XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)

* [XSL formatēšanas objekti](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)


