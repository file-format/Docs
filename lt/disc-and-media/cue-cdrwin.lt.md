{
   "date":"2023-10-18",
   "keywords":[
"užuomina",
"signalo failas",
"cue cdrwin cue lapo failas",
"kaip atidaryti signalo failą",
"failą",
"cue failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CUE failo formatas – CDRWIN Cue lapas",
   "description":"Sužinokite apie CUE CDRWIN Cue Sheet failo formatą ir API, kurios gali kurti ir atidaryti CUE failus.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin-lt",
         "parent":"disc-and-media"
}
},
   "lastmod":"2023-10-18"
}

## Kas yra CUE failas?

**.CUE** failas, taip pat žinomas kaip **CDRWIN Cue Sheet**, yra paprasto teksto failas, kuriame pateikiama informacija apie garso kompaktinio disko arba disko vaizdo takelius ir išdėstymą, paprastai BIN arba ISO formatu. Šie failai dažnai naudojami disko struktūrai ir turiniui apibūdinti, todėl CD įrašymo programinė įranga arba virtualaus disko programinė įranga gali tiksliai atkurti originalų diską.

## CUE failo pavyzdys

Štai pavyzdys, kaip gali atrodyti .cue failas:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN lazdos lapas

CDRWIN Cue Sheet yra specifinis .cue failo formato variantas, naudojamas CDRWIN programinėje įrangoje. CDRWIN yra CD / DVD įrašymo ir kūrimo programinė įranga, o jos .cue lapai yra skirti naudoti su šia programine įranga. Šiuose .cue lapuose yra informacijos, reikalingos CDRWIN norint tiksliai sukurti arba įrašyti CD ar DVD.

Štai keletas pagrindinių CDRWIN Cue Sheets detalių:

1.  **Unikalus CDRWIN**: CDRWIN .cue lapai yra patentuotas formatas, būdingas CDRWIN programinei įrangai. Nors jie turi panašumų su standartiniais .cue failais, jie yra pritaikyti dirbti su CDRWIN funkcijomis ir nustatymais.
    
2.  **Patogi sąsaja**: CDRWIN suteikia lengvai naudojamą sąsają .cue lapams kurti ir redaguoti. Vartotojai gali patogiai pridėti arba keisti informaciją apie takelius, indeksus, spragas ir kitus parametrus.
    
3.  **Suderinami diskų tipai**: CDRWIN Cue Sheets pirmiausia naudojami kuriant įvairių tipų kompaktinius ir DVD diskus, įskaitant duomenų diskus, garso kompaktinius diskus, mišraus režimo diskus ir kt. Formatas leidžia vartotojams nurodyti norimo sukurti disko tipą ir turinį.
    
4.  **Disko išdėstymo valdymas**: CDRWIN Cue Sheets leidžia išsamiai valdyti disko išdėstymą ir struktūrą, įskaitant takelių tvarką, pauzės / tarpo nustatymus ir bet kokias kitas konkrečias vartotojo nuostatas.
    
5.  **ISO ir BIN palaikymas**: CDRWIN gali dirbti su ISO ir BIN disko vaizdo formatais. Lapas .cue nurodo, kuris vaizdo failas naudojamas diske, užtikrinant tinkamą ženklų ir vaizdo sinchronizavimą.
    
6.  **Įrašymas ir kopijavimas**: šie .cue lapai yra labai svarbūs įrašant diskus arba kopijuojant takelius iš diskų naudojant CDRWIN. Jie padeda užtikrinti, kad galutinis produktas atitiktų numatytą išdėstymą ir turinį.
    
7.  **Atsarginis kopijavimas ir atkūrimas**: CDRWIN naudotojai dažnai sukuria .cue lapus kurdami atsargines kompaktinių arba DVD diskų kopijas. Šie lapai vėliau gali būti naudojami disko turiniui atkurti, įskaitant takelio išdėstymą ir laiką.

## Kaip atidaryti CUE failą?

CDRWIN Cue Sheets yra specialiai sukurti CDRWIN programinei įrangai, todėl paprastai jie skirti atidaryti ir naudoti CDRWIN.

Programos, kurios atidaro arba nurodo CUE failus

- CDRWIN
- Išmanieji projektai IsoBuster
- EZB Systems UltraISO

## Kiti CUE failai

Štai kiti failų tipai, kuriuose naudojamas **.cue** failo plėtinys.

**Diskas ir laikmena**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## Nuorodos
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)


