{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"failą",
"pratęsimas",
"Dokumento formatas",
"Excel dvejetainės skaičiuoklės failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra XLSB failas ir API, kurios gali juos sukurti ir atidaryti.",
  "title": "Kas yra XLSB failas?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-ltb"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra XLSB failas?

XLSB failo formatas nurodo Excel dvejetainio failo formatą, kuris yra įrašų ir struktūrų rinkinys, nurodantis Excel darbaknygės turinį. Turinys gali apimti nestruktūrizuotas arba pusiau struktūrizuotas skaičių lenteles, tekstą arba skaičių ir tekstą, formules, išorinius duomenų ryšius, diagramas ir vaizdus. Skirtingai nuo [XLSX](/spreadsheet/xlsx/) (kuris pagrįstas Open XML failo formatu), XLSB yra dvejetainis Excel darbaknygės failas. XLSB failus galima skaityti ir rašyti greičiau, todėl jie naudingi dirbant su dideliais failais. XLSB retai naudojamas darbaknygėms saugoti, nes XLSX (ir anksčiau [XLS](/spreadsheet/xls/)) yra dažniausiai naudotojų pasirenkami darbaknygių įrašymo failų formatai. Jį galima atidaryti naudojant Microsoft Office 2007 ir naujesnę versiją.

## XLSB failo formato specifikacijos ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Nuo to laiko specifikacijos buvo keletą kartų peržiūrėtos, o naujausia specifikacijų versija (v 10.0) buvo paskelbta 2018 m. balandžio mėn. Specifikacijas Microsoft pateikia viešai kaip [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) ir kiekvienas turėtų jas perskaityti arba rašyti failus XLSB failo formatu.

## XLSB failo struktūra ##

XLSB failas yra paketas, kurį sudaro dalių rinkinys. Šiose dalyse yra informacija apie darbaknygės turinį, įskaitant darbaknygės duomenis ir paketo struktūrą. Kai kuriose dalyse yra informacija, saugoma naudojant dvejetainius įrašus, kai kuriose yra XML, o kitose yra informacija, saugoma kaip dvejetainis baitų srautas. Kiekviename dvejetainiame įraše yra nulis arba daugiau struktūrinių laukų, kuriuose yra darbaknygės duomenys.

#### Paketas ####

XLSB paketas yra [ZIP](/compression/zip/) archyvas, kuriame turi būti tiksliai viena darbaknygės dalis. Ši dalis turi būti santykių tikslas šioje paketo santykių dalyje. Darbaknygės dalis yra pradinė XLSB dokumento dalis.

#### #### dalis

Dalis yra baitų srautas, turintis susietą turinio tipą, kuris nurodo dalyje saugomo turinio pobūdį ir tipą. Kai kurios dalys saugo informaciją dvejetainiu formatu, o kitos saugo informaciją kaip XML. Specifikacijų dokumento skyriuje [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) pateikiamos galiojančios dalys, turinio tipai ir būtini / pasirenkami ryšiai tarp visų paketo dalių.

#### Santykiai ####

Šaltinis ir tikslinis išteklius yra susiję ryšiu. Santykiai gali būti:

**Paketo ryšys:** kai tikslas yra dalis, o šaltinis yra paketas kaip visuma

**Ryšys tarp dalių:** kai tikslas yra dalis, o šaltinis yra paketo dalis

**Aiškus ryšys:** kai šaltinis nurodomas iš šaltinio dalies turinio, nurodant ryšio elemento ID atributo vertę

**numanomas ryšys** yra ryšys, kuris nėra aiškus

**Vidiniai santykiai:** kai taikinys yra paketo dalis

**Išorinis ryšys:** kai taikinys yra išorinis šaltinis, kurio nėra pakete

#### Įrašas ####

Įrašas yra pagrindinis kūrimo blokas, naudojamas informacijai apie funkcijas saugoti darbaknygėje. Kiekvienas dvejetainis įrašas yra kintamo ilgio baitų seka. Dvejetainis įrašas susideda iš trijų komponentų:

* įrašo tipas

* rekordinio dydžio ir

* tam įrašo tipui būdingi įrašo duomenys.


**Įrašo tipas:** Įrašo tipas rodo įrašo nurodytą įrašo tipą. Taip pat nurodoma šiam įrašui būdingų įrašo duomenų struktūra. Galiojantys įrašų tipai yra išvardyti specifikacijų dokumento [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) skyriuje. Įrašo tipas turi būti vienas arba du baitai ir turi būti didesnis arba lygus 128 ir mažesnis nei 16384.

**Įrašo dydis:** įrašo dydis nurodo baitų skaičių, kuris nurodo bendrą įrašo duomenų dydį. Ši reikšmė PRIVALO būti nuo vieno iki keturių baitų. Ši reikšmė PRIVALO būti vienas baitas, jei žemo baito aukštas bitas yra lygus 0; kitu atveju ši reikšmė TURI būti didesnė nei vienas baitas. Jei baitų skaičius yra didesnis nei vienas baitas, kiekvieno iš eilės baito aukštas bitas nurodo, ar naudojamas papildomas baitas. Jei antrojo baito aukštas bitas yra lygus 1, tada ši vertė PRIVALO naudoti papildomą trečiąjį baitą. Jei trečiojo baito aukštasis bitas yra lygus 1, tada ši vertė PRIVALO naudoti papildomą ketvirtą baitą. Ketvirtojo baito aukštasis bitas PRIVALO būti ignoruojamas. Vertė susideda iš septynių mažų kiekvieno baito bitų kartu. Maži, mažiausiai reikšmingi bitai yra pirmame baite, o kiekviename paskesniame baite yra aukštesnės eilės bitai nei ankstesniame baite.

**Įrašo duomenys:** Įrašo duomenų komponente yra laukai, atitinkantys konkretų įrašo tipą ir apimantys likusią įrašo dalį. Laukų tvarka ir struktūra tam tikram įrašo tipui, nurodytam įrašų sąraše, yra nurodyta atitinkamoje to įrašo tipo skyriuje Įrašai. Bendras įrašo duomenų komponento dydis TURI būti lygus įrašo dydžiui. Įrašo duomenų komponento laukuose gali būti paprastos reikšmės, reikšmių masyvai, kelių laukų struktūros, laukų masyvai ir struktūrų matricos.

#### XLSB įrašo pavyzdys ####

Šis įrašo tipas ir dydis nurodo **BrtCommentText** įrašą, kurio dydis yra 200 baitų:

11111101 00000100 11001000 00000001 [Įrašyti laukai]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, kuris lygus 512. Įrašo tipo reikšmė yra 125 + 512 arba 637, o tai atitinka **BrtCommentText** įrašo tipą. Kitas baitas yra 11001000, nurodant mažą 72 reikšmę ir kad įrašo dydžiui reikia antro baito. Antrasis baitas yra 00000001, nurodantis didesnę reikšmę 1 * 128 ir kad įrašo dydžiui nereikia papildomo baito. Įrašo dydis yra 72 + 128 arba 200, o tai nurodo bendrą įrašo duomenų komponento dydį baitais. Įrašo duomenų komponento laukai nurodomi **BrtCommentText**.

## Nuorodos Nr.

* [[MS-XLSB] – „Excel“ (.xlsb) dvejetainis failo formatas](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


