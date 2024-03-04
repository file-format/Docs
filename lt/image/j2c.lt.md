{
  "date": "2019-10-11",
  "keywords": [
"j2c failą",
"j2c failo formatas",
"kas yra j2c failas",
"failą",
"j2c pavyzdys",
"j2c failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "Sužinokite apie J2C failo formatą ir API, kurios gali kurti ir atidaryti J2C failus.",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-ltc"
}
},
  "lastmod": "2021-02-14"
}

## Kas yra J2C failas?

Failas su plėtiniu .j2c yra JPEG failo formato variantas ir yra suglaudintas naudojant bangletės glaudinimą. Ji turi beveik identišką žymeklių ir segmentų sistemą JPEG 2000 failo formatui. J2C failo formatas yra toks, kaip apibrėžta JPEG 2000 stovo 1 dalyje, kuri palaiko ir nuostolingą, ir be nuostolių glaudinimą. JPEG 2000 kodų srautas buvo sukurtas taip, kad būtų įterptas į [JP2](/image/jp2/) arba kitą failo formatą, nors jis gali būti ir pats faile. J2C failą galima atidaryti naudojant Adobe Photoshop 2020, Adobe Illustrator 2020 ir Corel Paintshop Pro.

## J2C failo formatas

J2C failo formatas yra toks pat kaip ir JPEG 2000, kuris dažnai išsaugomas kaip .jp2 ir .jpc. Tai leidžia J2C failams taikyti tą patį metodą, koduojant metaduomenis XML formatu, kai standartas 12234-1 naudojamas kaip nuoroda tarp Exif žymų ir XML komponentų. Jis dar labiau patobulintas JPEG 2000 part-2 plėtiniu, kuris sujungia animacijos mechanizmą ir kodo srauto konfigūracijas į vieną vaizdą. Tokie išplėstinio failo formato failai išsaugomi kaip [.jpx](/image/jpx/).

### JPEG2000 failo išdėstymas

JPEG2000 palaiko įvairias programas, pagrįstas išplečiamų failų formatų atitiktimi. Nors paprasčiausiame tipe gali būti vienas vaizdas, sudėtingesni tipai gali apimti vaizdų serijas, sukrautas vienas ant kito arba suskirstytas pagal laiką.

#### JP2 dėžutė
Tai yra aukščiausio lygio JP2 failo formato kūrimo blokas, kurio antraštėje yra tipo ir ilgio laukai bei duomenų sekcija. Žymiausias dėžutės tipas yra gretimos kodų srauto dėžutės. Šio langelio duomenų skyriuje saugomas JPEG2000 kodų srautas.

#### JPEG2000 CodeStream

JPEG2000 CodeStream yra baitų seka, reikalinga JPEG2000 suglaudintam vaizdui iššifruoti. Jei faile nėra nieko kito, išskyrus šį kodų srautą, jis vadinamas neapdorotu kodų srauto failu. Paprastai JPEG kodų srautas yra JPEG2000 glaudinimo algoritmo taikymas vaizdui, nors tai nėra vienintelis būdas.

#### Plytelių dalys ####

JPEG2000 koduotas vaizdas yra duomenų vienetų, vadinamų paketais, rinkinys. Šie paketai yra saugomi kodų sraute paketų grupėse, vadinamose plytelių dalimis. Prieš koduodamas vaizdą, koduotuvas padalija vaizdą į stačiakampį blokų tinklelį, vadinamą plytelėmis, kur kiekviena plytelė užkoduojama atskirai, neatsižvelgiant į kitas plyteles.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 failo formatas" >}}

## J2C suspaudimas
JPEG 2000 naudoja bangelių glaudinimo technologiją, todėl jis yra greitas, nes bet kurioje peržiūros srityje ar lange rodomas palyginti nedaug pikselių. Tai galima pabrėžti tuo, kad labai didelio dydžio (gigabaitais) vaizdams ekrane atsiras vos keli megabaitai pikselių. Tai padeda greitai gauti ir pateikti tik tą vaizdo duomenų dalį, kuri reikalinga ekrano pikseliams užpildyti. Tam taip pat reikalinga didelės spartos dekompresijos technologija, kuri pagreitintų vaizdų gavimo mechanizmą kuriant reikiamus vaizdus.

J2C pasinaudoja greito išskleidimo pranašumais ir gauna tik reikiamą informaciją pikselių duomenims, kad dalis matomų vaizdų greitai būtų rodoma ekranuose. J2C pirmiausia skirtas duomenims peržiūrėti, o ne jų redaguoti.

## J2C identifikavimas
JPEG 2000 failai turi parašo baitus FF 4F FF 51.

### Mimo tipai
JPEG 2000 failams registruoti MIME tipai apima:
  * vaizdas/j2c
  * vaizdas/jpx
  * vaizdas/jpm
  * video/mj2

## Patobulinimai, palyginti su JPEG standartu
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

