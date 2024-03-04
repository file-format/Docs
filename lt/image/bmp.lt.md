{
  "date": "2019-10-11",
  "keywords": [
"bmp failą",
"bmp failo formatas",
"kas yra bmp failas",
"failą",
"bmp pavyzdys",
"bmp failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP – vaizdo failo formatas",
  "description": "Sužinokite apie BMP failo formatą ir API, kurios gali kurti ir atidaryti BMP failus.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-ltp"
}
},
  "lastmod": "2019-09-10"
}

# Kas yra BMP failas? #

Failai, kurių plėtinys yra .BMP, yra taškinio vaizdo failai, naudojami taškinių skaitmeninių vaizdų saugojimui. Šie vaizdai nepriklauso nuo grafikos adapterio ir taip pat vadinami nepriklausomu bitmap (DIB) failo formatu. Ši nepriklausomybė skirta atidaryti failą keliose platformose, pvz., Microsoft Windows ir Mac. BMP failo formatas gali saugoti duomenis kaip dvimačius skaitmeninius vaizdus tiek nespalvotu, tiek spalvotu formatu su įvairiu spalvų gyliu.

## BMP failo formato specifikacijos ##

Įrenginio nepriklausomi taškiniai paveikslėliai veikia kaip pagalbinė priemonė keistis taškais tarp įrenginių ir programų. Dėl nuolatinio šio failo formato evoliucijos antraštėse esanti informacija gali skirtis priklausomai nuo Bitmap versijos. Vieną bitmap failą sudaro fiksuotos ir kintamo dydžio struktūros tam tikra seka.

Bitmap failo struktūros yra išdėstytos tokia tvarka:


|Struktūra|Neprivaloma|Dydis|Paskirtis
---|---|---|---|
|Failo antraštė|Ne|14|Saugoti bendrą informaciją apie bitmap vaizdo failą
|DIB antraštė|Ne|Fiksuoto dydžio|Saugoti išsamią informaciją apie bitmap vaizdą ir apibrėžti pikselių formatą
|Papildomų bitų kaukės|Taip|12 arba 16 baitų|Norėdami apibrėžti pikselių formatą
|Spalvų paletė|Pusiau pasirenkama|Kintamo dydžio|Norėdami apibrėžti spalvas, naudojamas bitmap vaizdo duomenims
|Atotrūkis1|Taip|Kintamo dydžio|Struktūros derinimas
|Pixel Array|No|Variable-size|Pixel formatą apibrėžia DIB antraštė arba papildomų bitų kaukės.
|Atotrūkis2|Taip|Kintamo dydžio|Struktūros derinimas
|ICC Spalvos profilis|Taip|Kintamas dydis|Norėdami apibrėžti spalvų profilį spalvų valdymui

Kai bitmap vaizdas įkeliamas į atmintį, jis tampa DIB struktūra, kurią Windows naudoja per GDI API. Failo antraštė nėra šios duomenų struktūros dalis. Spalvą taip pat gali sudaryti 16 bitų įrašai, kurie sudaro šiuo metu nurodytos paletės indeksus, o ne aiškius RGB spalvų apibrėžimus. Pažvelkime į kai kuriuos iš jų išsamiai, ypač antraštes.

### Bitmap failo antraštė ###

Bitmap failo antraštė yra panaši į kitas failo antraštes, naudojamas failui identifikuoti. Kadangi yra įvairių BMP failo formato variantų, pirmieji 2 BMP failo formato baitai yra simbolis B, o tada simbolis M ASCII koduotėje. Visos sveikųjų skaičių reikšmės saugomos mažo galo formatu.

|Poslinkis šešiakampis|Poslinkis dec|Dydis|Paskirtis
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2 struktūrinio taškinio plano masyvas * **CI** – OS/2 struktūros spalvos piktograma * **CP** – OS/2 const spalvų žymeklis * **IC** – OS/2 struktūros piktograma * **PT** – OS/2 rodyklė
|02|2|4 baitai|BMP failo dydis baitais
|06|6|2 baitai|Rezervuota; tikroji vertė priklauso nuo vaizdą kuriančios programos
|08|8|2 baitai|Rezervuota; tikroji vertė priklauso nuo vaizdą kuriančios programos
|0A|10|4 baitai|Baito poslinkis, ty pradinis adresas, kuriame galima rasti bitmap vaizdo duomenis (pikselių masyvą).

#### DIB antraštė (bitmap informacijos antraštė) ####

