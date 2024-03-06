{
  "date": "2021-02-15",
  "keywords": [
"asf fails",
"asf faila formātā",
"kas ir asf fails",
"failu",
"asf piemērs",
"asf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF — uzlaboto sistēmu faila formāts",
  "description": "Uzziniet par ASF faila formātu un API, kas var izveidot un atvērt ASF failus.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-lvf"
}
},
  "lastmod": "2021-02-16"
}

## Kas ir ASF fails?

Fails ar paplašinājumu .asf ir multivides faila formāts digitālo multivides straumju glabāšanai un atskaņošanai tīklā. Tas ir konteinera faila formāts, kurā var būt gan video, gan audio saturs straumēšanai tiešsaistē. Jūs reti atradīsit ASF failus, un, visticamāk, jūs saskaraties ar Windows Media Audio ([WMA](/audio/wma/)) un Windows Media Video ([WMV](/video/wmv/)) failiem, kas abi norāda ASF failus, kuru saturs ir kodēts ar atbilstošiem kodekiem. Windows multivides failus var izveidot un lasīt, izmantojot Windows Media Format SDK.

## ASF faila formāts

ASF failā var būt vairākas neatkarīgas vai atkarīgas straumes. Tas var ietvert vairākas audio straumes daudzkanālu audio vai vairākas bitu pārraides ātruma video straumes. Vairāki bitu pārraides ātrumi padara straumes piemērotas pārraidei dažādos joslas platumos. Turklāt ASF faila straumes var būt saspiestā vai nesaspiestā formātā. Vislabākā saspiešana tiek panākta, izmantojot Microsoft Windows Media Audio and Video 9 Series kodekus. Pilnīgas ASF faila formāta specifikācijas ir pieejamas vietnē [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF augstākā līmeņa failu struktūra

ASF faili loģiski satur trīs veidu augstākā līmeņa objektus:

* `Header Object` — obligāts un jāievieto katra ASF faila sākumā

* `Datu objekts` - obligāts un jāseko galvenes objektam

* "Indeksa objekts(-i)" — neobligāts, taču noderīgs, lai nodrošinātu uz laiku balstītu nejaušu piekļuvi ASF failiem


Nākamajā attēlā parādīta ASF failu augstākā līmeņa failu struktūra.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF augstākā līmeņa galvenes objekts

Objekts Header nodrošina labi zināmu baitu secību ASF failu sākumā un pēc izvēles var saturēt metadatus, piemēram, bibliogrāfisko informāciju. Tajā ir visa informācija, kas nepieciešama, lai pareizi interpretētu informāciju datu objektā. Galvenes objekts var ietvert vairākus standarta objektus, tostarp, bet ne tikai:

 * Faila rekvizītu objekts — satur globālos faila atribūtus.
 * Straumes rekvizītu objekts — definē digitālās multivides straumi un tās īpašības.
 * Header Extension Object — ļauj ASF failam pievienot papildu funkcionalitāti, vienlaikus saglabājot atpakaļejošu saderību.
 * Saturs Apraksts Objekts — satur bibliogrāfisku informāciju.
 * Skripta komandas objekts — satur komandas, kuras var izpildīt atskaņošanas laika skalā.
 * Marķiera objekts — nodrošina nosauktus lēciena punktus failā.

Galvenes objekts tiek attēlots, izmantojot šādu struktūru:

|Lauka nosaukums |Lauka tips |Izmērs (biti)|
---|---|---|
|Objekta ID| GUID| 128|
|Objekta izmērs| QWORD| 64|
|Galvenes objektu skaits| DWORD| 32|
|Rezervēts1| BAITS| 8|
|Rezervēts2| BAITS| 8|

#### ASF augstākā līmeņa datu objekts

Visi ciparu multivides dati ASF failam ir ietverti datu objektā un tiek glabāti ASF datu pakešu veidā. Katra datu pakete ir noteikta garuma un satur datus vienai vai vairākām digitālo multivides straumēm.

#### ASF augstākā līmeņa indeksa objekti

ASF augstākā līmeņa indeksa objektiem ir šādi divi veidi:

 * Vienkāršs indeksa objekts — satur uz laiku balstītu video datu indeksu ASF failā. Laika intervāls starp indeksa ierakstiem ir nemainīgs un tiek saglabāts vienkāršā indeksa objektā.
 * Indeksa objekts — attiecas uz indeksa objektu, multivides objekta indeksa objektu un laika koda indeksa objektu, kuru formāti ir līdzīgi. Tāpat kā vienkāršais indeksa objekts, indeksa objekts indeksē pēc laika ar fiksētu laika intervālu, bet neaprobežojas tikai ar video straumēm.

## Atsauces

* [ASF faila formāts — Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [QuickTime faila formāts — Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


