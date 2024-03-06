{
  "date": "2019-10-11",
  "keywords": [
"osm fails",
"kas ir osm fails",
"failu",
"osm piemērs",
"osm faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM — OpenStreetMap faila formāts",
  "description": "Uzziniet par OSM failu formātu un API, kas var izveidot un atvērt OSM failus.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-lvm"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir OSM fails?

OpenStreetMap (OSM) ir milzīga brīvprātīga ģeogrāfiskās informācijas kolekcija, kas glabājas dažāda veida failos, izmantojot dažādas kodēšanas shēmas, lai šos datus pārvērstu bitos un baitos. OSM ir kopīgs darbs, lai izveidotu bezmaksas rediģējamu pasaules karti. Šīs sadarbības galvenais rezultāts ir ģeogrāfiskie dati, nevis pati karte. Ģeogrāfiskās informācijas izmantošanas vai pieejamības ierobežojumi lielākajā daļā pasaules izraisa nepieciešamību izveidot OSM.

No OSM pieejamie dati ir gatavi aizstāt Google Maps klasiskajām lietojumprogrammām (Facebook, Craigslist uc) un noklusējuma datus GPS uztvērēju lietojumprogrammām. Lai gan datu kvalitāte visā pasaulē ir dažāda, OpenStreetMap datus var ērti salīdzināt ar patentu datu avotiem.

## Īsa OSM faila formāta vēsture

Iedvesmojoties no Wikipedia panākumiem, 2004. gadā britu uzņēmējs Stīvs Kosts izveidoja šo kopienas pasaules kartēšanas projektu Apvienotajā Karalistē. Sākotnēji viņš koncentrējās uz Apvienotās Karalistes kartēšanu. OpenStreetMap fonds pirmo reizi tika izveidots 2006. gada aprīlī, lai atbalstītu bezmaksas ģeotelpiskās informācijas attīstību, paplašināšanos un apriti ikvienam. 2006. gada decembrī Yahoo palīdzēja OpenStreetMap ar aerofotografēšanu karšu izgatavošanai.

Pilnīgus ceļu datus par Nīderlandi un maģistrālo ceļu datus par Indiju un Ķīnu 2007. gada aprīlī OSM sniedza Automotive Navigation Data (AND). 2007. gada decembrī Oksfordas Universitāte bija visievērojamākā organizācija, kas savā galvenajā vietnē integrēja OpenStreetMap datus. Kopš tā laika vairāk nekā 2 miljoni reģistrētu lietotāju šajā projektā ir iesnieguši datus, izmantojot GPS ierīces, aerofotografēšanu un manuālas aptaujas. Šie kopienas sniegtie dati ir pieejami saskaņā ar Open Database licenci. Anglijā reģistrēta bezpeļņas organizācija OpenStreetMap Foundation uzturēja OSM vietni.

## OSM faila formāts

Ģeogrāfisko datu glabāšanai ir daudz veidu un failu formātu, taču **OSM** faila formāts ir ierobežots ar OpenStreetMap. OSM ir īpaši izstrādāts standarta formāts, kas paredzēts vienkāršai pārvietošanai pa internetu. Strukturēts sakārtots formāts, kas kodēts XML formātā, veido .osm failu. Programmā OpenStreetMap ir četri pagrieziena elementi, lai saglabātu topoloģisko datu struktūru:

{{< figure src="../OSM.png" alt="OSM faila formāts" >}}


|Mezgli|Veidi|Attiecības|Tagi
---|---|---|---|
|<ul><li> Apzīmē ģeogrāfisko stāvokli, kas saglabāts kā platuma un garuma pāri.</li><li> Izmanto, lai attēlotu kartes objektus bez izmēra, piemēram, kalnu virsotnes.</li></ul> |<ul><li> Sakārtoti mezglu saraksti, kas apzīmē polilīniju vai daudzstūri</li><li> Attēlojiet lineārus objektus, piemēram, ceļus un upes, un zonas, piemēram, stāvvietas, džungļus un parkus.</li></ul> |<ul><li> Sakārtoti mezglu un ceļu saraksti attēlo to attiecības, piemēram, barjeras un pagriezienus uz ceļiem, automaģistrāles aptver dažādus esošos ceļus un zonas ar caurumiem.</li></ul> |<ul><li> Saglabājiet metadatus par kartes objektiem.* Vienmēr pievienoti jebkuram mezglam, ceļam vai relācijai</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

OSM galveno datu glabāšanai izmanto trīs veidu failus.

OSM apstrādā visus šos failus ar informāciju par to formatējuma detaļām. Taču šie faili rada tos pašus iekšējos objektus. Datu failiem redzamais karodziņš uz OSM objektiem vienmēr ir patiess, kas neattiecas uz vēstures un izmaiņu failiem.

Parasti tiek izmantoti dažādi OSM failu formāti. Failu formāti nosaka satura kodējumu diskā vai vadā bitos un baitos. OSM spēj lasīt un rakstīt maksimāli no šiem formātiem.

**XML**

Sākotnējais OSM formāts ir balstīts uz XML. Galvenās OSM datu bāzes API atgriešanas dati ir XML formātā.

**PBF**

Protokolu buferu kodējums ir binārā formātā un viens no kompaktākajiem formātiem.

**O5M/O5C**

Binārā formāta pamatā ir vienkāršāks formāts, bet salīdzinoši mazāk izmantots. OSM var lasīt, bet nevar rakstīt šo formātu.

**OPL**

Vienkāršs formāts, ko ieteicams izmantot ar standarta UNIX komandrindas rīkiem. Tuvu CSV failiem, ļauj vienu OSM entītiju vienā rindā.

**ATKLĀJUMS**

Teksta formāts, kas paredzēts atkļūdošanai. OSM var rakstīt šo formātu, bet nevar lasīt.

**MELNAIS CAURUMS**

Manekens formāts, kas apglabā visus datus. OSM var rakstīt šo formātu, bet nevar lasīt.

## OSM datu krātuve ##

OSM galvenā **PostgreSQL** datubāze saglabā OSM datu galveno kopiju ar PostGIS paplašinājumu. Katram datu primitīvam galvenā datu bāze uztur tabulu, kuras rindās tiek glabāti atsevišķi objekti. Visi labojumi atjaunina šo datu bāzi, un visi citi formāti tiek veidoti, izmantojot šo datu bāzi. Lai pārsūtītu datus no vienas vietas uz citu, tiek izveidoti daudzi lejupielādējami datu bāzu pūli. Divi formāti, no kuriem viens izmanto XML un otrs, izmantojot protokola bufera bināro formātu (PBF), nosaka šos kopumus. Visi dati tiek glabāti failā planet.osm

## Saspiešana OSM failos ##

Teksta formāti (XML, OPL un atkļūdošana) pēc izvēles izmanto gzip vai bzip2 saspiešanu.

## Atsauces Nr.

* [OSM failu formātu rokasgrāmata](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)

* [Uzziniet OSM](https://learnosm.org/en/osm-data/getting-data/)