Išsami informacija apie vaizdą pateikiama šioje antraštėje. Remiantis šia informacija, bus nustatyta programa, kuri bus naudojama vaizdui rodyti ekrane. Visose tokiose antraštėse yra DWORD (32 bitų) laukas, nurodantis jų dydį, kad programa galėtų lengvai nustatyti vaizde naudojamą antraštę. Iš esmės taip yra dėl to, kad DIB formatas buvo kelis kartus pratęstas. Toliau pateikiama DIB antraštė su išvardytais laukais.

#### Spalvų paletė ####

BMP spalvų paletė yra masyvas struktūrų, kurios nurodo kiekvienos spalvos RGB intensyvumo reikšmes ekrano įrenginio spalvų paletėje. Kiekvienas bitmap duomenų pikselis saugo vieną reikšmę, naudojamą kaip indeksą spalvų paletėje. Spalvos informacija, saugoma elemente prie to indekso, nurodo to pikselio spalvą. Spalvų prieinamumas taškinio žemėlapio faile skiriasi taip:

* Vieno, 4 ir 8 bitų – tikimasi, kad visada bus spalvų paletė

* Šešiolika, 24 ir 32 bitų – niekada neturi spalvų palečių

* Šešiolika ir 32 bitų BMP failai – vietoje spalvų paletės yra bitų laukų kaukės reikšmės


#### Pixel Storage ####

Bitmap pikseliai saugomi kaip bitai, supakuoti į eilutes, kurių kiekvienos eilutės dydis suapvalinamas iki 4 baitų kartotinio (32 bitų DWORD) užpildant. Bendras baitų kiekis, reikalingas vaizdo pikseliams saugoti, negali būti tiesiogiai apskaičiuotas skaičiuojant bitus. Kadangi reikalingas užpildymas, reikia suapvalinti kiekvienos eilutės dydį iki 4 baitų kartotinio. Papildymo baitai (nebūtinai 0) turi būti pridėti prie eilučių pabaigos, kad eilučių ilgis būtų keturių baitų kartotinis. Kai pikselių masyvas įkeliamas į atmintį, kiekviena eilutė turi prasidėti atminties adresu, kuris yra 4 kartotinis.

Vaizdas iš tikrųjų apibūdinamas 32 bitų DWORD pikselių masyvo atvaizdu. Paprastai pikseliai saugomi iš apačios į viršų, pradedant apatiniame kairiajame kampe, einant iš kairės į dešinę, o tada eilė po eilutės iš vaizdo apačios į viršų. Toliau pateikiami pikselių formatai ir jų reikšmė:

* 1 bito pikselyje (1 bpp) formatas palaiko 2 skirtingas spalvas (pvz., juodą ir baltą).

* 2 bitų pikselyje (2 bpp) formatas palaiko 4 skirtingas spalvas ir išsaugo 4 pikselius 1 baite, o kairysis pikselis yra dviejuose svarbiausiuose bituose. Kiekviena pikselio reikšmė yra 2 bitų indeksas į lentelę, kurioje yra iki 4 spalvų.

* 4 bitų viename taške (4 bpp) formatas palaiko 16 skirtingų spalvų ir išsaugo 2 pikselius 1 baite, o kairysis pikselis yra reikšmingesniame įbrėžime. Kiekviena pikselio reikšmė yra 4 bitų indeksas į lentelę, kurioje yra iki 16 spalvų.

* 8 bitų vienam pikseliui (8 bpp) formatas palaiko 256 skirtingas spalvas ir išsaugo 1 pikselį 1 baite. Kiekvienas baitas yra indeksas į lentelę, kurioje yra iki 256 spalvų.

* 16 bitų vienam pikseliui (16 bpp) formatas palaiko 65536 skirtingas spalvas ir išsaugo 1 pikselį 2 baitų WORD. Kiekvienas WORD gali apibrėžti alfa, raudoną, žalią ir mėlyną pikselio pavyzdžius.

* 24 bitų pikselių (24 bpp) formatas palaiko 16 777 216 skirtingų spalvų ir išsaugo 1 pikselio reikšmę 3 baituose. Kiekviena pikselio reikšmė apibrėžia raudoną, žalią ir mėlyną pikselio pavyzdžius (8.8.8.0.0 RGBAX žymėjime). Tiksliau, tokia tvarka: mėlyna, žalia ir raudona (8 bitai kiekvienam pavyzdžiui).

* 32 bitų vienam pikseliui (32 bpp) formatas palaiko 4 294 967 296 skirtingas spalvas ir išsaugo 1 pikselį 4 baitų DWORD. Kiekvienas DWORD gali apibrėžti alfa, raudoną, žalią ir mėlyną pikselio pavyzdžius.


## Nuorodos Nr.

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP failo formatas](https://en.wikipedia.org/wiki/BMP_file_format)


