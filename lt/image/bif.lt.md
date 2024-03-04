{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF failas – „Ventana“ visos skaidrės vaizdo formatas",
  "description":"Sužinokite apie BIF failo formatą ir API, kurios gali kurti ir atidaryti BIF failus.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-lt",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Kas yra BIF failas?

BIF failas yra rastrinio vaizdo failas, kuriame yra skaidrės pavyzdys. Jį sudaro keli TIFF vaizdai, kurie skaidrių peržiūros programomis sujungiami į vieną sudėtinį vaizdą. BIF failai sukurti naudojant Ventana Medical Systems skaitmeninių skaidrių skaitytuvą ir visiškai suderinami su [TIFF](/image/tiff/) v 6.0 apibrėžimo BigTIFF variantu.

## BIF failo formatas

BIF failas išsaugomas kaip dvejetainis vaizdo failas ir jį sudaro net 200 000 x 200 000 pikselių. Tai gali sukelti didelių failų dydžių ir pažeisti 4 GB dydžio ribą, nustatytą 32 bitų failų rodyklėmis, apibrėžtomis TIF standarte. Tačiau naudojant 64 bitų failų rodykles, šią failo dydžio kliūtį įveikia TIFF standarto BigTIFF variantas.

### Kas naudoja BIF failą?

BIF failus naudoja skaitmeniniai skaidrių skaitytuvai, norėdami nuskaityti ir kurti skaitmenines skaidrių pavyzdžių kopijas. Jei esate patologas, galite atidaryti šiuos BIF failus skaidrių peržiūros programose. Turėdami didelį detalių lygį ir didelės raiškos duomenis, galite priartinti ir nutolinti skaidrės vaizdą, kad peržiūrėtumėte daugiau ar mažiau detalių pavyzdžių. Šiuose failuose esantis [XML](/web/xml/) metaduomenų failas apibrėžia, kaip turi būti derinami vaizdai ir koks vaizdas turi būti naudojamas kaip failo miniatiūra.

## Kaip atidaryti BIF failą?

BIF failus galite atidaryti naudodami:

 * OpenSlide (keli platforma)
 * ImageJ (keli platforma)
 * NetScope Viewer (Windows)

## Nuorodos Nr.

 * [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

