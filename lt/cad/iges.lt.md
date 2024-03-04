{
  "date": "2020-03-16",
  "keywords": [
"IGES failas",
"Dokumento formatas",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie IGES failo formatą ir API, kurios gali kurti ir atidaryti IGES failus.",
  "title": "IGES failo formatas",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-lts"
}
},
  "lastmod": "2020-07-28"
}

## Kas yra IGES failas?

Failas su plėtiniu .iges naudojamas keistis projektavimo informacija tarp kompiuterinio projektavimo (CAD) programų. IGES reiškia pradines grafikos mainų specifikacijas. Informacija, kuria keičiamasi naudojant IGES, apima grandinės schemą, vielos rėmą, laisvos formos paviršių arba vientiso modeliavimo vaizdus. IGES randa savo pritaikymą tradiciniams inžineriniams brėžiniams, modelių analizei ir gamybos funkcijoms. Formatas gali keistis tiek 2D, tiek 3D projektavimo informacija tarp CAD programų. IGES failus galima atidaryti su keliomis CAD programomis, tokiomis kaip Autodesk ir CADSoftTools ABViewer. Taip pat yra keletas API, leidžiančių programiškai atidaryti ir konvertuoti IGES failus.

## IGES failo formatas

IGES failai yra ASCII teksto formatu ir gali būti atidaromi bet kuriame teksto rengyklėje, kad peržiūrėtumėte failo turinį. Tekstinė informacija IGES faile pateikiama Hollerith formatu. Įprastame IGES faile gali būti tūkstančiai eilučių, atspindinčių 2D arba 3D informaciją, kuria galima keistis pagal šį formatą. IGES failas yra padalintas į penkias dalis, kurios 73 stulpelyje žymimos konkrečia didžiąja raide. Šios skiltys yra skiltys Pradėti (S), Visuotinis (G), Duomenų įvedimas (D), Parametrų duomenys (P) ir Pabaiga (T). Duomenų įvedimo ir parametrų duomenų skyriai paprastai yra atitinkamai sutrumpinti DE ir PD.

### IGES failo antraštė

Start ir Global skyriuose yra pagrindinė informacija apie:
 * Failo pavadinimas ir jo šaltinis
 * Skyriaus Parametrų duomenys skyrikliai
 * Failo autorius ir kita bendra informacija.

Pavyzdinio dokumento Vikipedijoje skyriai Pradėti ir Visuotiniai yra tokie.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Duomenų įvedimo (DE) ir parametrų duomenų (PD) skyrius

#### Duomenų įvedimo skyrius
IGES failą sudaro keli objektai, kuriuose yra informacija apie pagrindinius IGES failo formato duomenis. Objekte yra informacijos apie skirtingus IGES duomenų formato elementus ir jis naudojamas piešti. Dažniausiai naudojami objektai yra šie:
 * Apvalus lankas
 * Sudėtinė kreivė
 * Kūgio lankas
 * Lėktuvas
 * Linija

Tai tik keletas ir IGES sistemoje yra apie 150 skirtingų subjektų. Kiekvienas subjektas identifikuojamas pagal tipo numerį, pvz.:
 * Apskritimas lankas (100 tipas)
 * LINIJA (110 tipas)

##### Objekto ypatybės

Kiekvienas deklaruotas subjektas turi šias savybes.

