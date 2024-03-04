{
  "date": "2021-08-11",
  "keywords": [
"wim failą",
"wim failo formatas",
"kas yra wim failas",
"failą",
"wim pavyzdys",
"wim failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WIM failo formatą ir API, kurios gali kurti ir atidaryti WIM failus.",
  "title": "WIM – „Windows“ vaizdo formato failas",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wi-ltm"
}
},
  "lastmod": "2021-08-11"
}

## Kas yra WIM failas?
Failai su .wim plėtiniais pirmą kartą buvo matyti sistemoje Windows Vista. WIM priklauso failų pagrindu sukurtam vaizdo formatui, kuris paprastai buvo įdiegtas Microsoft Windows Vista. Tai leidžia vieną disko vaizdą įdiegti įvairiose kompiuterių platformose. WIM failai naudojami failams, pvz., naujinimams, tvarkykles ir komponentams tvarkyti, iš naujo nepaleidžiant operacinės sistemos vaizdo. AQ WIM faile yra failų rinkinys ir susiję metaduomenys, kurie yra labai panašūs į kitus disko failų formatus.

## WIM failų formatai
WIM failo formatas nėra panašus į sektorių formatus, tokius kaip VHD arba IS, iš tikrųjų jis yra pagrįstas failais, o tai reiškia, kad pagrindinis WIM informacijos vienetas yra failas. Pagrindinis failų pagrįstumo pranašumas yra tas, kad failų sistemos medyje kelis kartus nurodomas vieno atvejo failo saugojimas ir aparatinės įrangos nepriklausomybė. Tai sumažina įvairių failų atidarymo ir uždarymo išlaidas atskirai, nes failai saugomi viename WIM. failą. WIM failai gali saugoti kelis disko vaizdus, kurie nurodomi pagal jų unikalų pavadinimą arba skaitinį indeksą.
### Suspaudimo algoritmų palaikymas
WIM palaiko šias mažėjančio greičio ir didėjančio santykio glaudinimo algoritmų šeimas:
- XPRESS
- LZX
- LZMS
- Tvirtas suspaudimas.
Pirmosios trys šeimos yra pagrįstos LZ77, o Solid-compression buvo pristatytas kartu su LZMS WIMGAPI Windows 8 ir DISM Windows 8.1.
### WIM failo formato įrankiai
Šie įrankiai paprastai palaiko WIM failo formatą:

– **ImageX**: komandų eilutės įrankis, naudojamas redaguoti, kurti ir įdiegti Windows disko vaizdus Windows vaizdo formatu. Kartu su atitinkamu WIMGAPI jis platinamas kaip nemokamo Windows automatinio diegimo rinkinio dalis. Pradedant nuo Windows Vista, Windows sąranka naudoja WAIK API, kad įdiegtų Windows.
– **DISM**: Windows 7 ir Windows Server 2008 R2 įdiegtas įrankis, galintis atlikti su paslauga susijusias užduotis Windows diegimo atvaizde, nesvarbu, ar tai būtų internetinis vaizdas, ar neprisijungęs vaizdas aplanke ar WIM faile. šis įrankis galėjo prijungti ir atjungti vaizdus, pridėti įrenginio tvarkyklę prie vaizdo neprisijungus ir pateikti užklausas dėl įdiegtų įrenginio tvarkyklių neprisijungus pasiekiamame vaizde.
 



## Nuorodos 

* [Windows vaizdo formatas – pateikė Vikipedija](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



