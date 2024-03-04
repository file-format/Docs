{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"failą",
"formatu",
"Failo tipas",
"pratęsimas",
"kas yra 3DS failas?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie 3DS failų formatą ir API, kurios gali atidaryti ir kurti 3DS failus.",
  "title": "3DS failo formatas",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra 3DS failas?

Failas su plėtiniu .3ds yra 3D Sudio (DOS) tinklelio failo formatas, kurį naudoja Autodesk 3D Studio. Autodesk 3D Studio yra 3D failų formatų rinkoje nuo 1990 m., o dabar tapo 3D Studio MAX, skirtu darbui su 3D modeliavimu, animacija ir atvaizdavimu. 3DS faile yra duomenų, skirtų 3D scenoms ir vaizdams atvaizduoti, ir tai yra vienas iš populiariausių 3D duomenų importavimo ir eksportavimo failų formatų. Jame atsižvelgiama į tokią informaciją kaip kameros vietos, tinklelio duomenys, apšvietimo informacija, peržiūros srities konfigūracijos, išlyginimo grupės duomenys, bitmap nuorodos ir atributai, kad būtų sukurtos viršūnės ir daugiakampiai, skirti atvaizduoti sceną.

## 3DS failo formatas – daugiau informacijos
Iš esmės 3DS yra dvejetainis failo formatas ir atitinka iš anksto nustatytą duomenų saugojimo ir gavimo struktūrą. Dvejetainis failo formatas įgalina 3DS failo formatą greičiau mažesnį, palyginti su tekstiniais failų formatais. Duomenys 3DS faile saugomi gabalų pavidalu.

### 3DS dalis

Kiekviena 3DS failo dalis yra duomenų blokas, kuriame yra ID, bloko ilgis kito bloko vietai ir patys duomenys. Dalies ID leidžia 3DS failo formato skaitytuvams praleisti blokus, kurių jie neatpažįsta. Tai taip pat padeda išplėsti formatą. Kiekviename gabale saugoma informacija, susijusi su formomis, apšvietimu ir žiūrėjimo informacija, kuri kartu atvaizduoja sceną. Lukštai yra išdėstyti hierarchine struktūra 3DS faile ir panašūs į XML dokumento objektų medį.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-ltt.

**Ruselio ilgis:** po gabalo ID rašomas 4 baitų sveikasis skaičius (mažuoju endianu), kuris reiškia gabalo ilgį. Į šį ilgį taip pat įeina duomenų ilgis, jų subblokų ilgis ir 6 baitų antraštė.

**Naudinga apkrova:** po gabalo ilgio nurodomi tikrieji gabalo duomenų baitai, o po to pateikiami jo pogrupiai toje pačioje hierarchinėje struktūroje, kurią galima išplėsti iki kelių lygių.

### Gabalo struktūra

Paprasto gabalo hierarchinė struktūra yra tokia, kaip parodyta žemiau:

**gabalas**

|pradžia|pabaiga|dydis|pavadinimas
--- | --- | --- | ---
|0|1|2|Klauso ID
|2|5|4|Kitas gabalas

Gabalai turi hierarchiją, kuri identifikuojama pagal ID. 3ds failas turi pirminį gabalo ID 4D4Dh. Tai visada yra pirmoji failo dalis. Su pirminiame gabale yra pagrindiniai gabalai.

**Pagrindiniai gabaliukai**

|id|Aprašymas
--- | ---
|3D3D|Objekto tinklelio duomenų pradžia.
|B000|Keliautojo duomenų pradžia.

Next Chunk rodyklė po ID bloko nurodo kitą pagrindinį elementą.
Iškart po pagrindinio gabalo yra kitas gabalas. Tai gali būti bet koks kitas leistinas gabalų tipas, esantis pagrindinėje jo dalyje.
For the Mesh description (3D3D) they could be any multiples of.

**3D3D dalys – tinklelio blokas**


|id|Aprašymas
--- | ---
|1100|nežinoma
|1200|Fono spalva.
|1201|nežinoma
|1300|nežinoma
|1400|nežinoma
|1420|nežinoma
|1450|nežinoma
|1500|nežinoma
|2100|Aplinkos spalvų blokas
|2200|rūkas?
|2201|rūkas?
|2210|rūkas?
|2300|nežinoma
|3000|nežinoma
|4000|Objektų blokas
|7001|nežinoma
|AFFF|nežinoma

**4000 dalių – objekto aprašymo blokas**
Pirmasis Subchunk 4000 elementas yra ASCIIZ objektų pavadinimo eilutė.
Atminkite, kad objektas gali būti tinklelis, šviesa arba fotoaparatas.

|id|Aprašymas
--- | ---
|4010|nežinoma
|4012|šešėlis?
|4100|Trikampis daugiakampis objektas
|4600|Šviesa
|4700|Kamera

## Nuorodos

* [Geometrijos failų formatai – „Autodesk“](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS – Vikipedija](https://en.wikipedia.org/wiki/.3ds)


