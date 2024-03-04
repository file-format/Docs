{
  "date": "2019-10-11",
  "keywords": [
"jp2 failą",
"jp2 failo formatas",
"kas yra jp2 failas",
"failą",
"jp2 pavyzdys",
"jp2 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 – vaizdo failo formatas",
  "description": "Sužinokite apie JP2 failo formatą ir API, kurios gali kurti ir atidaryti JP2 failus.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-lt2"
}
},
  "lastmod": "2020-08-10"
}

## Kas yra JP2 failas? ##

JPEG 2000 (**JP2**) yra vaizdo kodavimo sistema ir pažangiausias vaizdo glaudinimo standartas. Ji naudoja banglečių technologiją, kad iš karto koduotų bet kokios kokybės turinį be nuostolių. Be to, be jokios didelės nuobaudos dėl kodavimo efektyvumo, JPEG 2000 turi galimybę pasiekti ir efektyviai iššifruoti tą patį turinį į daugybę kitų skiriamųjų gebų ir savybių. JPEG 2000 kodo srautai yra labai keičiami, nes yra dominančių regionų, kurie suteikia galimybę atsitiktinei erdvinei prieigai.

JPEG 2000 yra vienas iš labiausiai keičiamo dydžio standartų. Įvairios vaizdo dalys gali būti saugomos naudojant įvairias savybes. Pažymėtinas našumo padidėjimas gali būti pasiektas užsakius kodo srautą įvairiais būdais. Nepaisant to, JP2 reikalauja sudėtingų ir sudėtingų skaičiavimo koduotuvų / dekoderių, kaip šio lankstumo rezultatas. Palyginti su JPEG, JPEG 2000 sukuria tik skambėjimo artefaktus, dėl kurių žiedai šalia vaizdo krašto ir gali būti neryškūs, o JPEG naudoja 8 × 8 vaizdo artefaktų blokus, kurie gali būti ir skambantys, ir blokuojantys artefaktai. Turi iki 16384 įvairių komponentų, kurių matmenys yra terapikseliais, o tikslumas gali siekti 38 bitus/pavyzdį.

## Istorija ##

2000 m. Jungtinės fotografijos ekspertų grupės komitetas sukūrė JP2, siekdamas patobulinti savo atskirą kosinuso transformaciją pagrįstą JPEG standartą naudojant šį naują bangele pagrįstą metodą. JPEG komitetas siekė pateikti savo bazinius metodus nemokant licencijos mokesčių. JP2 licencijoje, kuri konkuravo tarp 20 įmonių, jos laimėjo pergale. JPEG 2000 buvo paskelbtas ISO standartu, nors dauguma interneto naršyklių nėra pasirengusios padėti JPEG 2000 nuo 2017 m.

## JPEG 2000 vaizdo kodavimo sistemos dalys ##

Toliau pateikiamos pagrindinės dalys, kurios sudaro visą JPEG 2000 standartų rinkinį.


|Dalis|Pavadinimas|Aprašymas|Numeris
---|---|---|---|
|1 dalis|Pagrindinė kodavimo sistema| Apibrėžia kodo srauto sintaksę. Įvairūs JPEG 2000 vaizdų dekodavimo etapai. Paaiškina pagrindinį JP2 failo formatą, metaduomenis ir IP teises.|ISO/IEC 15444-1
|2 dalis|Plėtiniai|Apibrėžia failo formato kodo srauto plėtinius ir leidžia demonstruoti HDR pavyzdžius, nurodyti spalvų erdvės specifikacijas, apkarpyti, geometrines transformacijas; įvairios animacijos, metaduomenys ir kelių kodų srautas.|ISO/IEC 15444-2
|3 dalis|Motion JPEG 2000 (MJ2 arba MJP2)|Įveskite failo formatą judesių sekoms, koduojančius vaizdus į nepriklausomą kodo srautą.|ISO/IEC 15444-3
|4 dalis | Atitiktis | Nurodo kodavimo ir dekodavimo bandymo metodus ir tikrina pliko kodo srautų ir JP2 failų failus.|ISO/IEC 15444-4
|5 dalis | Pamatinė programinė įranga|Susideda iš dviejų šaltinio kodo paketų (Java, C), kuriuose įdiegta pagrindinė kodavimo sistema ir kuriuos galima įsigyti pagal atvirojo kodo licencijas.|ISO/IEC 15444-5
|6 dalis|Sudėtinis vaizdo failo formatas|Nurodo JPM failo formatą ir leidžia sukurti kelių puslapių dokumentą, skirtą į faksą panašioms programoms. Palaiko JBIG2 ir JPEG naudojimą.|ISO/IEC 15444-6
|8 dalis|JPEG 2000 apsaugotas (JPSEC)|Užtikrina operacijų, turinio ir technologijų saugumą ir leidžia saugius JPEG 2000 bitų srautus.|ISO/IEC 15444-8
|9 dalis|JPIP|Apibrėžia įrankius tinklinėje aplinkoje, leidžiančius pasiekti metaduomenis ir vaizdus, ir nurodo interaktyvius ir efektyvius protokolus|ISO/IEC 15444-9
|10 dalis|JP3D|1 dalies tūrinis išplėtimas ir įvedamas Z matmuo. Išplečiama išklotinių, kodų blokų, apylinkių ir 3D dominančio regiono pasiekiamumo funkcijų koncepcija.|ISO/IEC 15444-10
|11 dalis|JPWL|Svarbi gerai organizuotą perdavimą belaidžiu tinklu, kuriame yra klaidų. Šis plėtinys suderinamas su dekoderiais | ISO/IEC 15444-11
|13 dalis | Pradinio lygio kodavimo įrenginys | Apibrėžiamas pagrindinės kodavimo sistemos pradinio lygio kodavimo įrenginys.|ISO/IEC 15444-13
|14 dalis|JPXML|Atvaizdavimas XML formatu ir paaiškinami žymeklio segmentai bei metodai, kaip pasiekti vidinius vaizdų duomenis.|ISO/IEC 15444-14
|15 dalis|HTJ2K (neparengiamas)|Nurodomas alternatyvus bloko kodavimo algoritmas. Algoritmas siūlo dešimt kartų didesnį pralaidumą ir be nuostolių kodavimą / dekodavimą.|

