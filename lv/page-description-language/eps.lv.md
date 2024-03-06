{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"failu",
"pagarinājumu",
"faila formātā",
"Lapas izkārtojums",
"Iekapsulēts PostScript"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par EPS failu formātu un API, kas var izveidot un atvērt EPS failus.",
  "title": "EPS faila formāts — iekapsulēts PostScript fails",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir EPS fails?

.eps fails ir attēla fails, kas tiek saglabāts diskā Encapsulated Postscript faila formātā. Tajā var būt jebkura teksta, grafikas un attēlu kombinācija. EPS failos var būt ietverts arī bitkartes priekšskatījuma attēls, kas ir iekapsulēts, lai tos varētu parādīt lietojumprogrammas, kuras var atvērt šādus failus.

## Īsa EPS faila formāta vēsture

Ātri apskatot EPS faila formātu no vēstures viedokļa, tiek atklāta šāda informācija:

* Pirmo EPS versiju Adobe izlaida laikā no 1985. līdz 1988. gadam

* EPS specifikācijas 2.0 versija tika publicēta 1989. gada janvārī

* EPS versijas 3.0 specifikācija tika publicēta kā atsevišķs dokuments 1992. gadā; šī ir jaunākā publicētā versija.


EPS kopā ar Open Structuring Conventions paplašinājuma mehānismu, kas aprakstīts Adobe PostScript valodas dokumentu strukturēšanas konvenciju specifikācijas 9. punktā, veidoja Adobe Illustrator Artwork faila formāta agrīno versiju pamatu.

## EPS faila formāts

EPS ir patentēts, bet publiski dokumentēts formāts, un EPS faila formāta specifikācijas ir publiski pieejamas izstrādātāju uzziņai. EPS ir [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Dokumentu strukturēšanas konvencija), kas atbilst faila formātam, un tas atbilst visiem DSC noteiktajiem noteikumiem. DSC ir īpašs Adobe PostScript dokumentu faila formāts. Jebkurai lietojumprogrammai, kas apgalvo, ka tā spēj lasīt EPS failus, ir jābūt saderīgai ar DSC.

EPS fails sastāv no divām galvenajām sadaļām, kā paskaidrots tālāk.

### Priekšskatījuma attēls ###

Tipisks EPS fails satur priekšskatījuma attēlu formātā, kas paredzēts ērtai lietošanai darbplūsmā, kas ietver vairākas sistēmas vai lietojumprogrammas. Priekšskatījuma mērķis ir izveidot attēlu tādā formātā, kādu var atveidot lielākā daļa grafikas lietojumprogrammu; priekšskatījumam parasti ir zemāka izšķirtspēja, pikseļu izmēri un/vai bitu dziļums. Priekšskatījuma fails var būt vienā no vairākiem formātiem. EPS_3 specifikācijā ir norādīti trīs ierīcei raksturīgi priekšskatījuma formāti:

* Apple Macintosh PICT attēls, ko izmanto lietojumprogramma QuickDraw

* DOS datoriem TIFF bitkarte

* Windows metafails.


PICT un Windows Metafile var ietvert gan bitkartes datus, gan vektorgrafiku. Turklāt specifikācijā ir definēts ļoti vienkāršs no ierīces neatkarīgs attēlojums iegultam bitkartes priekšskatījuma attēlam. Šis attēlojums ir pazīstams kā Encapsulated PostScript Interchange Format (EPSI).

EPSI priekšskatījums ir bitkarte, kas attēlota kā ASCII heksadecimālā sistēma, kas atrodas starp dažiem PostScript komentāriem identifikācijai un ir paredzēta vienkāršai un viegli pārnēsājamai. Lai atšķirtu EPS failus ar dažādiem priekšskatījuma formātiem, EPS specifikācijā tika ieteikti dažādi DOS failu paplašinājumi un Macintosh failu tipi.

### PostScript kods

EPS faila formātā ir jāietver vismaz:

* galvenes komentārs, %!PS-Adobe-3.0 EPSF-3.0

* un ierobežojošā lodziņa komentārs %%BoundingBox: llx lly urx ury, kas apraksta ilustrācijas robežas. Šie četri argumenti atbilst ierobežojošā lodziņa apakšējam kreisajam (llx, lly) un augšējam labajam (urx, ury) stūrim.


EPS failā nevar izmantot nevienu no šiem operatoriem:

* joslas ierīce,

* Cleardictstack

* kopēt lapu

* dzēst lapu

* izejas serveris

* rāmja ierīce

* grestoreall

* initclip

* initgraphics

* initmatrix

* atmest

* renderjoslas

* setglobal

* iestatīt lapas ierīci

* koplietots

* sākt darbu.


## EPS konvertēšana uz citiem failu formātiem

EPS failus var pārveidot standarta attēlu formātos, piemēram, [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) un [PDF](/pdf/), izmantojot dažādas lietojumprogrammas, piemēram, Adobe Illustrator, Photoshop un PaintShop Pro.

Sakarā ar [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) EPS failos, Office 2016, Office 2013, Office 2010 un Office 365 ir atspējojusi iespēju ievietot EPS failus Office dokumentos.

## Atsauces

* [Encapsulated PostScript — Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


