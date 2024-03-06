{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"XML papīra specifikācijas",
"Fails",
"Pagarinājums",
"Faila formāts",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS — lapas izkārtojuma faila formāts",
  "description": "Uzziniet par XPS failu formātu un API, kas var izveidot un atvērt XPS failus.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-lvs"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir XPS fails?

XPS fails ir lapas izkārtojuma faili, kuru pamatā ir Microsoft izveidotās XML papīra specifikācijas. Tas tika izstrādāts kā EMF faila formāta aizstājējs un ir līdzīgs [PDF](/pdf/) faila formātam, taču izmanto XML dokumenta izkārtojumā, izskatā un drukāšanas informācijā. Faktiski ir pamatotāk teikt, ka XPS ir PDF mēģinājums, taču daudzu iemeslu dēļ nevarēja iegūt pietiekami daudz popularitātes, jo tas pieder PDF. Microsoft nodrošina XPS Document Writer pēc noklusējuma, sākot no operētājsistēmas Windows 7, lai izveidotu XPS failus. XPS failus var ģenerēt, dokumenta drukāšanas laikā kā printeri atlasot Microsoft XPS Document Writer.

XPS skatītāji ir integrēti kā daļa no Windows Vista, Windows 7, Windows 8 un Internet Explorer 6 vai jaunākas versijas. XPS faili kļūst tikai lasāmi, kad tie ir ģenerēti. Tas palielina lietotāja pārliecību par saņemtajiem dokumentiem, kas nosūtīti kā XPS, lai nodrošinātu dokumenta autentiskumu. XPS dokumentā var būt viena vai vairākas lapas, kas ir pārveidotas no sākotnējā dokumenta.

## Īsa vēsture ##

Microsoft iesniedza XPS specifikāciju uzņēmumam Ecma International. 2007. gada jūnijā tika izveidota Ecma Tehniskā komiteja 46 (TC46), lai izstrādātu standartu, kura pamatā ir OpenXPS papīra specifikācijas. Ecma International apstiprināja Ecma standartu (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) 2009. gada jūnijā 97. Ģenerālajā asamblejā.

## XPS faila formāts ##

XPS formāts sastāv no XML marķējuma, kas nosaka dokumenta sastāvu un katras lapas vizuālo izskatu, kā arī renderēšanas noteikumus dokumenta parādīšanai vai drukāšanai. Tā saglabā visu informāciju, lai atkārtoti izveidotu dokumentu jebkurā sistēmā, kas padara to neatkarīgu no šajā sistēmā pieejamajiem resursiem. Formāts būtībā ir ZIP arhīvs, un, pārdēvējot faila paplašinājumu uz ZIP, jūs redzēsit veidojošos failus, kas satur dokumenta datus. Šajos dokumentos ietilpst:

* dokumenta lappušu faili (.fpage) — satur dokumenta satura un dokumenta formāta iestatījumus. Katrai XPS dokumenta lapai ir viens FPAGE fails.

* Dokumenta iestatījumu fails (.fdoc) — saglabā XPS arhīvā iekļautos iestatījumus.

* dokumenta fragmentu faili (.frag) — definē iestatījumus faktiskajam XPS failam, un katrai dokumenta lapai ir savs .frag fails.


{{< figure src="../XPS-1.png" alt="XPS faila formāts" >}}

Šie faili saglabā dokumenta saturu tādā veidā, ka, piemēram, ja kādam savā datorā nav instalēti tie paši fonti, XPS skatītājs joprojām atveidos šos oriģinālos fontus. Tas nozīmē, ka ir jāiekļauj XML iezīmēšanas fails katram:

* Lappuse

* Teksts

* Iegultie fonti

* Rastra attēli

* 2D vektorgrafika

* Digitālo tiesību pārvaldība


XPS dokumenta formāts ietver labi definētu daļu un attiecību kopu, no kurām katra atbilst konkrētam dokumenta mērķim. Formāts arī paplašina pakotnes funkcijas, tostarp ciparparakstus, sīktēlus un izvietošanu.

Tipisks XPS dokuments izskatās šādi, un to var analizēt, ņemot vērā XPS faila formātu [specifications](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS faila formāts" >}}


## Atsauces Nr.

* [XPS faila formāta specifikācijas](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)

* [XPS — Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)


