{
  "date": "2021-02-25",
  "keywords": [
"ttc failą",
"ttc failo formatas",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC – „TrueType“ rinkinio failo formatas",
  "description": "„TrueType Collection“ (TTC) failas sujungia kelis šriftus į vieną failą. „Apple“ ir „Microsoft“ naudojo TTF „Mac“ ir „Windows“ operacinėse sistemose.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-ltc"
}
},
  "lastmod": "2021-02-25"
}

## Kas yra TTC failas?
TTC yra sutrumpintas kaip TrueType kolekcija yra True Type formato plėtinys. TTC failas gali sujungti kelis šrifto failus į jį. Šie failai naudingi derinant kelis šriftus, turinčius daug bendrų glifų. Iki Windows 2000 TTC failai buvo naudojami kinų, japonų ir korėjiečių kalbose Windows versijose, tačiau vėliau palaikymas buvo prieinamas visuose regionuose.


## Šriftų rinkinio failo struktūra 
TTC failą sudaro TTC antraštės lentelė, lentelių katalogai ir kelios OpenType lentelės. TTC antraštę reikia rasti failo pradžioje. Kiekvienam šriftui turi būti sudarytas visas lentelės katalogas. TableDirectory formatas turėtų būti panašus į nerinkimo failo formatą. Lentelės skaičiai visuose TTC failo kataloguose skaičiuojami nuo TTC failo pradžios.
TTC failo lentelės pateikiamos atitinkamų šriftų lentelių kataloge. Keletas OpenType lentelių turi būti rodomos kelis kartus, vieną kartą kiekvienam šriftui, įtrauktam į TTC. Tuo tarpu kitos lentelės gali būti bendrinamos keliais šriftais TTC faile.

### TTC antraštė
Iki šiol galimos dvi TTC antraštės lentelės versijos:
- 1.0 versija naudojama TTC failams be skaitmeninių parašų.
- 2.0 versija gali būti naudojama TTC failams su skaitmeniniu parašu arba be jo.
Čia yra abiejų versijų TTC antraštės lentelės:

**TTC antraštės 1.0 versija:**

|Tipas|Vardas|Aprašymas|
---|---|---|
|TAG|ttcTag|Šriftų rinkinio ID eilutė: 'ttcf' (naudojama šriftams su CFF arba CFF2 kontūrais, taip pat TrueType kontūrais)|
|uint16|majorVersion|Pagrindinė TTC antraštės versija, = 1.|
|uint16|minorVersion|Mažoji TTC antraštės versija, = 0.|
|uint32|numFonts|Šriftų skaičius TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Kiekvieno šrifto poslinkių į TableDirectory masyvas nuo failo pradžios|

**TTC antraštės 2.0 versija:**

|Tipas|Vardas|Aprašymas|
---|---|---|
|TAG|ttcTag |Šriftų rinkinio ID eilutė: 'ttcf'|
|uint16| majorVersion |Pagrindinė TTC antraštės versija, = 2.|
|uint16| minorVersion |Mažoji TTC antraštės versija, = 0.|
|uint32| numFonts |Šriftų skaičius TTC|
|Poslinkis32| tableDirectoryOffsets[numFonts] |Kiekvieno šrifto TableDirectory poslinkių masyvas nuo failo pradžios|
|uint32| dsigTag |Žyma, nurodanti, kad yra DSIG lentelė, 0x44534947 ('DSIG') (nuulis, jei nėra parašo)|
|uint32| dsigLength |DSIG lentelės ilgis (baitais) (nulis, jei nėra parašo)|
|uint32| dsigOffset |DSIG lentelės poslinkis (baitais) nuo TTC failo pradžios (nulis, jei nėra parašo)|

## Nuorodos
 * [OpenType šrifto failas](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

