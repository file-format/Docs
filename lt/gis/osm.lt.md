{
  "date": "2019-10-11",
  "keywords": [
"osm failą",
"kas yra osm failas",
"failą",
"osm pavyzdys",
"osm failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM – OpenStreetMap failo formatas",
  "description": "Sužinokite apie OSM failo formatą ir API, kurios gali kurti ir atidaryti OSM failus.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-ltm"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra OSM failas?

OpenStreetMap (OSM) yra didžiulis savanoriškos geografinės informacijos saugyklų rinkinys įvairių tipų failuose, naudojant skirtingas kodavimo schemas, kad šie duomenys būtų konvertuojami į bitus ir baitus. OSM yra bendradarbiavimo pastangos kuriant nemokamą redaguojamą pasaulio žemėlapį. Pagrindinis šio bendradarbiavimo rezultatas yra geografiniai duomenys, o ne pats žemėlapis. Geografinės informacijos naudojimo arba prieinamumo apribojimai daugelyje pasaulio šalių sukelia poreikį sukurti OSM.

Iš OSM gaunami duomenys yra paruošti pakeisti Google Maps klasikinėms programoms (Facebook, Craigslist ir kt.) ir numatytuosius GPS imtuvų taikomųjų programų duomenis. Nors duomenų kokybė visame pasaulyje skiriasi, OpenStreetMap duomenis galima patogiai palyginti su patentiniais duomenų šaltiniais.

## Trumpa OSM failo formato istorija

Įkvėptas Vikipedijos sėkmės, 2004 m. britų verslininkas Steve'as Coastas sukūrė šį bendruomenės pasaulio žemėlapių sudarymo projektą JK. Iš pradžių jis daugiausia dėmesio skyrė Jungtinės Karalystės žemėlapiams. OpenStreetMap Foundation pirmą kartą buvo įkurtas 2006 m. balandžio mėn., siekiant remti nemokamos geografinės erdvės raidą, plėtrą ir platinimą bet kam. 2006 m. gruodžio mėn. Yahoo padėjo OpenStreetMap fotografuoti iš oro, kad būtų galima sukurti žemėlapius.

Išsamius Nyderlandų kelių duomenis ir Indijos bei Kinijos magistralinių kelių duomenis 2007 m. balandžio mėn. OSM pateikė Automotive Navigation Data (AND). 2007 m. gruodžio mėn. Oksfordo universitetas buvo ryškiausia organizacija, integravusi OpenStreetMap duomenis į savo pagrindinę svetainę. Nuo to laiko daugiau nei 2 milijonai registruotų vartotojų įneša duomenis į šį projektą naudodami GPS įrenginius, aerofotografavimą ir rankines apklausas. Šie bendruomenės pateikti duomenys yra prieinami pagal atvirosios duomenų bazės licenciją. Anglijoje registruota ne pelno organizacija OpenStreetMap Foundation prižiūrėjo OSM svetainę.

## OSM failo formatas

Geografiniams duomenims saugoti yra daug būdų ir failų formatų, tačiau **OSM** failo formatas yra apribotas OpenStreetMap. OSM yra specialiai sukurtas standartinis formatas, skirtas lengvai transportuoti internetu. Struktūrinis sutvarkytas formatas, užkoduotas XML, sudaro .osm failą. OpenStreetMap yra keturi pagrindiniai elementai, skirti saugoti topologinių duomenų struktūrą:

{{< figure src="../OSM.png" alt="OSM failo formatas" >}}


|Mazgai|Būdai|Santykiai|Žymos
---|---|---|---|
|<ul><li> Nurodo geografinę padėtį, saugomą kaip platumos ir ilgumos poras.</li><li> Naudojamas žemėlapio ypatybėms be dydžio, pvz., kalnų viršūnėms, pavaizduoti.</li></ul> |<ul><li> Surūšiuoti mazgų sąrašai, reiškiantys poliliniją arba daugiakampį</li><li> Pavaizduokite linijinius objektus, pvz., kelius ir upes, ir zonas, pvz., automobilių stovėjimo aikšteles, džiungles ir parkus.</li></ul> |<ul><li> Surūšiuoti mazgų ir kelių sąrašai atspindi jų ryšį, pavyzdžiui, kliūtis ir posūkius keliuose, greitkeliai apima skirtingus esamus kelius ir sritis su skylėmis.</li></ul> |<ul><li> Saugokite metaduomenis apie žemėlapio objektus.* Visada pridedamas prie bet kokio mazgo, būdo ar santykio</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

Pagrindiniams duomenims saugoti OSM naudoja trijų tipų failus.

OSM tvarko visus šiuos failus su informacija apie jų formatavimo informaciją. Tačiau šie failai sukuria tuos pačius vidinius objektus. Duomenų failams matoma vėliavėlė OSM objektuose visada yra teisinga, o tai netaikoma istorijos ir pakeitimų failams.

Įprastai naudojami OSM failų formatai yra įvairūs. Failų formatai apibrėžia turinio kodavimą diske arba laidu bitais ir baitais. OSM gali skaityti ir rašyti daugiausiai šių formatų.

**XML**

Originalus OSM formatas yra pagrįstas XML. Pagrindinės OSM duomenų bazės API grąžinami duomenys yra XML formatu.

**PBF**

Protokolo buferių kodavimas yra dvejetainio formato ir vienas kompaktiškiausių formatų.

**O5M/O5C**

Dvejetainiu formatu pagrįstas paprastesnis formatas, bet palyginti mažiau naudojamas. OSM gali skaityti, bet negali rašyti šio formato.

**OPL**

Paprastas formatas, siūlomas naudoti su standartiniais UNIX komandų eilutės įrankiais. Arti CSV failų, leidžia vieną OSM objektą vienoje eilutėje.

**DEBUG**

Teksto formatas, skirtas derinimui. OSM gali rašyti šį formatą, bet negali skaityti.

**JUODOJI SKYLĖ**

Manekeno formatas, kuriame yra visi duomenys. OSM gali rašyti šį formatą, bet negali skaityti.

## OSM duomenų saugykla Nr.

Pagrindinėje OSM **PostgreSQL** duomenų bazėje saugoma pagrindinė OSM duomenų kopija su PostGIS plėtiniu. Kiekvienam duomenų primityvui pagrindinė duomenų bazė palaiko lentelę, kurios eilutėse saugomi atskiri objektai. Visi pakeitimai atnaujina šią duomenų bazę, o visi kiti formatai formuojami naudojant šią duomenų bazę. Sukurta daugybė atsisiunčiamų duomenų bazių telkinių, skirtų duomenims perkelti iš vienos vietos į kitą. Šiuos telkinius apibrėžia du formatai, vienas naudojant XML, o kitas naudojant Protocol Buffer Binary Format (PBF). Visi duomenys saugomi faile planet.osm

## Suspaudimas OSM failuose ##

Teksto formatai (XML, OPL ir Debug) pasirinktinai naudoja gzip arba bzip2 glaudinimą.

## Nuorodos Nr.

* [OSM failų formatų vadovas](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)

* [Sužinokite OSM](https://learnosm.org/en/osm-data/getting-data/)


