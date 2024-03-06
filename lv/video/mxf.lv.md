{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MXF - Materiālu apmaiņas formāts",
  "keywords": [
"MXF",
"matroska video",
"mkv formātā",
"kā atskaņot MXF failus",
"SMPTE",
"multivide",
"video"
],
  "description": "Uzziniet par MXF failu formātu un API, kas var izveidot un atvērt MXF failus.",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mx-lvf"
}
},
  "lastmod": "2021-03-01"
}

## Kas ir MXF fails?

Fails ar paplašinājumu .mxf ir multivides konteinera formāts, kas satur digitālo video un audio datu nesēju, kā arī metadatu informāciju par failu. Tas atbilst SMPTE (Motion Picture and Television Engineers) standartam, kas ir globāla inženierzinātņu, tehnoloģiju un mediju un izklaides industrijā strādājošu vadītāju asociācija. MXF failus var konvertēt citos failu formātos, piemēram, [AVI](/video/avi/) vai [MOV](/video/mov/).

## MXF faila formāts

MXF faili patiesībā ir bināri faili, kas sastāv no baitu secības noteiktā formātā. Dekodēšanas lietojumprogrammām ir jāatbilst šim formātam, lai to saprastu un iegūtu informāciju no tā. Formāts ļauj pievienot jaunus vienumus, nepārkāpjot atpakaļejošo saderību, izmantojot tālāk aprakstīto KLV kodējumu.

 * Atslēga – elementa identifikators, SMPTE universālā etiķete (UL)
 * Length – datu garums, kas ir mainīga garuma kodējums, ko izmanto, lai samazinātu šim vienumam nepieciešamās vietas daudzumu
 * Vērtība – elementa faktiskā vērtība.

### SMPTE formāta specifikācijas

MXF faila formāts ir definēts saskaņā ar šādām SMPTE specifikācijām.

* SMPTE ST 377-1:2011. Televīzija — materiālu apmaiņas formāts (MXF) — faila formāta specifikācija

* SMPTE ST 377-2 (notiek darbs uz 2012. gada janvāri). KLV kodētā paplašinājuma sintakse MXF.

* SMPTE ST 378:2004 (arhivēts 2010. gads). Televīzija — materiālu apmaiņas formāts (MXF) — darbības modelis 1a (viena prece, viena pakete)

* SMPTE ST 379-1:2009. Materiālu apmaiņas formāts (MXF) — MXF vispārīgais konteiners

* SMPTE ST 379-2:2010. Materiālu apmaiņas formāts (MXF) — MXF ierobežots vispārīgais konteiners

* SMPTE ST 380:2004. Televīzija — materiālu apmaiņas formāts (MXF) — aprakstošā metadatu shēma 1 (standarta, dinamiska)

* SMPTE ST 381-1:2005. Televīzija — materiālu apmaiņas formāts (MXF) — MPEG straumju kartēšana MXF vispārīgajā konteinerā (dinamiskā)

* SMPTE ST 381-2:2011. Materiālu apmaiņas formāts (MXF) — MPEG straumju kartēšana MXF ierobežotajā vispārīgajā konteinerā

* SMPTE ST 382:2007. Materiālu apmaiņas formāts (MXF) — AES3 straumju un apraides viļņu audio kartēšana MXF vispārīgajam konteineram

* SMPTE ST 383:2008. Televīzija — materiālu apmaiņas formāts (MXF) — DV-DIF datu kartēšana MXF vispārīgajam konteineram

* SMPTE ST 384:2005. Televīzija — materiālu apmaiņas formāts (MXF) — nesaspiestu attēlu kartēšana MXF vispārīgajā konteinerā

* SMPTE ST 385:2004. Televīzija — materiālu apmaiņas formāts (MXF) — SDTI-CP būtības un metadatu kartēšana MXF vispārīgajā konteinerā

* SMPTE ST 386:2004 (arhivēts 2010. gads). Televīzija — materiālu apmaiņas formāts (MXF) — D-10 tipa būtības datu kartēšana MXF vispārīgajam konteineram

* SMPTE ST 387:2004 (arhivēts 2010. gads). Televīzija — materiālu apmaiņas formāts (MXF) — D-11 tipa būtības datu kartēšana MXF vispārīgajam konteineram

