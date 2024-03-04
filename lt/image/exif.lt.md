{
  "date": "2019-10-11",
  "keywords": [
"exif failą",
"exif failo formatas",
"kas yra exif failas",
"failą",
"exif pavyzdys",
"exif failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "Sužinokite apie EXIF failo formatą ir API, kurios gali kurti ir atidaryti EXIF failus.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra EXIF failas?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. Nuo šiandien standartą valdo Japonijos elektronikos ir informacinių technologijų pramonės asociacija (JEITA). EXIF yra vaizdo ir garso formatų, daugiausia naudojamų skaitmeniniuose fotoaparatuose ir skaitytuvuose, specifikacijų standartas.

EXIF standartas apima žymėjimo ir metaduomenų informaciją su vaizdo failu. Metaduomenyse gali būti tokios informacijos kaip fotoaparato modelis, užrakto greitis, data ir laikas, diafragma, gamintojas, ekspozicijos laikas, X raiška, Y skiriamoji geba ir tt Paprastai EXIF duomenys yra paslėpti pagal numatytuosius nustatymus. Norint peržiūrėti EXIF duomenis, vaizdų peržiūros programoje reikia pasirinkti peržiūros ypatybes. Exif metaduomenyse taip pat gali būti miniatiūros kartu su techniniais ir pirminiais vaizdo duomenimis viename vaizdo faile.

## Istorija ir versijos ##

* 1995 m. spalio mėn. JEIDA sukūrė 1 versiją. Šioje versijoje JEIDA apibrėžė struktūrą, kurią sudaro vaizdo duomenų formatas ir atributų informacija bei pagrindinės žymės.

* 1997 m. lapkričio mėn. 1.1 versija buvo pristatyta su dauguma 1 versijos žymų, tačiau taip pat buvo pridėtos nuostatos dėl pasirenkamos atributo informacijos ir formato veikimo.

* 1998 m. birželio mėn., 2 versija su sRGB spalvų erdve, suglaudintomis miniatiūromis ir garso failais.

* 1998 m. gruodžio mėn. 2.1 versija su patobulinta saugykla ir atributų informacija.

* 2002 m. vasario mėn., 2.2 versija, patobulinta versija 2.1 su spausdinimo apdaila.

* 2003 m. rugsėjo mėn. 2.21 versija su pasirenkama spalvų erdve, žinoma kaip „Adobe RGB“.


## EXIF failo formatas

EXIF naudoja šiuos failų formatus, pridėdamas specifinių metaduomenų.

1. [JPEG](/image/jpeg/) – diskretinė kosinuso transformacija (DCT), skirta suspaustiems vaizdo failams.
1. [TIFF](/image/tiff/) 6.0 redakcija (RGB arba YCbCr), skirta nesuspaustiems vaizdo failams.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) garso failams (Linear [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) arba ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM nesuspaustiems garso duomenims, ir [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) suspaustiems garso duomenims).

### EXIF naudojamas žymeklis ###

Žymeklis 0xFFE0~~0xFFEF yra Application Marker, naudojamas vartotojo programoje. Pavyzdžiui, senesnėse skaitmeninėse kamerose vaizdams saugoti naudojamas JFIF (JPEG failų mainų formatas). JFIF naudoja APP0 (0xFFE0) žymeklį, kad įterptų skaitmeninės kameros konfigūracijos duomenis ir miniatiūrą. Be to, EXIF taip pat naudoja programos žymeklį duomenims įterpti, tačiau EXIF naudoja APP1 (0xFFE1) žymeklį, kad išvengtų konflikto su JFIF formatu. Kiekvienas EXIF failo formatas prasideda nuo šio formato.


|SOI žymeklis|APP1 žymeklis|APP1 duomenys|Kitas žymeklis
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Jis prasideda nuo SOI (0xFFD8) žymeklio, todėl tai yra JPEG failas. Tada iškart seka APP1 žymeklis. Visi EXIF duomenys saugomi šioje APP1 duomenų srityje. Viršutinėje lentelėje esanti SSSS dalis reiškia APP1 duomenų srities (EXIF duomenų srities) dydį. Atkreipkite dėmesį, kad dydis SSSS taip pat apima paties deskriptoriaus dydį. Po SSSS paleidžiami APP1 duomenys. Pirmoji dalis yra specialūs duomenys, skirti identifikuoti, ar naudojamas EXIF, ar ne, ASCII simbolis EXIF ir 2 baitai 0x00. Po APP1 žymeklio srities seka kiti JPEG žymekliai.

### Exif duomenų struktūra ###

Žemiau parodyta apytikslė EXIF duomenų struktūra (APP1). Kaip aptarta aukščiau, EXIF duomenys prasideda nuo ASCII simbolio EXIF ir 2 baitų 0x00, tada eina EXIF duomenys. EXIF naudoja TIFF formatą duomenims saugoti.


|FFE1|APP1 žymeklis
---|---|
|SSSS|APP1 duomenys|APP1 duomenų dydis
|45786966 0000|Exif antraštė
|49492A00 08000000|TIFF antraštė
|XXXX. . . .|IFD0 (pagrindinis vaizdas)|Katalogas
|LLLLLLLL|Nuoroda į IFD1
|XXXX. . . .|IFD0 duomenų sritis
|XXXX. . . .|Exif SubIFD|Katalogas
|00000000|Nuorodos pabaiga
|XXXX. . . .|Exif SubIFD duomenų sritis
|XXXX. . . .|IFD1(miniatiūros vaizdas)|Katalogas
|00000000|Nuorodos pabaiga
|XXXX. . . .|IFD1 duomenų sritis
|FFD8XXXX. . . XXXXFFD9|Miniatūros vaizdas

#### TIFF antraštė ####

8 baitų [TIFF](/image/tiff/) failo antraštėje yra ši informacija:

0-1 baitai: faile naudojama baitų tvarka. Teisinės reikšmės yra: II(4949.H)MM (4D4D.H).

II formatu baitų tvarka visada yra nuo mažiausiai reikšmingo baito iki reikšmingiausio baito, tiek 16 bitų, tiek 32 bitų sveikiesiems skaičiams. Tai vadinama mažojo galo baitų tvarka. MM formatu baitų tvarka visada yra nuo reikšmingiausios iki mažiausiai reikšmingos tiek 16 bitų, tiek 32 bitų sveikiesiems skaičiams. Tai vadinama didžiąja baitų tvarka.

2–3 baitai: savavališkas, bet kruopščiai parinktas skaičius (42), kuris toliau identifikuoja failą kaip TIFF failą. Baitų tvarka priklauso nuo 0–1 baitų reikšmės.

4–7 baitai: pirmojo IFD poslinkis (baitais). Katalogas gali būti bet kurioje failo vietoje po antraštės, bet turi prasidėti nuo žodžio ribos. Visų pirma, vaizdų failų katalogas gali sekti jame aprašomus vaizdo duomenis. Skaitytojai turi sekti nuorodas, kad ir kur jie nuvestų. Terminas baitų poslinkis šiame dokumente visada vartojamas norint nurodyti vietą TIFF failo pradžios atžvilgiu. Pirmojo failo baito poslinkis yra 0.

#### Vaizdo failų katalogas ####

IFD yra informacijos apie vaizdą ir nuorodų į faktinius vaizdo duomenis. Jį sudaro 2 baitų skaičius katalogo įrašų (ty laukų skaičius), po kurio seka 12 baitų lauko įrašų seka. , po kurio seka kito IFD 4 baitų poslinkis (arba 0, jei jo nėra). TIFF faile turi būti bent 1 IFD ir kiekvienas IFD turi turėti bent vieną įrašą.

##### IFD įrašas #####

Kiekvienas 12 baitų IFD įrašas yra tokio formato.


|Baitai|Aprašymas
---|---|
|0-1|Žyma, identifikuojanti lauką
|2-3|Lauko tipas
|4-7|Nurodyto tipo skaičius
|8-11|Vertės poslinkis, lauko reikšmės failo poslinkis (baitais). Tikimasi, kad reikšmė prasidės nuo žodžio ribos; Taigi atitinkamas vertės poslinkis bus lyginis skaičius. Šis failo poslinkis gali būti nukreiptas bet kurioje failo vietoje, net po vaizdo duomenų

TIFF laukas yra loginis objektas, susidedantis iš TIFF žymos ir jos reikšmės. Ši loginė koncepcija įgyvendinama kaip IFD įrašas, pridėjus faktinę vertę, jei ji netelpa į vertės / poslinkio dalį, paskutinius 4 IFD įrašo baitus. Sąvokos TIFF laukas ir IFD įrašas daugeliu atvejų yra keičiami.

#### Miniatiūros vaizdas ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Yra 3 formatai miniatiūroms; JPEG formatas (JPEG naudoja YCbCr), RGB TIFF formatas, YCbCr TIFF formatas.

##### JPEG formato miniatiūra #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Atrodo, kad JPEG formatas ir 160 x 120 pikselių dydis yra rekomenduojamas Exif2.1 ar naujesnės versijos miniatiūros formatas.

##### TIFF formato miniatiūra #####

Jei IFD1 žymos Compression(0x0103) reikšmė yra 1, miniatiūros vaizdo formatas nėra suglaudintas (vadinamas TIFF vaizdu). Miniatiūros duomenų pradžios taškas yra StripOffset(0x0111) žyma, miniatiūros dydis yra StripByteCounts(0x0117) žymos suma.

## Nuorodos Nr.

* [EXIF – Vikipedija](https://en.wikipedia.org/wiki/Exif)

* [EXIF failo formatas](https://www.media.mit.edu/pia/Research/deepview/exif.html)


