{
  "date": "2019-10-11",
  "keywords": [
"u3d failą",
"u3d failo formatas",
"kas yra u3d failas",
"failą",
"u3d pavyzdys",
"u3d failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D – universalus 3D failo formatas",
  "description": "Sužinokite apie U3D failų formatą ir API, kurios gali atidaryti ir kurti U3D failus.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-ltd"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra U3D failas?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/) dokumentai palaiko U3D objektų įterpimą ir gali būti peržiūrimi naudojant Adobe Reader (7 ir naujesnės versijos).

U3D formatas buvo sukurtas siekiant sukurti universalų trijų dimensijų duomenų saugojimo ir keitimosi standartą. Tačiau šis formatas dažniausiai naudojamas koduojant 3D PDF, o ne kaip mainų formatą. Acrobat 3D konvertuoja palaikomą 3D failo tipą į U3D arba KLR konvertuojant į PDF.

## U3D failo formatas

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

Pirmasis U3D leidimas buvo sutelktas į pagrindinius 3D grafikos savybių, tokių kaip geometrija, spalva, tekstūros, apšvietimas, kaulai ir transformacija pagrįsta animacija, atvaizdavimą. Antrasis ir trečiasis leidimai ištaisė kai kurias klaidas pirmajame leidime, o trečioji versija buvo dažniausiai naudojamas pramonės programinės įrangos tipas. Ketvirtajame leidime pateikiami aukštesnės eilės primityvų (lenktų paviršių) apibrėžimai. [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) yra prieinami internete, kad naudotojas galėtų peržiūrėti ECMA svetainėje.

### Duomenų tipai U3D failuose

Dvejetainiame faile bus šie tipai: U8, U16, U32, U64, I16, I32, F32, F64 ir String.

 * U8: 8 bitų sveikasis skaičius be ženklo
 * U16: 16 bitų sveikasis skaičius be ženklo
 * U32: 32 bitų sveikasis skaičius be ženklo
 * U64 : 64 bitų sveikasis skaičius be ženklo
 * I16 : 16 bitų sveikasis skaičius
 * F32: vienkartinė IEEE plūdė.
 * F64: IEEE dvigubo tikslumo plūdė.
 * Eilutė: U3D failo eilutės prasideda nepasirašytu 16 bitų sveikuoju skaičiumi, kuris apibrėžia bendrą eilutės simbolių ilgį. Stygos visada apdorojamos kaip didžiosios ir mažosios raidės.

## U3D failo struktūra

U3D faile yra blokų seka. Kiekviename U3D faile yra 3 skirtingų tipų blokai.

 * Failo antraštės blokas
 * Deklaracijos blokas
 * Tęsinio blokas

Įkroviklis nustato bloko pabaigą, jei to bloko duomenys nereikalingi arba jei to bloko tipo dekoderis nepasiekiamas.

{{< figure src="../u3d.png" alt="U3D failo formatas" >}}

### Failo antraštės blokas
Failo antraštės bloke yra failo informacija, kurią naudoja įkeltas, kad nustatytų, kaip skaityti failą.

### Deklaracijos blokas

Deklaracijos blokuose yra informacija apie faile esančius objektus. Deklaracijos bloko objektai turi būti apibrėžti.

### Tęsimo blokas

Papildoma informacija apie objektus, deklaruotus Deklaracijos bloke, pateikiama tęsimo bloke. Kiekvienas tęsimo blokas turi būti susietas su deklaracijų bloku.


## Nuorodos Nr.

* [U3D failo formatas – Vikipedija](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D failo formato specifikacijos](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


