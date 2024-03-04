{
  "date": "2019-10-11",
  "keywords": [
"png failą",
"png failo formatas",
"kas yra png failas",
"failą",
"png pavyzdys",
"png failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PNG failo formatas – rastrinio vaizdo failas",
  "description": "Sužinokite apie PNG failo formatą ir API, kurios gali kurti ir atidaryti PNG failus.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PNG failas?

**PNG** (Portable Network Graphics) failas yra rastrinio vaizdo failo formatas, kuriame naudojamas be nuostolių glaudinimas. Šis failo formatas buvo sukurtas kaip grafinio mainų formato ([GIF](/image/gif/)) pakaitalas ir neturi jokių autorių teisių apribojimų. Tačiau PNG failo formatas nepalaiko animacijų. PNG failo formatas palaiko be nuostolių glaudinimą, todėl jis populiarus tarp vartotojų. Laikui bėgant, PNG tapo vienu iš plačiai naudojamų vaizdo failų formatų.

## Trumpa PNG failo formato istorija

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Pagrindiniai įvykiai, susiję su PNG failų formatais, išvardyti toliau:

* 1996 m. spalis: buvo išleista PNG specifikacijų 1.0 versija, kuri vėliau pasirodė kaip [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. 1996 m. spalį tai tapo W3C rekomendacija.

* 1998 m. gruodžio mėn.: buvo išleista 1.1 versija su nedideliais pakeitimais ir trimis naujais gabalais.

* 1999 m. rugpjūčio mėn.: buvo išleista 1.2 versija, pridėjus vieną papildomą gabalėlį.

* 2003 m. lapkritis: PNG tapo tarptautiniu standartu (ISO/IEC 15948:2003). Ši PNG versija tik šiek tiek skiriasi nuo 1.2 versijos ir neprideda jokių naujų dalių.

* 2004 m. kovo mėn.: ISO/IEC 15948:2004


## Funkcinis GIF ir PNG palyginimas

PNG failo formatas buvo sukurtas taip, kad būtų paprastas ir nešiojamas, teisiškai neapkrautas, keičiamas, lankstus ir tvirtas. Toliau pateiktoje lentelėje išvardytos GIF funkcijos, kurios be naujų funkcijų yra paveldėtos PNG failo formatu.

|Funkcija|GIF|PNG|
---|---|---|
|Iki 256 spalvų rodyklės spalvos vaizdai|Taip|Taip|
|Srautinio perdavimo palaikymas|Taip|Taip|
|Skaidrumas|Taip|Taip|
|Papildoma informacija|Taip|Taip|
|Aparatinės įrangos ir platformos nepriklausomumas|Taip|Taip|
|Veiksmingas|Taip|Taip|
|Truecolor vaizdai iki 48 bitų viename pikselyje|Ne|Taip|
|Pilkos spalvos vaizdai iki 16 bitų pikselyje|Ne|Taip|
|Visas alfa kanalas (bendrosios skaidrumo kaukės)|Ne|Taip|
|Vaizdo gama informacija|Ne|Taip|
|Patikimumas|Ne|Taip|
|Greitesnis pradinis pristatymas|Ne|Taip|

## PNG failo struktūra

Beveik visos operacinės sistemos palaiko PNG failų atidarymą. Pavyzdžiui, Microsoft Windows Viewer turi galimybę atidaryti PNG failus, nes OS pagal numatytuosius nustatymus palaiko diegimo dalį. PNG failą sudaro PNG parašas, po kurio seka //chunks// serija.

### PNG failo antraštė

Pirmuose aštuoniuose PNG failo baituose visada yra šios (dešimtainės) reikšmės:

{{{137 80 78 71 13 10 26 10 }}}

Šis parašas rodo, kad likusioje failo dalyje yra vienas PNG vaizdas, susidedantis iš dalių serijos, prasidedančios IHDR dalimi ir baigiant IEND dalimi.

### gabaliukai ###

Kiekviena dalis susideda iš keturių dalių:

**Ilgis:** 4 baitų sveikasis skaičius be ženklų, nurodantis baitų skaičių gabalo duomenų lauke. Ilgis skaičiuoja tik duomenų lauką, o ne save, gabalo tipo kodą ar CRC. Nulis yra tinkamas ilgis. Nors koduotuvai ir dekoderiai turėtų laikyti ilgį be ženklo, jo reikšmė neturi viršyti 231 baito.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Chunk Data:** duomenų baitai, atitinkantys gabalo tipą, jei yra. Šio lauko ilgis gali būti nulinis.

**CRC:** 4 baitų CRC (Cyclic Redundancy Check), apskaičiuotas pagal ankstesnius gabalo baitus, įskaitant gabalo tipo kodą ir gabalo duomenų laukus, bet neįskaitant ilgio lauko. CRC yra visada, net ir gabalams, kuriuose nėra duomenų.

Dalies duomenų ilgis gali būti bet koks baitų skaičius iki didžiausio; todėl įgyvendintojai negali manyti, kad gabalai yra sulygiuoti ant bet kokių ribų, didesnių už baitus.

Dalys gali būti rodomos bet kokia tvarka, atsižvelgiant į kiekvienam gabalo tipui taikomus apribojimus. (Vienas pastebimas apribojimas yra tas, kad IHDR turi būti rodomas pirmas, o IEND turi būti rodomas paskutinis; taigi, IEND dalis yra failo pabaigos žymeklis.) Gali būti rodomi keli to paties tipo fragmentai, tačiau tik tuo atveju, jei tai specialiai leidžiama tam tipui.

#### Gabalų tipai

Dalių tipai skirstomi į **kritinius** ir **pagalbinius** gabalus, remiantis 4 baitų didžiosioms ir mažosiomis raidėmis jautria ASCII reikšme, priskirta gabalo tipui. Visi diegimai turi suprasti ir sėkmingai pateikti standartines kritines dalis. Tinkamame PNG vaizde turi būti IHDR dalis, vienas ar daugiau IDAT dalių ir IEND dalis.

### Suspaudimas

PNG glaudinimo metodas 0 (vienintelis šiuo metu PNG apibrėžtas glaudinimo metodas) nurodo sumažinimo / padidinimo glaudinimą, kai slankusis langas yra ne didesnis kaip 32 768 baitai. Suspaudimo sumažinimas yra LZ77 darinys, naudojamas zip, gzip, pkzip ir susijusiose programose. Buvo atlikti išsamūs tyrimai, patvirtinantys jo patentų neturintį statusą. Suspausti duomenys zlib duomenų sraute saugomi kaip blokų serija, kurių kiekvienas gali atstovauti neapdorotus (nesuspaustus) duomenis, LZ77 suglaudintus duomenis, užkoduotus fiksuotais Huffman kodais, arba LZ77 suglaudintus duomenis, užkoduotus pasirinktiniais Huffmano kodais. Paskutiniame bloke esantis žymeklio bitas identifikuoja jį kaip paskutinį bloką, leidžiantį dekoderiui atpažinti suspausto duomenų srauto pabaigą.

#### Išankstinis suspaudimo filtravimas

Norint paruošti vaizdo duomenis optimaliam suspaudimui, taikomi išankstinio suspaudimo filtrai. PNG filtro metodas apibrėžia penkis pagrindinius filtrų tipus:

|Filtro tipas|Pavadinimas|Numatoma reikšmė|
---|---|---|
|0|Nėra|Skenavimo linija perduodama nepakeista|
|1|Sub|Persiunčia skirtumą tarp kiekvieno baito ir ankstesnio pikselio atitinkamo baito vertės.|
|2|Aukštyn|Filtras Aukštyn() yra kaip ir Sub() filtras, išskyrus tai, kad kaip numatytojas naudojamas pikselis, esantis tiesiai virš dabartinio pikselio, o ne tik jo kairėje.|
|3|Vidutinis|Filtras Average() naudoja dviejų gretimų pikselių (kairėje ir aukščiau) vidurkį taško vertei numatyti.|
|4|Paeth|Paeth() filtras apskaičiuoja paprastą tiesinę trijų gretimų pikselių funkciją (kairėje, viršuje, viršuje kairėje), tada kaip numatytoją pasirenka gretimą pikselį, esantį arčiausiai apskaičiuotos vertės.|

Filtravimo algoritmai taikomi baitams, o ne pikseliams, neatsižvelgiant į vaizdo bitų gylį ar spalvų tipą. Filtravimo algoritmai veikia pagal baitų seką, kurią sudaro nuskaitymo linija. Jei paveikslėlyje yra alfa kanalas, alfa duomenys filtruojami taip pat, kaip ir vaizdo duomenys.

Kai vaizdas yra persipynęs, kiekvienas persipynimo modelio eiga filtravimo tikslais traktuojamas kaip nepriklausomas vaizdas. Filtrai veikia su baitų sekomis, kurias sudaro pikseliai, iš tikrųjų perduodami praėjimo metu, o ankstesnė nuskaitymo linija yra ta, kuri buvo perduota anksčiau tuo pačiu praėjimu, o ne ta, kuri yra greta visame vaizde. Atkreipkite dėmesį, kad per vieną kartą perduodamas vaizdas visada yra stačiakampio formos, bet mažesnio pločio ir (arba) aukščio nei visas vaizdas. Kai šis antrinis vaizdas tuščias, filtravimas netaikomas.

## Nuorodos Nr.

* [PNG – pagrindinis puslapis](http://www.libpng.org/pub/png/)


