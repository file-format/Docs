{
  "date": "2019-10-11",
  "keywords": [
"wmf failu",
"wmf faila formātā",
"kas ir wmf fails",
"failu",
"wmf piemērs",
"wmf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMF — Microsoft Windows metafaila formāts",
  "description": "Uzziniet par WMF failu formātu un API, kas var izveidot un atvērt WMF failus.",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir WMF fails?

Faili ar WMF paplašinājumu ir Microsoft Windows Metafile (WMF) vektoru, kā arī bitkartes formāta attēlu datu glabāšanai. Lai būtu precīzāk, WMF pieder grafikas failu formātu vektora failu formātu kategorijai, kas ir neatkarīga no ierīces. Windows grafiskās ierīces interfeiss (GDI) izmanto WMF failā saglabātās funkcijas, lai ekrānā parādītu attēlu. Vēlāk tika publicēta uzlabota WMF versija, kas pazīstama kā Enhanced Meta Files (EMF), kas padara formātu daudz funkcijām bagātāku. Praktiski WMF ir līdzīgi SVG.

## WMF faila formāta specifikācijas ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. Faila formāts sastāv no mainīga garuma ierakstu sērijas, kas satur grafikas zīmēšanas komandas, objektu definīcijas un rekvizītus. Tā kā WMF faili ir balstīti uz komandām, kas tiek atveidotas GDI attēla zīmēšanai, to sauc arī par attēla digitālo ierakstu, ko var atskaņot, lai reproducētu šo attēlu. Pilnas WMF faila formāta specifikācijas ir pieejamas tiešsaistē, un tās ir jāizmanto lietojumprogrammu izstrādei darbam ar WMF failiem. WMF fails ir sakārtots:

* WMF galvenes ieraksts

* WMF ieraksts(-i)

* WMF faila beigu ieraksts


### WMF galvenes ieraksts ###

**META_HEADER ieraksts** satur informāciju, kas nosaka metafaila īpašības, tostarp:

* Metafaila veids

* Metafaila versija

* Metafaila lielums

* Metafailā definēto objektu skaits

* Lielākā viena ieraksta lielums metafailā


### WMF ievietojamās galvenes ieraksts ###

**META_PLACEABLE ieraksts** satur paplašinātu informāciju par attēlu, tostarp:

* Ierobežojošs taisnstūris

* Loģiskās vienības izmērs, mērogošana

* Kontrolsumma apstiprināšanai


### WMF rekords ###

WMF ierakstiem ir vispārīgs formāts, kas norādīts specifikāciju dokumentā. Katrs WMF ieraksts satur šādu informāciju:

* Ieraksta lielums

* Ierakstīšanas funkcija

* Parametri, ja tādi ir, ierakstīšanas funkcijai


## Atsauces Nr.

* [[MS-WMF]: Windows metafaila formāts](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [Windows MetaFile — Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)


