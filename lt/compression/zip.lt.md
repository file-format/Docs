{
  "date": "2019-12-09",
  "keywords": [
"zip failą",
"zip failo formatas",
"kas yra zip failas",
"failą",
"zip pavyzdys",
"zip failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIP",
  "description": "Kas yra ZIP failas ir API, kurios gali kurti ir atidaryti ZIP failus.",
  "linktitle": "ZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-ltp"
}
},
  "lastmod": "2019-12-09"
}

## Kas yra ZIP failas? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## Trumpa ZIP failo formato istorija

ZIP failo formato istorija prasidėjo nuo System Enhancement Associates (SEA) pareikšto ieškinio prieš PKWARE dėl ARC priemonės naudojimo be leidimo savo prekės ženklui ir gaminio išvaizdos bei vartotojo sąsajos autorių teisių. Prieš tai Philas Katzas perrašė SEA šaltinio kodą ir išleido PKXARC, ARC ištraukiklį ir PKARC, failų kompresorių, kaip nemokamą programinę įrangą MS-DOS sistemoms. Pralaimėjusi ieškinį, PKWARE nebegalėjo naudoti nieko, kas susiję su ARC. Čia buvo sukurtas naujas failų glaudinimas, pavadintas ZIP, kuris tapo PKZIP programos dalimi PKWARE, Inc.

Katzas išleido ZIP failo formato specifikacijas į viešą domeną, išlaikydamas nuosavybės teises į savo glaudinimo ir ištraukimo įrankį, ty PKZIP. ZIP glaudinimo sistema galėjo (ir gali) archyvuoti failus aplanke, naudodama 32 bitų ciklinio perteklinio patikrinimo ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritmą, kad suspaustų failų dydžius. Skirtingai nuo ARC, .ZIP aplankuose buvo katalogo failas, kuris atliko kriptografo kodų knygos vaidmenį, kuriame saugoma informacija, reikalinga suspaustiems failams pateikti.

## Palaikomi ZIP suspaudimo metodai

Pagal .ZIP failo formato specifikacijas palaikomi šie glaudinimo metodai.

* Laikyti – nereikalauja suspaudimo

* Susitraukti

* Sumažinimas (tai reiškia suspaudimo koeficientus nuo 1 iki 4 lygio)

* Susprogdinti

* Išleiskite

* Deflat64

* BZIP2

* LZMA (EFS)

* WavPack

* PPMd I versija, 1 versija


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## ZIP failo formato specifikacijos

ZIP failai turi galimybę saugoti kelis failus naudojant skirtingus glaudinimo būdus, tuo pat metu palaiko failo saugojimą be jokio suspaudimo. Kiekvienas failas saugomas/suglaudinamas atskirai, o tai padeda juos išskleisti arba pridėti naujų, netaikant glaudinimo ar išglaudinimo visam archyvui.

### Bendras ZIP failo formatas

Kiekvienas ZIP failas yra struktūrizuotas taip:


|ZIP failo formatas
---|
|1 vietinė failo antraštė
|Failo duomenys 1
|1 duomenų aprašas
|Vietinė failo antraštė 2
|Failo duomenys 2
|2 duomenų aprašas
| ....
| ....
|Vietinė failo antraštė N
|Failo duomenys N
|Duomenų aprašas N
|Archyvo iššifravimo antraštė
|Archyvuokite papildomų duomenų įrašą
|Centrinis katalogas

Archyvavimo tikslais ZIP failo formatas naudoja 32 bitų CRC algoritmą. Kad būtų pateikti suspausti failai, ZIP archyvo gale yra katalogas, kuriame saugomi esantys failai ir jų vieta archyvo faile. Taigi jis atlieka kodavimo vaidmenį, kad būtų galima įterpti informaciją, reikalingą suspaustiems failams pateikti. ZIP skaitytuvai naudoja katalogą, kad įkeltų failų sąrašą, neskaitydami viso ZIP archyvo. Formatas išsaugo dvigubas katalogo struktūros kopijas, kad būtų užtikrinta didesnė apsauga nuo duomenų praradimo.

Kiekvienas ZIP archyvo failas vaizduojamas kaip atskiras įrašas, kuriame kiekvieną įrašą sudaro vietinio failo antraštė ir suspausti failo duomenys. Archyvo pabaigoje esančiame kataloge yra nuorodos į visus šiuos failų įrašus. ZIP failų skaitytuvai turėtų vengti skaityti vietinių failų antraštes, o visų rūšių failų sąrašas turėtų būti skaitomas iš katalogo. Šis katalogas yra vienintelis tinkamų failų įrašų šaltinis archyve, nes failus galima pridėti ir archyvo pabaigoje. Štai kodėl, jei skaitytojas nuo pat pradžių skaito vietines ZIP archyvo antraštes, jis gali perskaityti neteisingus (ištrintus) įrašus, taip pat tuos, kurie nėra iš archyvo ištrinamo katalogo dalis.

