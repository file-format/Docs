{
  "date": "2021-06-29",
  "keywords": [
"com-tiedosto",
"mikä on com-tiedosto",
"tiedosto",
"com esimerkki",
"com tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi COM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata COM-tiedostoja.",
  "title": "COM - DOS-komentotiedostomuoto",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-fim"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on COM-tiedosto?
COM-tiedostoja käytetään yksinkertaisesti komentojen tai käskyjen suorittamiseen. COM-tiedosto koostuu suoritettavasta ohjelmasta, joka voidaan ajaa Windowsista tai MS-DOS:sta. Samoin EXE-tiedosto, myös COM-tiedosto tallennetaan binäärimuodossa, mutta se eroaa EXE-tiedostosta, koska sillä ei ole otsikkoa tai metatietoja ja sen enimmäiskoko on noin 64 kt. Kun COM-tiedosto suoritetaan ensimmäisen kerran 32-bittisessä järjestelmässä, se kehottaa asentamaan NT Virtual DOS Machine (NTVDM) -komponentin. COM-tiedostoa voidaan ajaa Microsoft Windowsin 64-bittisessä versiossa virtuaalikoneella, joka tukee MS-DOS-ympäristöä.

## COM-tiedostomuoto
COM-tiedostomuoto on binäärinen suoritettava muoto, jota käytetään Microsoft Windowsissa tai MS-DOSissa. Sen rakenne koostuu vain joukosta ohjeita; sillä ei ole otsikkoa, eikä se sisällä tavallisia metatietoja. Se tallentaa kaikki tietonsa ja koodinsa vain yhteen segmenttiin, ja sen binaarin koko on enintään 64 kt. Tämä tiedostomuoto ei siirry itse, kun yrität suorittaa uudelleen. Joten käyttöjärjestelmä lataa sen ennalta asetettuun osoitteeseen. Lisäksi on mahdollista tehdä COM-tiedosto suoritettavaksi molemmissa käyttöjärjestelmissä **fat-binäärimuodossa**. Ohjetasolla ei ole varsinaista yhteensopivuutta. Aloituspisteen ohjeet valitaan toiminnaltaan samanlaisiksi, mutta erilaisiksi molemmissa käyttöjärjestelmissä ja saavat ohjelman käynnissä siirtymään käytössä olevan käyttöjärjestelmän osioon. Se on pohjimmiltaan kaksi eri ohjelmaa, joissa on sama menettely yhdessä tiedostossa, jota edeltää käytettävä koodi.
### COM-tiedostoesimerkki
COM-tiedostoa suoritettaessa ohjeet luetaan ensimmäisestä tavusta alkaen ja niitä noudatetaan peräkkäin, kunnes viimeinen käsky löytyy. Tässä on esimerkki ASM-koodista:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Viitteet 

* [COM-tiedosto - Wikipewdia](https://en.wikipedia.org/wiki/COM_file)


