{
  "date": "2019-10-11",
  "keywords": [
"dicom failą",
"dicom failo formatas",
"kas yra dicom failas",
"failą",
"dicom pavyzdys",
"dicom failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM – skaitmeninio vaizdo gavimo ir ryšių failo formatas",
  "description": "Sužinokite apie DICOM failo formatą ir API, kurios gali kurti ir atidaryti DICOM failus.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-ltm"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DICOM failas?

DICOM yra skaitmeninio vaizdo gavimo ir ryšių medicinos akronimas ir yra susijęs su medicinos informatikos sritimi. DICOM naudojamas įvairių tiekėjų medicininiams vaizdo gavimo įrenginiams, pvz., spausdintuvams, serveriams, skaitytuvams ir tt, integruoti. Be to, jame yra kiekvieno paciento identifikavimo duomenys, siekiant unikalumo. DICOM failai gali būti bendrinami tarp dviejų šalių, jei jos gali priimti vaizdo duomenis DICOM formatu. DICOM komunikacijos dalis yra taikomojo lygmens protokolas ir naudoja TCP/IP ryšį tarp objektų. Žiniatinklio paslaugų palaikomos versijos yra 1.0, 1.1, 2 arba naujesnės.

## Istorija ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. Antroji versija buvo išleista 1988 m., kuri buvo populiaresnė tarp pardavėjų, tačiau netrukus buvo suprasta, kad ir antrąją versiją reikia tobulinti. 3-ioji standarto versija buvo išleista 1993 m. kaip DICOM. 3.0 vis dar yra naujausia versija, tačiau ji buvo nuolat atnaujinama nuo 1993 m.

## DICOM failo formatas ##

DICOM yra failo formato apibrėžimo ir tinklo ryšio protokolo derinys. DICOM naudoja .DCM plėtinį. .DCM yra dviejų skirtingų formatų, ty 1.x formato ir 2.x formato. DCM formatas 1.x taip pat galimas dviem versijomis: normalia ir išplėstine. DICOM žiniatinklio paslaugoms naudojami HTTP ir HTTPS protokolai.

### Failo antraštė ###

Failo antraštėje yra 128 baitų failo preambulė ir 4 baitų DICOM priešdėlis.

**Preambulė # 128 baitai**|**Prefiksas # 4 baitai D, I, C, M**

**Preambulė** naudojama norint pasiekti vaizdus ir kitus duomenis DICOM faile, užtikrinantį suderinamumą su dažniausiai naudojamais vaizdo failų formatais.

**Prefikse** yra eilutė DICM kaip didžiosios raidės.

### Duomenų rinkinys ###

Kiekviename faile turi būti vienas duomenų rinkinys, atspindintis SOP egzempliorių ir SOP klasę su susijusiu IOD. Duomenų rinkinys yra realaus pasaulio informacijos atvaizdas. Duomenų rinkinyje yra duomenų elementų, o duomenų elementuose yra to objekto atributų reikšmės. Atributų struktūra nurodyta IOD. DICOM duomenų objektas susideda iš daugybės atributų, įskaitant tokius elementus kaip pavadinimas, ID ir kt., taip pat vienas specialus atributas, kuriame yra vaizdo pikselių duomenys.

### Duomenų elementai ###

Duomenų elementą sudaro duomenų elementas Tag, vertės ilgis ir duomenų elemento vertė. Yra 5 tipų duomenų elementai, būtent 1 tipo būtini duomenų elementai, 1C tipo sąlyginiai duomenų elementai, 2 tipo būtini duomenų elementai, 2C tipo sąlyginiai duomenų elementai ir 3 tipo pasirenkami duomenų elementai. Pagrindiniai Trys duomenų elementų struktūrų tipai yra tokie.

**Duomenų elementas su aiškia VR**

|Grupės numeris|Elemento numeris|Vertės vaizdavimas|Rezervuotas|Vertės ilgis|Vertės laukas
---|---|---|---|---|---|
|2 baitai|2 baitai|2 baitai|2 baitai # 0x00, 0x00|4 baitai|vertės ilgio baitai

**Duomenų elementas su aiškia VR**

|Grupės numeris|Elemento numeris|Vertės vaizdavimas|Vertės ilgis|Vertės laukas
---|---|---|---|---|
|2 baitai|2 baitai|2 baitai|2 baitai|vertės ilgio baitai

**Duomenų elementas su numanoma VR**


|Grupės numeris|Elemento numeris|Vertės ilgis|Vertės laukas
---|---|---|---|
|2 baitai|2 baitai|4 baitai|vertės ilgio baitai

1. **Duomenų elemento žyma**: tvarkingas sveikasis skaičius, nurodantis grupės numerį ir elemento numerį
1. **Vertės vaizdavimo VR**: VR yra simbolių eilutė, nurodanti duomenų elemento VR.
1. **Vertės ilgis**: ar jis be ženklo sveikasis skaičius reiškia aiškų vertės lauko ilgį.
1. **Vertės laukas**: aprašomos duomenų elementų reikšmės.

## Perkėlimo sintaksė Nr.

Perdavimo sintaksė yra kodavimo taisyklių rinkinys, kad būtų galima vienareikšmiškai pavaizduoti abstrakčias sintakses. Perdavimo sintaksės pagalba bendraujantys subjektai derasi dėl įprastų kodavimo metodų, kuriuos palaiko.

## SOP ##

IOD ir DIMSE sąjunga apibrėžia SOP klasę. SOP klasės apibrėžime yra taisyklės ir semantika, kurios gali apriboti naudojimąsi paslaugomis DIMSE paslaugų grupėje arba IOD atributus. Paslaugų elementų pavyzdžiai yra saugoti, gauti, rasti, perkelti ir kt. Objektų pavyzdžiai yra KT vaizdai, MR vaizdai, bet taip pat apima tvarkaraščių sąrašus, spausdinimo eiles ir kt.

## Paslaugos ##

DICOM teikia įvairias paslaugas, daugiausia susijusias su duomenų perdavimu. Kiekvienas iš jų trumpai aprašytas žemiau:


**Store:** DICOM Store paslauga siunčia vaizdus ar kitus objektus į nuotraukų archyvavimo ir ryšio sistemą (PACS) arba serverį.


**Saugojimo įsipareigojimas:** Saugojimo įsipareigojimo paslauga naudojama patvirtinti, kad vaizdas buvo visam laikui išsaugotas įrenginyje bet kokio tipo laikmenoje.


**Užklausa / gavimas:** ši paslauga leidžia darbo stočiai rasti vaizdų ar kitų objektų sąrašus ir gauti juos iš PACS.


**Modalumo darbo sąrašas:** Modalumo darbo sąrašo paslauga pateikia vaizdo gavimo procedūrų, kurias suplanavo atlikti vaizdo gavimo įrenginys, sąrašą.


**Spausdinti:** Ši paslauga siunčia vaizdus į spausdintuvą.

## Prievado numeriai per IP ##

DICOM naudoja šiuos TCP ir UDP prievadus:

1. 104
1. 2761
1. 2762
1. 11112

## Nuorodos Nr.

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)