* SMPTE ST 388:2004 (arhivēts 2010. gads). Televīzija — materiālu apmaiņas formāts (MXF) — A-likuma kodēta audio kartēšana MXF vispārīgajā konteinerā

* SMPTE ST 389:2005. Televīzija — materiālu apmaiņas formāts (MXF) — MXF vispārējā konteinera apgrieztās atskaņošanas sistēmas elements

* SMPTE ST 390:2011. Televīzija — materiālu apmaiņas formāts (MXF) — specializēts darbības modelis "Atom" (vienkāršā veidā attēlots viens vienums)

* SMPTE ST 391:2004 (arhivēts 2010. gads). Televīzija — materiālu apmaiņas formāts (MXF) — darbības modelis 1b (viena vienība, grupētas paketes)

* SMPTE ST 392:2004. Televīzija — materiālu apmaiņas formāts (MXF) — darbības modelis 2a (atskaņošanas saraksta vienumi, viena pakete)

* SMPTE ST 393:2004. Televīzija — materiālu apmaiņas formāts (MXF) — darbības modelis 2b (atskaņošanas saraksta vienumi, grupētas paketes)

* SMPTE ST 394:2006. Televīzija — materiālu apmaiņas formāts (MXF) — 1. sistēmas shēma MXF vispārīgajam konteineram

* SMPTE ST 405:2006. Televīzija — materiālu apmaiņas formāts (MXF) — elementi un atsevišķi datu vienumi MXF vispārējās konteineru sistēmas 1. shēmai

* SMPTE ST 407:2006. Televīzija — MXF — 3.a un 3.b darbības shēma

* SMPTE ST 408:2006. Televīzija — MXF — darbības modeļi 1c, 2c un 3c

* SMPTE ST 410: 2008. Materiālu apmaiņas formāts — vispārīgs straumes nodalījums.

* SMPTE ST 422:2006. Materiālu apmaiņas formāts — JPEG2000 kodu straumju kartēšana MXF vispārīgajā konteinerā

* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000 lietojumprogramma

* SMPTE ST 429.5:2006. D-Cinema Packaging — teksta ieraksta fails ar laiku

* SMPTE ST 429.6:2006. D-Cinema iepakojums — MXF Track File Essence šifrēšana

* SMPTE ST 434:2006. Materiālu apmaiņas formāts — XML kodējums metadatu un failu struktūras informācijai

* SMPTE ST 436:2006. Televīzija — MXF kartējumi VBI līnijām un papildu datu paketēm

* SMPTE ST 2019-4:2009. VC-3 kodēšanas vienību kartēšana MXF vispārīgajā konteinerā

* SMPTE ST 2037:2009. VC-1 kartēšana MXF vispārīgajā konteinerā

* SMPTE RP 2008:2008. Materiālu apmaiņas formāts — AVC straumju kartēšana MXF vispārīgajā konteinerā

* SMPTE RP 2057:2011. Teksta metadatu pārnešana MXF formātā

* SMPTE EG 41:2004. Materiālu apmaiņas formāts (MXF) — Inženierzinātņu vadlīnijas. Piezīme. Šis dokuments vairs nebija iekļauts SMPTE tīmekļa vietnē, kad to aplūkoja 2012. gada janvārī.

* SMPTE EG 42:2004. Materiālu apmaiņas formāts (MXF) — MXF aprakstošie metadati

* SMPTE RDD 3:2008. e-VTR MXF savietojamības specifikācija

* SMPTE RDD 9-2009. Sony MPEG Long GOP produktu MXF sadarbspējas specifikācija

* SMPTE metadatu reģistra izklājlapas izvēlne.


### MXF strukturālie metadati

Strukturālie metadati ir ļoti svarīgi MXF failā, jo tie satur noderīgu informāciju par faila saturu. MXF metadatos ir ietverta tāda informācija kā kadru nomaiņas ātrums, kadra izmērs, faila izveides datums un pielāgotās modifikācijas datums. Strukturālie metadati apraksta MXF faila struktūru un iespējas, kas ietver dažādu būtisku komponentu tehnisku aprakstu un izvades laika skalas sastāva nodošanu.

## Atsauces

 * [MXF — Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [OpenSource C++ bibliotēka for MXF](http://www.freemxf.org/)

