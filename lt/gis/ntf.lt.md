{
  "date": "2021-07-28",
  "keywords": [
"ntf failą",
"ntf failo formatas",
"kas yra ntf failas",
"failą",
"ntf pavyzdys",
"ntf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF – nacionalinio perdavimo formato failai",
  "description": "Sužinokite apie NTF failų formatą ir API, kurios gali kurti ir atidaryti NTF failus.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-ltf"
}
},
  "lastmod": "2021-07-28"
}

## Kas yra NTF failas?
Failai, kurių plėtinys yra .ntf, vadinami **Nacionaliniu perdavimo formatu (NTF)** failais; dažniausiai naudojamas JK Ordnance Survey (OS); specialiai geoerdviniams duomenims perduoti. Jį valdo Didžiosios Britanijos standartų institucija. Tai tapo standartiniu Ordnance Survey skaitmeninių duomenų perdavimo formatu. JK nacionalinė tinklelio projekcija, kuri yra skersinio Mercator tipas, turi visą NTF failų geografinę informaciją.

## NTF failo formatas
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Šis failo formatas buvo pristatytas siekiant išspręsti **PCIDSK** vektorinio segmento, kuriame yra tik vienas atributo laukas vienoje struktūroje, apribojimą, tačiau yra įvairių atributų, kuriuos galima išgauti naudojant vektorinius duomenis. Apeiti NTF failo formatą sudaro du segmentai. Kiekvienas segmentas susideda iš tų pačių vektorių, bet su skirtingais atributais. Pirmajame NTF vektorinio failo segmente yra vektoriai, kurių atributas yra funkcijos kodo numeris. Antrame segmente yra vektoriai, kurių atributas yra reikšmė.

### Koordinačių nuorodų sistema
GDB biblioteka vaizduoja rastrinius ir vektorinius duomenis su atitinkamomis TM projekcijos charakteristikomis:

- Pamatinė ilguma: 49,0
- Nuoroda platuma: 2.0
- Klaidingi rytai: 400 000
- Klaidinga šiaurė: -100 000
- Mastelis: 0,9996012717
– Elipsoidas: Airy 1830 (E009)
NTF failų atnaujinimui ar rašymui nėra palaikymo, taip pat negalima susieti su DTM failais.

### Ogrinfo pavyzdys
Šiame pavyzdyje NTF faile naudojama **ogrinfo** sluoksnių numeriams gauti:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Nuorodos

* [JK nacionalinis perdavimo formatas (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Web Mapping – iliustravo Tyleris Mitchellas](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


