{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Amazon puslapio numerio indeksas",
"pratęsimas",
"failą",
"formatu",
"eBook",
"Amazon Kindle."
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie Amazon APNX failo formatą ir API, kurios gali kurti ir atidaryti APNX failus.",
  "title": "APNX – „Amazon“ puslapio numerio indeksas",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-ltx"
}
},
  "lastmod": "2021-05-28"
}

## Kas yra APNX failas? ##

Amazon puslapio numerio indekso failas, kuriame naudojamas .apnx plėtinys, yra el. knygos failo tipas; naudojo Amazon Kindle. Šie failai iš tikrųjų yra žinomi kaip puslapių numeravimo failai, naudojami Kindle įrenginiuose. Taigi APNX failai paprastai sukuriami Kindle eBooks puslapiams pažymėti. Puslapių rūšiavimo funkcija pradėta naudoti Amazon Kindle įrenginiuose nuo 3.1 programinės įrangos. Jis ieško puslapių indeksų APNX faile ir susieja jį su puslapių numeriais originalioje spausdintinėje knygoje. Šie failai išsaugomi Kindle įrenginiuose kartu su Amazon eBooks failais. Negalite atidaryti ar redaguoti APNX failų.

## APNX failo formato specifikacijos ##

### Išdėstymas

|baitai| turinys| komentarai|
---|---|---|
|4 |00010001 | Formato identifikatorius. Vertė 65537 little-endian.|
|4 |kito pradžia | Poslinkis pasibaigus pirmosios antraštės vietai. Pradedama nauja antraštės informacijos seka|
|4 |ilgis| Pirmosios antraštės ilgis|
|N |pirma antraštė | Eilutė su turinio antrašte. Pradedama kita seka|
|2 |nežinomas | Visada 1|
|2 |ilgis | Antrosios antraštės ilgis|
|2 |puslapių skaičius | Bendras baitų skaičius po antrosios antraštės, atitinkančios puslapius. Į šią sumą įeina baitai, kurių nepaiso puslapio žemėlapis.|
|2 |nežinomas | Visada 32|
|N |antra antraštė | Eilutė su puslapio susiejimo antrašte|
|4*N |pamušalas | Pirmasis skaičius, pateiktas puslapio susiejimo antraštėje, rodo 0 baitų skaičių.|
|4*N |puslapių sąrašas ||

### Turinio antraštė

Turinio antraštę sudaro eilutė, įtraukta į {}, kurioje yra raktų, reikšmių poros:

|turinys| komentarai|
---|---|
|contentGuid| Vadovas.|
|asinas | Amazon knygos Kindle versijos identifikatorius.|
|cdeType | MOBI cdeType. El. knygoms visada turėtų būti EBOK.|
|fileRevisionId | Šio failo peržiūra.|

#### Pavyzdys
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Puslapio atvaizdavimo antraštė
Puslapio susiejimo antraštė susideda iš eilutės, įtrauktos į {}, kurioje yra raktų ir reikšmių poros.

|turinys | komentarai|
---|---|
|asinas | ISBN 10 popierinei knygai, kurią puslapiai atitinka|
|puslapio žemėlapis| Trijų reikšmių kortelių. Atrodo taip: (N,N,N)\
1) baitų skaičius po antraštės, kuri pradeda puslapių numeravimo seką\
2) nežinomas\
3) nežinomas\|
#### Pavyzdys
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Puslapių sąrašas

Puslapių sąrašas yra neapdoroto HTML poslinkių seka. Kiekvienas
reikšmė yra naujo puslapio pradžia. Kiekvienas įrašas yra 4 baitų didelis endianas
tarpt.



## Nuorodos

* [Amazon APNX failo formatas](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX – sukūrė MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


