{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR2 filformat - Canon Raw 2 billedfil",
  "description":"Lær om CR2-filformat og API'er, der kan oprette og åbne CR2-filer.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2-da",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Hvad er CR2 fil?

En CR2-fil (Camera RAW 2) er en RAW-billedfil, der er oprettet af Canons digitalkameraer. Den gemmer de originale ikke-behandlede tabsfri billeddata, som er optaget af kameraet. CR2-filformatet er udviklet af Canon til sine digitale kameraer og kan optage billeder i høj kvalitet på op til 14 bits RGB. Dette giver billeder i høj kvalitet med tilstrækkelig plads til efterbehandling. CR2 billedformat er blevet brugt af Canon i deres 350D, 20D og 1D kameramodeller. CR2-filer er RAW-filer og indeholder yderligere metadataoplysninger såsom kameraoplysninger, linseoplysninger, bracketing-oplysninger, hvidbalance og andre indstillinger.

## CR2 filformat

CR2-filer gemmes på kameraets hukommelseskort som binære filer i Canons proprietære filformat. CR2-filformatet erstattede det oprindeligt brugte CRW-filformat og blev senere erstattet af Canon RAW 3-filformatet. CR2-filformatet er baseret på [TIFF](/image/tiff/)-specifikationerne, som har 4 billedfilmapper (IFD'er).

|Offset |Indhold |Kommentar|
---|---|---|
|0x0000 |Header |indeholder byte-rækkefølgen, versionen og offset til RAW-billedet|
|computed |IFD#0 |denne del indeholder Exif-sektionen, som indeholder Makernotes-sektionen.
Oplysninger om billede#0|
|beregnet |billede#0 |lille version af billedet (en fjerdedel af originalens størrelse), komprimeret i Jpeg|
|beregnet |IFD#1 |Information om billede#1.|
|beregnet |billede#1 |lille version af billedet, komprimeret i Jpeg|
|beregnet |IFD#2 |Information om billede#2.|
|beregnet |billede#2 |lille version af billedet, ikke komprimeret|
|i overskrift| IFD#3| Oplysninger om billede#3, RAW-billedet i fuld dimension|
|beregnet |billede#3 |RAW-billeddata, tabsfri komprimeret i Jpeg (ikke RGB-data!)|

## Fordel ved CR2 filformat

Lagring af billeder i RAW-format giver mulighed for en masse efterbehandling af fotografiet, såsom justering af hvidbalancen. Dette er langt vanskeligere og med et stort kvalitetstab med andre billedfilformater såsom [JPEG](/image/jpeg/).

## Er CR2 bedre end JPEG?

CR2-filer er råfiler uden tab af data og dermed intet tab af kvalitet. JPEG på den anden side er tabsgivende billedfilformat, da det mister nogle data for at reducere filen. Således er CR2-filerne af høj kvalitet og mere velegnede til retouchering og forbedringer.

## Referencer

 * [CR2-filformat](http://lclevy.free.fr/cr2/)

