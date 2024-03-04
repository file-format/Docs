{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MXF – medžiagų mainų formatas",
  "keywords": [
"MXF",
"matroskos vaizdo įrašas",
"mkv formatu",
"kaip leisti MXF failus",
"SMPTE",
"multimedija",
"vaizdo įrašą"
],
  "description": "Sužinokite apie MXF failo formatą ir API, kurios gali kurti ir atidaryti MXF failus.",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mx-ltf"
}
},
  "lastmod": "2021-03-01"
}

## Kas yra MXF failas?

Failas su plėtiniu .mxf yra daugialypės terpės konteinerio formatas, kuriame yra skaitmeninės vaizdo ir garso laikmenos kartu su failo metaduomenų informacija. Ji atitinka SMPTE (Kino ir televizijos inžinierių draugijos) standartą, kuris yra pasaulinė inžinerijos, technologijų ir žiniasklaidos bei pramogų pramonės vadovų asociacija. MXF failus galima konvertuoti į kitus failų formatus, pvz., [AVI](/video/avi/) arba [MOV](/video/mov/).

## MXF failo formatas

MXF failai iš tikrųjų yra dvejetainiai failai, kuriuos sudaro tam tikro formato baitų seka. Dekodavimo programos turi atitikti šį formatą, kad būtų galima jį suprasti ir iš jo išgauti informaciją. Formatas leidžia pridėti naujų elementų nepažeidžiant atgalinio suderinamumo naudojant KLV kodavimą, kuris aprašytas toliau.

 * Raktas – elemento identifikatorius, SMPTE universali etiketė (UL)
 * Ilgis – duomenų ilgis, kuris yra kintamo ilgio kodavimas, naudojamas siekiant sumažinti vietos, reikalingos šiam elementui, kiekį
 * Vertė – tikroji elemento vertė.

### SMPTE formato specifikacijos

MXF failo formatas apibrėžtas pagal šias SMPTE specifikacijas.

* SMPTE ST 377-1:2011. Televizija – medžiagų mainų formatas (MXF) – failo formato specifikacija

* SMPTE ST 377-2 (2012 m. sausio mėn. atliekami darbai). KLV užkoduota plėtinio sintaksė, skirta MXF.

* SMPTE ST 378:2004 (archyvuota 2010 m.). Televizija – medžiagų mainų formatas (MXF) – 1a veikimo modelis (vienas elementas, vienas paketas)

* SMPTE ST 379-1:2009. Medžiagų mainų formatas (MXF) – MXF bendras konteineris

* SMPTE ST 379-2:2010. Medžiagų mainų formatas (MXF) – MXF suvaržytas bendrasis konteineris

* SMPTE ST 380:2004. Televizija – medžiagų mainų formatas (MXF) – aprašomųjų metaduomenų schema-1 (standartinė, dinaminė)

* SMPTE ST 381-1:2005. Televizija – medžiagų mainų formatas (MXF) – MPEG srautų susiejimas su MXF bendruoju konteineriu (dinaminis)

* SMPTE ST 381-2:2011. Medžiagų mainų formatas (MXF) – MPEG srautų susiejimas su MXF ribotu bendruoju konteineriu

* SMPTE ST 382:2007. Medžiagų mainų formatas (MXF) – AES3 srautų ir transliacijos bangos garso susiejimas su MXF bendruoju konteineriu

* SMPTE ST 383:2008. Televizija – medžiagų mainų formatas (MXF) – DV-DIF duomenų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 384:2005. Televizija – medžiagų mainų formatas (MXF) – nesuspaustų nuotraukų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 385:2004. Televizija – medžiagų mainų formatas (MXF) – SDTI-CP esmės ir metaduomenų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 386:2004 (archyvuota 2010 m.). Televizija – medžiagų mainų formatas (MXF) – D-10 tipo esmės duomenų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 387:2004 (archyvuota 2010 m.). Televizija – medžiagų mainų formatas (MXF) – D-11 tipo esmės duomenų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 388:2004 (archyvuota 2010 m.). Televizija – medžiagų mainų formatas (MXF) – A-teisė kodo garso susiejimas su MXF bendruoju konteineriu

