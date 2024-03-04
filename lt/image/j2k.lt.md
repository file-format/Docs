{
  "date": "2019-10-11",
  "keywords": [
"j2k failą",
"j2k failo formatas",
"kas yra j2k failas",
"failą",
"j2k pavyzdys",
"j2k failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2K",
  "description": "Sužinokite apie J2K failo formatą ir API, kurios gali kurti ir atidaryti J2K failus.",
  "linktitle": "J2K",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-ltk"
}
},
  "lastmod": "2020-08-03"
}

## Kas yra J2K failas?

**J2K** failas yra vaizdas, suglaudintas naudojant bangletės glaudinimą, o ne DCT glaudinimą. Šį failo formatą naudoja Jungtinės fotografijos ekspertų grupės (JPEG) 2000 failai. J2K failai saugo metaduomenų informaciją apie vaizdo failą XML formatu, skirtingai nei .jpeg arba .jpg, kurie šiam tikslui naudoja EXIF formatą. J2K failai palaiko 15 bitų spalvas, alfa skaidrumą ir be nuostolių glaudinimą. Yra keletas komercinių API, skirtų JPEG 2000 vaizdams iššifruoti, pvz., J2K-Codec. J2K failą galima atidaryti Windows OS naudojant standartines vaizdų peržiūros priemones.

## J2K failo formatas ##

J2K failo formatas yra toks pat kaip JPEG 2000, kuris dažnai išsaugomas kaip .jp2 ir .jpc. Dėl to J2K failai naudoja tą patį metaduomenų kodavimo metodą XML formatu, kai standartas 12234-1 naudojamas kaip nuoroda tarp Exif žymų ir XML komponentų. Jis dar labiau patobulintas JPEG 2000 part-2 plėtiniu, kuris sujungia animacijos mechanizmą ir kodo srauto konfigūracijas į vieną vaizdą. Tokie išplėstinio failo formato failai išsaugomi kaip .jpx.

### JPEG2000 failo išdėstymas ###

JPEG2000 palaiko įvairias programas, pagrįstas išplečiamų failų formatų atitiktimi. Nors paprasčiausiame tipe gali būti vienas vaizdas, sudėtingesni tipai gali apimti vaizdų serijas, sukrautas vienas ant kito arba suskirstytas pagal laiką.

#### JP2 dėžutė ####
Tai yra aukščiausio lygio JP2 failo formato kūrimo blokas, kurio antraštėje yra tipo ir ilgio laukai bei duomenų sekcija. Žymiausias dėžutės tipas yra gretimos kodų srauto dėžutės. Šio langelio duomenų skyriuje saugomas JPEG2000 kodų srautas.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream yra baitų seka, reikalinga JPEG2000 suglaudintam vaizdui iššifruoti. Jei faile nėra nieko kito, išskyrus šį kodų srautą, jis vadinamas neapdorotu kodų srauto failu. Paprastai JPEG kodo srautas yra JPEG2000 glaudinimo algoritmo taikymas vaizdui, nors tai nėra vienintelis būdas.

#### Plytelių dalys ####

JPEG2000 koduotas vaizdas yra duomenų vienetų, vadinamų paketais, rinkinys. Šie paketai yra saugomi kodų sraute paketų grupėse, vadinamose plytelių dalimis. Prieš koduodamas vaizdą, koduotuvas padalija vaizdą į stačiakampį blokų tinklelį, vadinamą plytelėmis, kur kiekviena plytelė užkoduojama atskirai, neatsižvelgiant į kitas plyteles.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 failo formatas" >}}

## J2K suspaudimas ##
JPEG 2000 naudoja bangelių glaudinimo technologiją, todėl jis yra greitas, nes bet kurioje peržiūros srityje ar lange rodomas palyginti nedaug pikselių. Tai galima pabrėžti tuo, kad labai didelio dydžio (gigabaitais) vaizdams ekrane atsiras vos keli megabaitai pikselių. Tai padeda greitai gauti ir pateikti tik tą vaizdo duomenų dalį, kuri reikalinga ekrano pikseliams užpildyti. Tam taip pat reikalinga didelės spartos dekompresijos technologija, kuri pagreitintų vaizdų gavimo mechanizmą kuriant reikiamus vaizdus skrydžio metu.

J2K naudojasi greito išskleidimo pranašumais ir gauna tik reikiamą informaciją pikselių duomenims, kad dalis matomų vaizdų greitai būtų rodoma ekranuose. J2K pirmiausia skirtas duomenims peržiūrėti, o ne jų redaguoti.

## J2K identifikavimo numeris
JPEG 2000 failų parašo baitai yra 6A 50 20 20.

### Mimo tipai ###
JPEG 2000 failams registruoti MIME tipai apima:
  * vaizdas/jp2
  * vaizdas/jpx
  * vaizdas/jpm
  * video/mj2

## Patobulinimai, palyginti su JPEG standartu ##
JPEG standarto patobulinimai apima:
  * Puikus suspaudimo našumas
  * Kelių skiriamųjų gebų vaizdavimas
  * Progresyvus perdavimas pikseliu ir raiškos tikslumas
  * Suspaudimo be nuostolių arba nuostolių pasirinkimas
  * Atsparumas klaidoms, lankstus failo formatas
  * Didelio dinaminio diapazono palaikymas
  * Šoninio kanalo erdvinė informacija

## Nuorodos Nr.
  * [Taubmanas, Davidas; Marcellin, Michael (2012 m.)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

