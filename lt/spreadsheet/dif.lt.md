{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"failą",
"pratęsimas",
"Dokumento formatas",
"Duomenų mainų failas",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra DIF failo plėtinys ir API, kurios gali kurti ir atidaryti DIF failus.",
  "title": "DIF – duomenų mainų failo formatas",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-ltf"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra DIF failas?

DIF reiškia duomenų mainų formatą, kuris naudojamas skaičiuoklių duomenims importuoti / eksportuoti tarp skirtingų programų. Tai yra Microsoft Excel, OpenOffice Calc, StarCalc ir daugelis kitų. Jis saugo duomenis, esančius vienoje skaičiuoklėje, o tai yra vienintelis šio failo formato apribojimas.

## Trumpa DIF failo formato ## istorija

DIF failo formatą devintojo dešimtmečio pradžioje sukūrė Software Arts, Inc.. DIF failo formato specifikacijos buvo įtrauktos į VisiCalc, kuri buvo pirmoji asmeninių kompiuterių skaičiuoklių programa. Šios specifikacijos buvo saugomos autorių teisių 1981 m. ir buvo registruotasis Software Arts Products Corp. prekės ženklas.

## DIF failo formatas ##

DIF saugo skaičiuoklės turinį ASCII tekstiniame faile, kuris leidžia jį peržiūrėti ir redaguoti naudojant teksto rengyklę. Formatas užima vietą duomenų serializavimo formatų sąraše dėl keitimosi duomenimis ypatybių. DIF failą sudaro 2 skyriai; antraštė ir duomenys.

Viskas DIF yra vaizduojama 2 arba 3 eilučių dalimi. Antraštės gauna 3 eilučių dalį; duomenys, 2.

* Antraštės dalys prasideda teksto identifikatoriumi, kurį sudaro tik didžiosios raidės, tik abėcėlės simboliai ir mažiau nei 32 raidės. Sekanti eilutė turi būti skaičių pora, o trečioji eilutė turi būti kabutes.

* Duomenų dalys prasideda skaičių pora, o kita eilutė yra kabučių eilutė arba raktinis žodis.


### Vertybės ###

Reikšmė užima dvi eilutes: pirmoji yra skaičių pora, o antroji yra eilutė arba raktinis žodis. Pirmasis poros skaičius nurodo tipą:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – eilės pradžia (eilutės pradžia)
** EOD – duomenų pabaiga
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – galioja
** NA – nėra
** ERROR – klaida
** TRUE – tikroji loginė vertė
** FALSE – klaidinga loginė reikšmė
* 1 – eilutės tipas, antrasis skaičius nepaisomas, sekanti eilutė yra eilutė su dvigubomis kabutėmis


### DIF antraštės dalis ###

DIF failo antraštės dalį sudaro identifikatoriaus eilutė, po kurios eina dvi reikšmės eilutės. Skaitinės vertės antraštės dalyse vietoj galiojimo raktinių žodžių naudoja tik tuščią eilutę. Šių antraščių dalių informacija yra tokia.

* LENTELĖ – po versijos yra skaitinė reikšmė, nenaudojamoje antroje vertės eilutėje yra generatoriaus komentaras

* VEKTORIAI – stulpelių skaičius pateikiamas kaip skaitinė reikšmė

* TUPLES – eilučių skaičius pateikiamas kaip skaitinė reikšmė

* DUOMENYS – po fiktyvios skaitinės reikšmės 0, toliau pateikiami lentelės duomenys, kiekviena eilutė prieš BOT reikšmę, visa lentelė baigiama EOD reikšme


### DIF pavyzdys ###

Toliau pateiktame pavyzdyje parodytas paprasto darbalapio turinys ir jam lygiavertis DIF vaizdas.


|Vardas|Amžius
---|---|
|Bobas|34
|Lakštas|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Nuorodos Nr.

* [ DIF – pagal Vikipediją](https://en.wikipedia.org/wiki/Data_Interchange_Format)