* SMPTE ST 389:2005. Televizija – medžiagų mainų formatas (MXF) – MXF bendrasis konteinerio atvirkštinio paleidimo sistemos elementas

* SMPTE ST 390:2011. Televizija – medžiagų mainų formatas (MXF) – specializuotas veikimo modelis „atomas“ (supaprastintas vieno elemento vaizdavimas)

* SMPTE ST 391:2004 (archyvuota 2010 m.). Televizija – medžiagų mainų formatas (MXF) – 1b veikimo modelis (vienas elementas, sugrupuoti paketai)

* SMPTE ST 392:2004. Televizija – medžiagų mainų formatas (MXF) – 2a veikimo modelis (grojaraščio elementai, vienas paketas)

* SMPTE ST 393:2004. Televizija – medžiagų mainų formatas (MXF) – 2b veikimo modelis (grojaraščio elementai, grupiniai paketai)

* SMPTE ST 394:2006. Televizija – medžiagų mainų formatas (MXF) – MXF bendrojo konteinerio 1 sistemos schema

* SMPTE ST 405:2006. Televizija – medžiagų mainų formatas (MXF) – MXF bendrosios konteinerių sistemos 1 schemos elementai ir atskiri duomenų elementai

* SMPTE ST 407:2006. Televizija – MXF – 3a ir 3b veikimo modeliai

* SMPTE ST 408:2006. Televizija – MXF – 1c, 2c ir 3c veikimo modeliai

* SMPTE ST 410: 2008. Medžiagų mainų formatas – bendras srauto skaidinys.

* SMPTE ST 422:2006. Medžiagų mainų formatas – JPEG2000 kodų srautų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 429.4:2006. D-Cinema pakuotė – MXF JPEG 2000 programa

* SMPTE ST 429.5:2006. D-Cinema Packaging – laiko teksto takelio failas

* SMPTE ST 429.6:2006. D-Cinema Packaging – MXF Track File Essence Encryption

* SMPTE ST 434:2006. Medžiagų mainų formatas – metaduomenų ir failų struktūros informacijos XML kodavimas

* SMPTE ST 436:2006. Televizija – VBI linijų ir papildomų duomenų paketų MXF atvaizdai

* SMPTE ST 2019-4:2009. VC-3 kodavimo vienetų susiejimas su MXF bendruoju konteineriu

* SMPTE ST 2037:2009. VC-1 susiejimas su MXF bendruoju konteineriu

* SMPTE RP 2008:2008. Medžiagų mainų formatas – AVC srautų susiejimas su MXF bendruoju konteineriu

* SMPTE RP 2057:2011. Tekstu pagrįstas metaduomenų pernešimas MXF formatu

* SMPTE EG 41:2004. Medžiagų mainų formatas (MXF) – inžinerinės gairės. Pastaba: šis dokumentas nebebuvo įtrauktas į SMPTE svetainę, kai buvo peržiūrėtas 2012 m. sausio mėn.

* SMPTE EG 42:2004. Medžiagų mainų formatas (MXF) – MXF aprašomieji metaduomenys

* SMPTE RDD 3:2008. e-VTR MXF sąveikos specifikacija

* SMPTE RDD 9-2009. „Sony MPEG Long GOP“ produktų MXF sąveikumo specifikacija

* SMPTE metaduomenų registro skaičiuoklės meniu.


### MXF struktūriniai metaduomenys

Struktūriniai metaduomenys yra pagrindiniai MXF failo elementai, nes juose yra naudingos informacijos apie failo turinį. MXF metaduomenyse yra tokia informacija kaip kadrų dažnis, kadro dydis, failo sukūrimo data ir pasirinktinio pakeitimo data. Struktūriniai metaduomenys apibūdina MXF failo struktūrą ir galimybes, įskaitant technišką įvairių esminių komponentų apibūdinimą ir išvesties laiko juostos sudarymo perteikimą.

## Nuorodos

 * [MXF – Vikipedija](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [Atvirojo kodo C++ biblioteka, skirta MXF](http://www.freemxf.org/)