Failų įrašų tvarka centriniame kataloge neturi sutapti su failų įrašų tvarka archyve.

### ZIP failo įrašai

Įrašai ZIP faile yra išdėstyti vienas po kito, kur kiekvieną įrašą sudaro:

* Vietinė failo antraštė

* Neprivalomi papildomi duomenų laukai

* Vartotojo duomenys (pasirinktinai suspausti / pasirinktinai užšifruoti)


Kiekvieno įrašo vietinio failo antraštėje pateikiama informacija apie failą, pvz., komentaras, failo dydis ir failo pavadinimas. Papildomuose duomenų laukuose (pasirinktinai) gali būti informacijos apie ZIP formato išplėtimo parinktis.

#### Vietinė failo antraštė

Vietos failo antraštė turi specifinę lauko struktūrą, kurią sudaro kelių baitų reikšmės. Visos reikšmės saugomos mažo galo baitų tvarka, kur lauko ilgis skaičiuoja ilgį baitais. Visose ZIP failo struktūrose kiekvienam failo įrašui naudojami 4 baitų parašai. Centrinio katalogo parašo pabaiga yra 0x06054b50 ir gali būti atskirta naudojant savo unikalų parašą. Toliau pateikiama vietos failo antraštėje saugomos informacijos tvarka.


|Poslinkis|Baitai|Aprašymas
---|---|---|
|0|4|Vietinio failo antraštės parašas # 0x04034b50 (skaitomas kaip nedidelis skaičius)
|4|2|Ištraukti reikalinga versija (minimali)
|6|2|Bendrosios paskirties bitų vėliavėlė
|8|2|Suspaudimo metodas
|10|2|Paskutinės failo modifikacijos laikas
|12|2|Paskutinės pakeitimo data
|14|4|CRC-32
|18|4|Suspaustas dydis
|22|4|Nesuspaustas dydis
|26|2|Failo pavadinimo ilgis (n)
|28|2|Papildomas lauko ilgis (m)
|30|n|Failo pavadinimas
|30+n|m|Papildomas laukas

#### Centrinio katalogo failo antraštė


|Poslinkis|Baitai|Aprašymas
---|---|---|
|0|4|Centrinio katalogo failo antraštės parašas # 0x02014b50
|4|2|Versija sukūrė
|6|2|Ištraukti reikalinga versija (minimali)
|8|2|Bendroji bitų vėliavėlė
|10|2|Suspaudimo metodas
|12|2|Paskutinės failo modifikacijos laikas
|14|2|Paskutinės pakeitimo data
|16|4|CRC-32
|20|4|Suspaustas dydis
|24|4|Nesuspaustas dydis
|28|2|Failo pavadinimo ilgis (n)
|30|2|Papildomas lauko ilgis (m)
|32|2|Failo komentaro ilgis (k)
|34|2|Disko numeris, kuriame prasideda failas
|36|2|Vidiniai failo atributai
|38|4|Išoriniai failo atributai
|42|4|Santykinis vietinio failo antraštės poslinkis. Tai yra baitų skaičius nuo pirmojo disko, kuriame yra failas, pradžios iki vietinio failo antraštės pradžios. Tai leidžia programinei įrangai, nuskaitančiai centrinį katalogą, nustatyti failo vietą ZIP faile.
|46|n|Failo pavadinimas
|46+n|m|Papildomas laukas
|46+n+m|k|Failo komentaras

#### Centrinio katalogo įrašo pabaiga


|Poslinkis|Baitai|Aprašymas
---|---|---|
|0|4|Centrinio katalogo parašo pabaiga # 0x06054b50
|4|2|Šio disko skaičius
|6|2|Diskas, kuriame prasideda centrinis katalogas
|8|2|Centrinio katalogo įrašų skaičius šiame diske
|10|2|Bendras centrinio katalogo įrašų skaičius
|12|4|Centrinio katalogo dydis (baitai)
|16|4|Centrinio katalogo pradžios poslinkis, palyginti su archyvo pradžia
|20|2|Komentaro ilgis (n)
|22|n|Komentuoti

## Nuorodos

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [PKZip failo struktūra](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