## JP2 failo formatas ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Nors vaizdo pavyzdžiai yra išskirtinai aprašyti JPEG 2000, tačiau JPEG-1 apima kitą papildomą informaciją apie spalvų erdvę ir skiriamąją gebą, kuri yra būtina norint užkoduoti vaizdą. Jei vaizdas saugomas kaip JPEG 2000 failas, **.jp2** naudojamas kaip plėtinys. Šis failo formatas dar labiau patobulintas JPEG 2000 part-2 plėtiniu, kuris apibrėžia animacijos mechanizmus ir daugelio kodų srautų konfigūraciją viename paveikslėlyje. **.jpx** plėtinys naudojamas, kai vaizdai išsaugomi naudojant šį išplėstinį failo formatą. Kadangi kodo srauto duomenys nėra laikomi pirmiausia išsaugotais failuose, todėl šiam tikslui nėra apibrėžtas joks standartinis plėtinys. Nors bandymo tikslais, jis dažnai gauna plėtinį **.jpc** arba **.j2k**. Priešingai nei JPEG-1, JPEG 2000 pasirenka kitokį metaduomenų kodavimo XML formatu būdą. Standartas 12234-1.4 (ISO TC42 komiteto) naudojamas kaip nuoroda tarp Exif žymų ir XML komponentų. JPEG 2000 gali turėti ISO standartą, XMP viduje.

### gabaliukai ###
JPEG 2000 failus sudaro nuoseklūs gabalai. Kiekvienas gabalas turi 8 baitų antraštę: 4 baitų gabalo dydis (didelis baitas, pirmiausia aukštas baitas) ir 4 baitų gabalo tipas – vienas iš iš anksto nustatytų parašų: jP arba jP2.

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000 apibrėžiamas potipiu, kuris turi būti viena iš reikšmių: jp2 (failo tipas \*.JP2), jp20 (failo tipas \*.JPA), jpm (failo tipas \*.JPM), jpx (failo tipas \*.JPX).

Kartodami gabalus, kol neaptinkamas nežinomas tipas, sudarome JPEG 2000 vaizdo / vaizdo failą.

### Spalvų transformacija ###

Iš pradžių reikalingas vaizdų transformavimas iš RGB spalvų erdvės į kitą spalvų erdvę. Šiuo tikslu yra du būdai: negrįžtama spalvų transformacija (ICT) ir grįžtama spalvų transformacija (RCT). Pirmoji naudoja YC,,B,,C,,R,, spalvų erdvę ir turi būti įdiegta fiksuotame / slankiajame taške, o vėliau modifikuota YUV spalvų erdvė ir grįžtama iš prigimties.// //Neapsiribojama RGB modeliu, JPEG 2000 kalba naudoja kelių komponentų transformaciją.

### Plytelių klijavimas ###

Kai spalva transformuojama, vaizdas paverčiamas stačiakampiais regionais, vadinamais plytelėmis, kurias galima transformuoti ir užkoduoti atskirai. Visų plytelių dydis bus vienodas arba visas vaizdas gali būti laikomas viena plytele. Dekoderis naudojasi plytelių klojimo pranašumais ir sunaudoja mažiau atminties arba gali iš dalies užkoduoti kai kurias plyteles. Nors šios technikos trūkumas yra vaizdo kokybės pablogėjimas.

### Wavelet transformacija ###

Vaizdas po plytelių klojimo yra bangele transformuojamas, kuris gali būti negrįžtamas arba grįžtamasis ir įgyvendinamas naudojant konvoliucijos arba kėlimo schemą.

### Suspaudimo laipsnis ###

Priklausomai nuo fizinių vaizdo ypatybių, gaunamas 20 % suspaudimo padidėjimas. JPEG 2000 erdvinio pertekliaus numatymas vaidina gyvybiškai svarbų vaidmenį glaudinimo procese, o didelės raiškos vaizdai dažniausiai įgyja didžiausią pranašumą.

## Programos, kurias aptarnauja standartinis ##

* Įrašyti, redaguoti ir saugoti HD vaizdo įrašus su rėmeliais

* Medicininiai vaizdai ir biometriniai duomenys

* palydoviniai vaizdai, nuotolinis stebėjimas ir judesio aptikimas

* Kliento/serverio ryšys, tinklo paskirstymas ir saugojimas.

* Skaitmeninis kinas, tiesioginis HDTV srautas, skaitmeninė garso ir vaizdo medžiaga


## Nuorodos Nr.

* [JPEG 2000 apžvalga](https://jpeg.org/jpeg2000/)

* [JPEG 2000 vaizdų kodavimo sistema](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


