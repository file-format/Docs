{
  "date": "2019-10-11",
  "keywords": [
"psd fails",
"psd faila formāts",
"kas ir psd fails",
"failu",
"psd piemērs",
"psd faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD — Photoshop attēla faila formāts",
  "description": "Uzziniet par PSD faila formātu un API, kas var izveidot un atvērt PSD failus.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-lvd"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PSD fails?

PSD, Photoshop Document, ir Adobe Photoshop vietējais faila formāts, ko izmanto grafikas projektēšanai un izstrādei. PSD faili var ietvert attēlu slāņus, regulēšanas slāņus, slāņu maskas, anotācijas, informāciju par failiem, atslēgvārdus un citus Photoshop specifiskus elementus. Photoshop failiem ir noklusējuma paplašinājums .PSD, un to maksimālais augstums un platums ir 30 000 pikseļi, kā arī divu gigabaitu garuma ierobežojums.

## PSD faila formāta specifikācijas ##

Dati PSD failā tiek glabāti lielā endian baitu secībā. Tas nozīmē īso un garo veselo skaitļu apmaiņu, lasot vai rakstot Windows platformā. Photoshop faila formāts ir sadalīts piecās galvenajās daļās. Tam ir daudz garuma marķieru, ko var izmantot, lai pārvietotos no vienas sadaļas uz nākamo. Garuma marķieri parasti ir polsterēti ar baitiem, lai tos noapaļotu līdz tuvākajam 2 vai 4 baitu intervālam. Piecas galvenās daļas ir:

* Faila galvene

* Krāsu režīma dati

* Attēlu resursi

* Informācija par slāni un masku

* Attēla dati


Lai nodrošinātu atbilstību, dati jāieraksta visos šajos sadaļas laukos, jo Photoshop var mēģināt izlasīt visu sadaļu. Tas arī nozīmē, ka, rakstot failā, izlaistajos laukos ir jāraksta nulles. Garuma lauks garuma norobežotajās sadaļās ir jāizmanto, lai izlemtu, kad pārtraukt lasīšanu. Vairumā gadījumu garuma laukā ir norādīts sekojošo baitu, nevis ierakstu skaits. Lasot failu, ir jāatceras šādi punkti.

* Vērtības kolonnā "Length" visās tabulās ir norādītas baitos.

* Visas vērtības, kas definētas kā unikoda virkne, sastāv no:

* 4 baitu garuma lauks, kas norāda rakstzīmju skaitu virknē (nevis baitus).

* Unikoda vērtību virkne, divi baiti katrai rakstzīmei.


### Faila galvene ###

Faila galvenē ir attēla pamatīpašības.

|Length|Apraksts
---|---|
|4|Paraksts: vienmēr vienāds ar '8BPS' . Nemēģiniet nolasīt failu, ja paraksts neatbilst šai vērtībai.
|2|Version: always equal to 1. Nemēģiniet nolasīt failu, ja versija neatbilst šai vērtībai. (~*~*PSB~*~* versija ir 2.)
|6|Rezervēts: jābūt nullei.
|2|Kanālu skaits attēlā, ieskaitot visus alfa kanālus. Atbalstītais diapazons ir no 1 līdz 56.
|4|Attēla augstums pikseļos. Atbalstītais diapazons ir no 1 līdz 30 000.
|4|Attēla platums pikseļos. Atbalstītais diapazons ir no 1 līdz 30 000.
|2|Dziļums: bitu skaits kanālā. Atbalstītās vērtības ir 1, 8, 16 un 32.
|2|Faila krāsu režīms. Atbalstītās vērtības ir: Bitmap # 0; pelēktoņu #1; Indeksēts # 2; RGB # 3; CMYK # 4; Daudzkanālu # 7; Duotone # 8; 9. laboratorija.

### Krāsu režīma datu sadaļa ###

Krāsu režīma datu sadaļa ir strukturēta šādi:


|Length|Apraksts
---|---|
|4|Šo krāsu datu garums
|mainīgs|Krāsu dati

Krāsu režīma dati ir pieejami tikai indeksētajām krāsām un divtoņiem, kā noteikts režīma laukā sadaļā Faila galvene. Visiem pārējiem režīmiem šī sadaļa ir attēlota ar 4 baitu nulles vērtībām. Indeksētiem krāsainiem attēliem garums ir 768, un krāsu dati satur attēla krāsu tabulu bez starplīmeņu secībā. Duotone attēliem krāsu datos ir ietverta divtoņu specifikācija (kuras formāts nav dokumentēts). Citas lietojumprogrammas, kas nolasa Photoshop failus, var uzskatīt divtoņu attēlu kā pelēku attēlu un tikai saglabāt divtoņu informācijas saturu, lasot un rakstot failu.

### Attēlu resursu sadaļa ###

Faila trešajā sadaļā ir attēla resursi. Tas sākas ar garuma lauku, kam seko resursu bloku sērija.


|Length|Apraksts
---|---|
|4|Attēla resursa sadaļas garums. Garums var būt nulle.
|Mainīgais|Attēla resursi (Attēlu resursu bloki)

Attēlu resursi tiek izmantoti, lai saglabātu ar attēliem nesaistītus datus, piemēram, pildspalvas rīku ceļus. Tie tiek saukti par resursu blokiem, jo tajos ir dati, kas tika saglabāti Macintosh resursā sākotnējās Photoshop versijās. Attēlu resursu bloku pamatstruktūra ir šāda:


|Length|Apraksts
---|---|
|4|Paraksts: '8BIM
|2|Unikāls resursa identifikators. Attēlu resursu ID satur Photoshop izmantoto resursu ID sarakstu.
|Mainīgais|Nosaukums: Pascal virkne, polsterēta, lai izmērs būtu vienmērīgs (nulles nosaukums sastāv no diviem baitiem no 0)
|4|Tālāk norādīto resursu datu faktiskais lielums
|Mainīgs|Resursu dati, kas aprakstīti sadaļās par atsevišķiem resursu veidiem. Tas ir polsterēts, lai izmērs būtu vienmērīgs.

Attēlu resursi izmanto vairākus standarta ID numurus.

### Slāņa un maskas informācija ###

Ceturtajā Photoshop faila sadaļā ir informācija par slāņiem un maskām, piemēram, slāņu skaitu, slāņu kanāliem, sajaukšanas diapazoniem, regulēšanas slāņa taustiņiem, efektu slāņiem un maskas parametriem. Ja nav slāņu vai masku, šī sadaļa tiek attēlota ar nulles 4 baitu lauku. Šīs sadaļas lasīšanas laikā īpaša uzmanība jāpievērš sadaļu garumam nulles vērtību dēļ. Slāņa un maskas sadaļas izkārtojums ir šāds:


|Length|Apraksts
---|---|
|4|Slāņa un maskas informācijas sadaļas garums. (PSB garums ir 8 baiti.)
|Mainīgs|Slāņa informācija
|Mainīgs|Informācija par globālo slāņu masku
|Mainīgs|Atzīmētu bloku sērija, kas satur dažāda veida datus.

#### Slāņa informācija ####

Nākamajā tabulā parādīta slāņa informācijas augsta līmeņa organizācija.


|Length|Apraksts
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB garums ir 8 baiti.)
|2|Slāņu skaits. Ja tas ir negatīvs skaitlis, tā absolūtā vērtība ir slāņu skaits, un pirmajā alfa kanālā ir apvienotā rezultāta caurspīdīguma dati.
|Mainīgs|Informācija par katru slāni. Sadaļā Slāņa ieraksti ir aprakstīta šīs informācijas struktūra katram slānim.
|Mainīgs|Kanāla attēla dati. Satur vienu vai vairākus attēla datu ierakstus katram slānim. Slāņi ir tādā pašā secībā kā slāņa informācijā

### Attēla dati ###

Attēla pikseļu dati ir ietverti faila sadaļā Attēla dati. Datu izkārtojums attēla datu sadaļā ir plakanā secībā, ti, vispirms visi sarkanie dati, tad visi zaļie dati utt. Katra plakne tiek saglabāta skenēšanas līnijas secībā, bez pad baitiem. Attēla datu sadaļa ir sakārtota formātā kā parādīts nākamajā tabulā.

|Length|Apraksts
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE saspiests, attēla dati sākas ar baitu skaitu visās skenēšanas līnijās (rindas * kanāli), un katrs skaits tiek saglabāts kā divu baitu vērtība. Tālāk seko RLE saspiestie dati, katru skenēšanas līniju saspiežot atsevišķi. RLE saspiešana ir tas pats saspiešanas algoritms, ko izmanto Macintosh ROM rutīnas PackBits un TIFF standarts. *2 = ZIP bez paredzēšanas *3 = ZIP ar prognozi.
|Mainīgs|Attēla dati. Planar order = RRR GGG BBB utt.

## Atsauces Nr.

* [PSD faila formāta specifikācijas — Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop faila formāts](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


