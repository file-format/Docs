{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"failą",
"pratęsimas",
"Dokumento formatas",
"Puslapio išdėstymas",
"Inkapsuliuotas PostScript"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie EPS failo formatą ir API, kurios gali kurti ir atidaryti EPS failus.",
  "title": "EPS failo formatas – inkapsuliuotas PostScript failas",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra EPS failas?

.eps failas yra vaizdo failas, kuris išsaugomas diske Encapsulated Postscript failo formatu. Jame gali būti bet koks teksto, grafikos ir vaizdų derinys. EPS failuose taip pat gali būti bitmap peržiūros vaizdas, įdėtas į vidų, kad būtų rodomas programos, galinčios atidaryti tokius failus.

## Trumpa EPS failo formato istorija

Greitai pažvelgus į EPS failo formatą iš istorijos perspektyvos, atskleidžiama ši informacija:

* Pirmąją EPS versiją „Adobe“ išleido 1985–1988 m

* EPS specifikacijos 2.0 versija buvo paskelbta 1989 m. sausio mėn

* EPS 3.0 versijos specifikacija buvo paskelbta kaip atskiras dokumentas 1992 m.; tai yra naujausia paskelbta versija.


EPS, kartu su atvirų struktūrinių susitarimų išplėtimo mechanizmu, aprašytu Adobe PostScript kalbos dokumentų struktūrizavimo konvencijų specifikacijos 9 punkte, sudarė ankstyvųjų Adobe Illustrator Artwork failo formato versijų pagrindą.

## EPS failo formatas

EPS yra patentuotas, bet viešai dokumentuotas formatas, o EPS failo formato specifikacijos yra viešai prieinamos kūrėjui. EPS yra [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Dokumentų struktūros konvencija) atitinkantis failo formatas ir atitinka visas DSC nustatytas taisykles. DSC yra specialus Adobe sukurtas PostScript dokumentų failo formatas. Bet kuri programa, kuri teigia galinti skaityti EPS failus, turi būti suderinama su DSC.

EPS failą sudaro du pagrindiniai skyriai, kaip paaiškinta toliau.

### Peržiūrėti vaizdą ###

Įprastame EPS faile yra peržiūros vaizdas formatu, skirtu patogiam naudojimui darbo eigoje, kurioje dalyvauja kelios sistemos arba programos. Peržiūros tikslas – kad vaizdas būtų tokio formato, kurį galėtų pateikti dauguma grafikos programų; peržiūra paprastai yra mažesnės skyros, pikselių matmenų ir (arba) bitų gylio. Peržiūros failas gali būti vienu iš kelių formatų. EPS_3 specifikacijose išvardyti trys konkretiems įrenginiams skirtos peržiūros formatai:

* Apple Macintosh – PICT vaizdas, naudojamas QuickDraw programoje

* DOS kompiuteriams – TIFF bitmap

* Windows metafailas.


PICT ir Windows Metafile gali apimti ir bitmap duomenis, ir vektorinę grafiką. Be to, specifikacijoje apibrėžiamas labai paprastas, nuo įrenginio nepriklausomas įterptojo bitų žemėlapio peržiūros vaizdo atvaizdavimas. Šis vaizdas žinomas kaip Encapsulated PostScript Interchange Format (EPSI).

EPSI peržiūra yra taškinė schema, vaizduojama kaip ASCII šešioliktainė, suvyniota tarp kelių PostScript komentarų, kad būtų galima identifikuoti, ir skirta būti paprastam ir lengvai perkeliamam. Norint atskirti EPS failus su skirtingais peržiūros formatais, EPS specifikacijoje buvo rekomenduojami skirtingi DOS failų plėtiniai ir Macintosh failų tipai.

### PostScript kodas

Į EPS failo formatą turi būti įtraukta bent ši informacija:

* antraštės komentaras, %!PS-Adobe-3.0 EPSF-3.0

* ir ribojamojo langelio komentaras %%BoundingBox: llx lly urx ury, apibūdinantis iliustracijos ribas. Šie keturi argumentai atitinka apatinį kairįjį (llx, lly) ir viršutinį dešinįjį (urx, ury) ribojančio langelio kampus.


EPS failas negali naudoti nė vieno iš šių operatorių:

* juostinis įrenginys,

* Cleardictstack

* kopijuoti puslapį

* ištrinti puslapį

* išėjimo serveris

* rėmo įrenginys

* grestoreall

* initclip

* Initgraphics

* initmatrica

* mesti

* atvaizdavimo juostos

* setglobal

* nustatyti puslapio įrenginį

* rinkinys bendrinamas

* pradėti darbą.


## EPS konvertavimas į kitus failų formatus

EPS failus galima konvertuoti į standartinius vaizdo formatus, tokius kaip [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) ir [PDF](/pdf/), naudojant skirtingas programas, pvz., Adobe Illustrator, Photoshop ir PaintShop Pro.

Dėl [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) EPS failuose, Office 2016, Office 2013, Office 2010 ir Office 365 išjungė galimybę įterpti EPS failus į Office dokumentus.

## Nuorodos

* [Encapsulated PostScript – Vikipedija](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