|Lauko pavadinimas|Aprašymas|
---|---|
|Subjekto tipas |Tai aprašomojo objekto tipas. Pavyzdžiui, 116 aprašo taško objektą.|
|PD rodyklė |Tai nurodo šio objekto duomenų vietą parametrų duomenų skiltyje. Ši vieta yra tiesiog eilutės numeris PD skiltyje, kurioje yra pirmoji šio objekto duomenų eilutė.|
|Struktūra |Nulis arba žymeklis į apibrėžimo objektą. Netaikoma daugumai subjektų|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Nenurodytas raštas (numatytasis) * 1 vientisas * 2 brūkšninis * 3 fantominis * 4 vidurio linija * 5 punktyrinė|
|Lygis| Nurodo lygius, kurie turi būti susieti su šiuo objektu. Leidžia subjektui pasirodyti daugiau nei viename lygyje|
|Žiūrėti| Nurodo peržiūros parinktis. Tai yra: 0 Nurodo vienodą matomumą ir charakteristikas visuose rodiniuose. Numatytasis rodyklės rodinys (tipas 410), kurį galima peržiūrėti iš Rodinio matomo susiejimo objekto nuorodos (402 tipas, 3 forma)
|Transformacijos matricos rodyklė| Nurodo transformacijos matricos objektą (tipas 124) arba pagal numatytuosius nustatymus yra nulis (be transformacijos)|
|Etiketės rodymo asociatyvumas| Nurodo etikečių rodymo asociatyvumą (tipas 402, 5 forma), kuris apibrėžia, kaip atrodo objekto etiketė.|
|Būsenos numeris| Yra keturios dviejų skaičių dalys. 1-2: Tuščia būsena. 00 normaliam arba 01 tuščiam. 3-4: pavaldžių objektų jungiklis: yra 00 nepriklausomam, 01 fiziškai priklausomam, 02 logiškai priklausomam ir 03 abiem. 5-6: Objekto naudojimo vėliavėlė: yra 00 geometrijai, 01 anotacijai, 02 apibrėžimui, 03 kitai, 04 loginei, 05 2D parametrinei ir 06 konstrukcijos geometrijai. Galiausiai, 7-8 yra hierarchija, kur 00 reiškia visuotinį iš viršaus į apačią (naudokite šio objekto charakteristikas), 01 yra visuotinis atidėjimas (nenaudokite šio objekto savybių), o 02 yra naudoti hierarchijos ypatybę (naudokite hierarchijos objektą (tipas 406, forma). 10)nustatyti hierarchinio grupavimo charakteristikas).|
|Sekos numeris| Nurodoma D#, kur # yra šios sekcijos eilutės numeris (ne iš failo viršaus). Tai taip pat naudojama norint nurodyti šį duomenų įvedimo objektą.|
|Subjekto tipas| jis nurodomas du kartus vienam subjekto sąrašui|
|Linijos svorio numeris| Nurodo storį, kai rodomas objektas. Mažiausias yra 1, 0 yra numatytasis|
|Spalvos numeris| Nurodo objekto spalvą. Leidžiamos sveikųjų skaičių reikšmės yra: 0 Nėra spalvos (numatytasis) 1 Juoda 2 Raudona 3 Žalia 4 Mėlyna 5 Geltona 6 Rausvai 7 Žydrai 8 Balta|
|Parametras Eilučių skaičius Skaičius| Nurodo eilučių skaičių, kurį šis objektas užima parametrų duomenų skiltyje|
|Formos numeris| Nurodo šio subjekto formą arba atvaizdavimą. Pakeičia parametrų duomenų interpretavimo būdą. Numatytoji vertė yra 0|
|Rezervuotas laukas| Nenaudotas|
|Rezervuotas laukas| Nenaudotas|
|Subjekto etiketė| Programoje nurodytas identifikatorius – teisė pagrįsta|
|Indekso numeris| Objekto etiketės skaitinis kvalifikatorius. Abu kartu sudaro unikalų objekto identifikatorių|
|Sekos numeris Žr. aukščiau. |Tai bus D#+1, nes kiekvienas objektas nurodytas dviejose eilutėse.|

#### Parametrų duomenų skyrius
Po skilties Duomenų įrašai seka skyrius Parametrų duomenys. Jame pateikiami kiekvieno atitinkamo įrašo duomenys ir objekto parametrai, remiantis skyrikliais, nurodytais visuotiniame skyriuje (paprastai kableliais atskiriami parametrai ir kabliataškis sąrašo pabaigai).


## Nuorodos
 * [IGES pateikė WikiPedia](https://en.wikipedia.org/wiki/IGES)

