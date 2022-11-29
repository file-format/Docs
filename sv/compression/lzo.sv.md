{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Komprimerad", "Fil", "Extension", "Filformat", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO-filformat",
  "description":"Läs mer om LZO-filformat och API:er som kan skapa och öppna LZO-filer.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Vad är LZO fil? ##

En fil med filtillägget .lzo kombineras med filarkiveringsfunktioner som kan minska alla filstorlekar i den komprimerade filen. Alla de komprimerade filerna kan bestå av en eller flera filer eller till och med grupper av pärmar med flera filer av olika slag och dimensioner. Storleken på en komprimerad fil är mindre jämfört med den gemensamma storleken för alla filer och mappar som lagras i en LZO-komprimerad fil. Alla LZO-komprimerade filer lagras i LZO-formatet och exekveras explicit med komprimeringsfunktioner som används av LZOP-filkomprimerings- och dekomprimeringsmjukvaran. Alla komprimeringsspecifikationer kombineras i detta filkomprimerings- och dekomprimeringsprogram som kommer från Lempel-Ziv-Oberhumes filkomprimeringsbibliotek. Snabbare dekompressionshastighet och utvecklade kompressionsförhållanden kombineras också i dessa LZO-filer.

## LZO-specifikation ##

Markus Franz Xaver Johannes Oberhumer utvecklade den ursprungliga "lzop"-algoritmen, baserad på tidigare algoritmer av Abraham Lempel och Jacob Ziv, 1996. Detta bibliotek implementerar en mängd olika algoritmer med följande egenskaper:

* Snabbare komprimering än DEFLATE
* Snabb dekompression
* Ytterligare buffertar som behövs under komprimering (av 8KB eller 64KB storlek, beroende på komprimeringsnivå)
* Käll- och destinationsbuffertarna är allt minne som krävs för dekomprimering
* Ger kontroll över både kompressionsförhållande och kompressionshastighet

Som en blockkomprimeringsalgoritm utför LZO överlappande komprimering såväl som dekompression på plats. För att uppnå överlappande komprimering måste blockstorleken för både komprimering och dekompression matcha. LZO-komprimeringsalgoritmen delar upp indata i matchningar (en glidande ordbok) och bokstavliga ord som inte stämmer överens, vilket ger bra resultat med mycket redundanta data och acceptabla resultat med icke-komprimerbara data, vilket bara ökar inkomprimerbar data med 1/64 av originalet storlek.

## Problem med att öppna en LZO-fil ##

Följande är några problem som kan orsaka dåligt fungerande LZO-filformat:
  


* Filen kan vara korrupt. För att lösa det här problemet, ladda ner filen igen eller be avsändaren att skicka om filen igen
* Den andra orsaken är en infekterad fil i det här fallet skanna filen ordentligt
* Felaktiga länkar till LZO-filen
* Borttagning av beskrivningen av LZO
* Inte tillräckligt med hårdvaruresurser
* Föråldrade drivrutiner för utrustningen
  


## Referenser ##

* [LZO - Av Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

