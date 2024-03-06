{
  "date": "2019-10-11",
  "keywords": [
"mf failu",
"mf",
"pagarinājumu",
"formātā",
"mf faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF — Java manifesta faila formāts",
  "description": "Uzziniet par MF failu formātu un API, kas var izveidot un atvērt MF failus.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-lvf"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir MF fails?

Fails ar paplašinājumu .mf ir Java manifesta fails, kurā ir informācija par atsevišķiem faila [JAR](/programming/jar/) ierakstiem. Pats MF fails atrodas JAR failā un nodrošina visu ar paplašinājumu un pakotni saistīto definīciju. JAR failus var izveidot, lai tos izmantotu kā izpildāmo failu. Šādā gadījumā mainfest fails norāda lietojumprogrammas galveno klasi, kas satur **`public static void main`** paziņojumu. Manifesta faili tiek nosaukti kā MANIFEST.MF, un tos var atvērt ar jebkuru teksta redaktoru operētājsistēmās Windows, MacOS un Linux.

## Manifesta faila formāta specifikācijas

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Galvenās sadaļas

Galvenā sadaļa:

* satur informāciju par JAR faila drošību un konfigurāciju

* satur informāciju par lietojumprogrammu vai paplašinājumu, kurā ir JAR fails

* definē galvenos atribūtus katram atsevišķam manifesta vienumam


**Piezīme**. Nevienu atribūtu šajā sadaļā nevar nosaukt par nosaukumu Vārds.

### Atsevišķas sadaļas

Atsevišķa sadaļa definē dažādus JAR faila pakotņu vai failu atribūtus. Katrai sadaļai jāsākas ar atribūtu Nosaukums”, kura vērtībai ir jābūt relatīvam ceļam uz failu vai absolūtam URL, kas atsaucas uz datiem ārpus arhīva.

### Manifesta specifikācijas

|Attieksmes|Apraksts|
---|---|
|manifesta fails|galvenās sadaļas jaunā rindiņa *individual-section|
|galvenā sadaļa|informācija par versiju jaunrindiņa *galvenais atribūts|
|version-info|Manifesta versija : versijas numurs|
|versijas-numurs|cipars+{.cipars+}*|
|main-attribute|(jebkurš likumīgs galvenais atribūts) newline|
|individual-section|Nosaukums : vērtība jaunā rindiņa *perentry-attribute|
|perentry-attribute|(jebkurš likumīgs perentry atribūts) newline|
|jauna rinda|CR LF | LF | CR (bez LF)|
|cipars|{0-9}|

## Atsauces

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR faila formāts](https://en.wikipedia.org/wiki/JAR_(file_format))

