{
  "date": "2019-10-11",
  "keywords": [
"png failu",
"png faila formātā",
"kas ir png fails",
"failu",
"png piemērs",
"png faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PNG faila formāts — rastra attēla fails",
  "description": "Uzziniet par PNG faila formātu un API, kas var izveidot un atvērt PNG failus.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PNG fails?

**PNG** (Portable Network Graphics) fails ir rastra attēla faila formāts, kas izmanto bezzudumu saspiešanu. Šis faila formāts tika izveidots, lai aizstātu grafikas apmaiņas formātu ([GIF](/image/gif/)), un tam nav autortiesību ierobežojumu. Tomēr PNG faila formāts neatbalsta animācijas. PNG faila formāts atbalsta bezzudumu attēlu saspiešanu, kas padara to populāru lietotāju vidū. Laika gaitā PNG ir kļuvis par vienu no plaši izmantotajiem attēlu failu formātiem.

## Īsa PNG faila formāta vēsture

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Tālāk ir norādīti galvenie notikumi saistībā ar PNG failu formātiem.

* 1996. gada oktobris: tika izlaista PNG specifikāciju versija 1.0, kas vēlāk parādījās kā [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. 1996. gada oktobrī tas kļuva par W3C ieteikumu.

* 1998. gada decembris: tika izlaista versija 1.1 ar nelielām izmaiņām un trīs jaunu daļu pievienošanu.

* 1999. gada augusts: tika izlaista versija 1.2, pievienojot vienu papildu daļu.

* 2003. gada novembris: PNG kļuva par starptautisku standartu (ISO/IEC 15948:2003). Šī PNG versija tikai nedaudz atšķiras no versijas 1.2, un tajā nav pievienoti jauni gabali.

* 2004. gada marts: ISO/IEC 15948:2004


## GIF un PNG funkcionālais salīdzinājums

PNG faila formāts tika izstrādāts tā, lai tas būtu vienkāršs un pārnēsājams, juridiski neapgrūtināts, maināms, elastīgs un izturīgs. Šajā tabulā ir uzskaitīti GIF līdzekļi, kas papildus jaunajiem līdzekļiem tiek mantoti ar PNG faila formātu.

|Funkcija|GIF|PNG|
---|---|---|
|Indeksa krāsu attēli līdz 256 krāsām|Jā|Jā|
|Straumēšanas atbalsts|Jā|Jā|
|Pārredzamība|Jā|Jā|
|Papildinformācija|Jā|Jā|
|Aparatūras un platformas neatkarība|Jā|Jā|
|Efektīvs|Jā|Jā|
|Truecolor attēli līdz 48 bitiem pikselī|Nē|Jā|
|Pelēktoņu attēli līdz 16 bitiem pikselī|Nē|Jā|
|Pilns alfa kanāls (vispārējās caurspīdīguma maskas)|Nē|Jā|
|Attēla gamma informācija|Nē|Jā|
|Uzticamība|Nē|Jā|
|Ātrāka sākotnējā prezentācija|Nē|Jā|

## PNG faila struktūra

Gandrīz visas operētājsistēmas atbalsta PNG failu atvēršanu. Piemēram, Microsoft Windows skatītājam ir iespēja atvērt PNG failus, jo operētājsistēmai pēc noklusējuma ir pieejams atbalsts kā daļa no instalēšanas. PNG fails sastāv no PNG paraksta, kam seko //chunks// sērijas.

### PNG faila galvene

Pirmie astoņi PNG faila baiti vienmēr satur šādas (decimāldaļas) vērtības:

{{{137 80 78 71 13 10 26 10 }}}

Šis paraksts norāda, ka pārējā faila daļā ir viens PNG attēls, kas sastāv no daļu sērijas, kas sākas ar IHDR gabalu un beidzas ar IEND gabalu.

### Gabali ###

Katrs gabals sastāv no četrām daļām:

**Length:** 4 baitu neparakstīts vesels skaitlis, kas norāda baitu skaitu gabala datu laukā. Garumā tiek skaitīts tikai datu lauks, nevis pats, gabala tipa kods vai CRC. Nulle ir derīgs garums. Lai gan kodētājiem un dekodētājiem garums jāuzskata par neparakstītu, tā vērtība nedrīkst pārsniegt 231 baitu.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Chunk Data:** Datu baiti, kas atbilst gabala veidam, ja tādi ir. Šī lauka garums var būt nulle.

**CRC:** 4 baitu CRC (Cyclic Redundancy Check), kas aprēķināts no iepriekšējiem gabala baitiem, tostarp gabala tipa koda un gabala datu laukiem, bet ne garuma lauku. CRC vienmēr ir klāt, pat tiem gabaliem, kuros nav datu.

Datu daļas garums var būt jebkurš baitu skaits līdz maksimālajam; tāpēc īstenotāji nevar pieņemt, ka gabali ir izlīdzināti uz robežām, kas ir lielākas par baitiem.

Daļas var parādīties jebkurā secībā, ievērojot ierobežojumus, kas noteikti katram gabalu veidam. (Viens ievērības cienīgs ierobežojums ir tāds, ka IHDR ir jāparādās vispirms un IEND jāparādās pēdējam; tādējādi IEND gabals kalpo kā faila beigu marķieris.) Var parādīties vairāki viena veida gabali, taču tikai tad, ja tas ir īpaši atļauts šim tipam.

#### Daļu veidi

Daļu veidi tiek iedalīti **Kritiski** un **Papildu** daļās, pamatojoties uz 4 baitu reģistrjutīgo ASCII vērtību, kas piešķirta fragmenta veidam. Visām implementācijām ir jāsaprot un veiksmīgi jāatveido standarta kritiskie gabali. Derīgā PNG attēlā ir jāietver IHDR gabals, viens vai vairāki IDAT gabali un IEND gabals.

### Saspiešana

PNG saspiešanas metode 0 (vienīgā saspiešanas metode, kas pašlaik ir definēta PNG) nosaka saspiešanu ar bīdāmo logu, kas nepārsniedz 32 768 baitus. Deflācijas saspiešana ir LZ77 atvasinājums, ko izmanto zip, gzip, pkzip un saistītās programmās. Ir veikti plaši pētījumi, lai atbalstītu tās patentbrīvā statusu. Saspiestie dati zlib datu plūsmā tiek glabāti kā bloku sērija, no kuriem katrs var attēlot neapstrādātus (nesaspiestus) datus, LZ77 saspiestus datus, kas kodēti ar fiksētiem Hafmena kodiem, vai LZ77 saspiestus datus, kas kodēti ar pielāgotiem Hufmena kodiem. Marķiera bits pēdējā blokā identificē to kā pēdējo bloku, ļaujot dekodētājam atpazīt saspiestās datu straumes beigas.

#### Pirmssaspiešanas filtrēšana

Lai sagatavotu attēla datus optimālai saspiešanai, tiek izmantoti pirmssaspiešanas filtri. PNG filtra metode definē piecus pamata filtru veidus šādi:

|Filtra veids|Nosaukums|Paredzamā vērtība|
---|---|---|
|0|Nav|Skenēšanas līnija tiek pārsūtīta nemodificēta|
|1|Sub|pārraida atšķirību starp katru baitu un iepriekšējā pikseļa atbilstošā baita vērtību.|
|2|Uz augšu|Filtrs Augšup() ir tāpat kā Sub() filtrs, izņemot to, ka pikselis tieši virs pašreizējā pikseļa, nevis tikai pa kreisi, tiek izmantots kā prognozētājs.|
|3|Vidējais|Filtrs Average() izmanto divu blakus esošo pikseļu vidējo vērtību (pa kreisi un augstāk), lai prognozētu pikseļa vērtību.|
|4|Paeth|Paeth() filtrs aprēķina vienkāršu trīs blakus esošo pikseļu lineāro funkciju (pa kreisi, augšā, augšā pa kreisi), pēc tam par prognozētāju izvēlas blakus pikseļu, kas ir vistuvāk aprēķinātajai vērtībai.|

Filtrēšanas algoritmi tiek piemēroti baitiem, nevis pikseļiem, neatkarīgi no attēla bitu dziļuma vai krāsu veida. Filtrēšanas algoritmi darbojas ar baitu secību, ko veido skenēšanas līnija. Ja attēlā ir alfa kanāls, alfa dati tiek filtrēti tāpat kā attēla dati.

Kad attēls ir pārripots, filtrēšanas nolūkos katra pītās raksta gājiens tiek uzskatīts par neatkarīgu attēlu. Filtri darbojas uz baitu secībām, ko veido pikseļi, kas faktiski pārraidīti caurlaides laikā, un iepriekšējā skenēšanas līnija ir tā, kas iepriekš tika pārraidīta tajā pašā caurlaidē, nevis tā, kas atrodas blakus visā attēlā. Ņemiet vērā, ka vienā piegājienā pārraidītais apakšattēls vienmēr ir taisnstūrveida, taču tā platums un/vai augstums ir mazāks nekā visa attēla daļa. Filtrēšana netiek lietota, ja šis apakšattēls ir tukšs.

## Atsauces Nr.

* [PNG — sākumlapa](http://www.libpng.org/pub/png/)


