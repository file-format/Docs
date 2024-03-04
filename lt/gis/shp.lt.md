{
  "date": "2019-10-11",
  "keywords": [
"shp failą",
"shp failo formatas",
"kas yra shp failas",
"failą",
"shp pavyzdys",
"shp failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP – ESRI Shapefile",
  "description": "Sužinokite apie SHP failo formatą ir API, kurios gali kurti ir atidaryti SHP failus.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-ltp"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra SHP failas?

SHP yra vieno iš pirminių failų tipų, naudojamų ESRI Shapefile atvaizdavimui, plėtinys. Ji reprezentuoja geoerdvinę informaciją vektorinių duomenų forma, kurią naudos geografinės informacijos sistemos (GIS) programos. Formatas buvo sukurtas kaip atviros specifikacijos, siekiant palengvinti ESRI ir kitų programinės įrangos produktų sąveiką.

## Duomenų atstovavimas

Kaip minėta, Shapefile formatas apibūdina duomenų rinkinio geoerdvinę informaciją kaip vektorines ypatybes. Šios vektoriaus funkcijos apima:

* taškai

* linijos

* daugiakampiai


Šios ypatybės kartu gali atstovauti beveik bet kokio tipo formas, pvz., vandens šulinius, šalies ribas, erdvinius taškus, upių tėkmę, ežerus ir kt. Kiekviena vektorinė ypatybė gali turėti atributų, kurie iš tikrųjų apibrėžia tos funkcijos paskirtį. Pavyzdžiui, formos faile, kuriame yra Los Andželo miestai, gali būti miesto pavadinimas ir temperatūra kaip atributai, kurie suteikia prasmingą erdvinių duomenų vaizdą.

## Susiję failai

Atskiro shp failo negali naudoti programinės įrangos programos, kad įprasmintų jame esančius duomenis. Siekiant suprasti tokiame faile esančią informaciją, Shape failas naudoja šiuos papildomus privalomus failus.

* shx failas - indekso failas

* dbf failas – dBASE failas, kuriame saugomi visi pagrindinio failo formų atributai

* prj failas – saugo failo projekto informaciją


Taip pat gali būti kitų pasirenkamų failų, kurių pavadinimas yra toks pat kaip ir pagrindinis failas.

## SHP failo formato specifikacijos

Atviros Shapefile specifikacijos yra prieinamos internete iš ESRI [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) forma ir išsamiai aprašo bendrą failo struktūrą. Informaciją pagrindiniame .shp faile sudaro antraštės ir įrašai. Po fiksuoto ilgio failo antraštės seka kintamo ilgio įrašai, kur kiekvienas įrašas yra sudarytas iš fiksuoto ilgio įrašo antraštės, po kurios seka kintamo ilgio įrašo turinys.

### Pagrindinė SHP failo antraštė

Pagrindinė failo antraštė prasideda nuo failo pradžios ir yra 100 baitų ilgio. Šios pagrindinės failo antraštės organizavimas kartu su baitų padėtimi, verte, tipu ir baitų tvarka yra toks, kaip parodyta šioje lentelėje.


|Baitai|laukas|reikšmė|tipas|baitų tvarka
---|---|---|---|---|
|0-3|Failo kodas|9994|Sveikasis skaičius|Big Endian
|4-23|Nenaudojama|0|Sveikasis skaičius|Big Endian
|24-27|Failo ilgis|Failo ilgis|Sveikasis skaičius|Big Endian
|28-31|Versija|1000|Sveikasis skaičius|Mažasis Endianas
|32-35|Formos tipas|Formos tipas|Sveikasis skaičius|Mažasis endijas
|36-67|minimalus ribojantis stačiakampis|Xmin, Ymin, Xmax ir Ymax|dvigubas|Mažasis Endianas
|68-83|Apribojanti dėžutė|Zmin, Zmax|dviguba|Mažasis Endianas
|84-99|Apribojanti dėžutė|Mmin, Mmax|dviguba|

Reikėtų pažymėti, kad failo ilgio reikšmė yra bendras failo ilgis 16 bitų žodžiais, įskaitant penkiasdešimt 16 bitų žodžių, sudarančių antraštę.

#### Formų tipai

Formų tipų lauko reikšmės aukščiau esančioje lentelėje yra tokios:


|Vertė|Formos tipas
---|---|
|0|Nulinė forma
|1|Taškas
|3|Polyline
|5|Daugiakampis
|8|Multipoint
|11|TaškasZ
|13|PolyLineZ
|15|DaugiakampisZ
|18|MultiPointZ
|21|TaškasM
|23|PolyLineM
|25|DaugiakampisM
|28|MultiPointM
|31|MultiPatch

### Duomenų įrašai ###

Po pagrindinės failo antraštės seka kintamo ilgio įrašai, kur kiekvieną įrašą sudaro fiksuoto ilgio įrašo antraštė, po kurios seka kintamo ilgio įrašo turinys.

#### Įrašo antraštė ####

Įrašo antraštėje yra fiksuoto 8 baitų ilgio informacija apie įrašo numerį ir įrašo turinio ilgį. Įrašo antraštės struktūra yra tokia, kaip parodyta:


|Baitai|laukas|reikšmė|tipas|baitų tvarka
---|---|---|---|---|
|0-3|Įrašo numeris|Įrašo numeris|Sveikas skaičius|Didelis
|4-7|Įrašo ilgis|Įrašo ilgis|Sveikas skaičius|Didelis

#### Įrašyti turinį ####

Shape failo įrašo turinį sudaro formos tipas, po kurio nurodomi tos formos geometriniai duomenys. Formos tipas 0 reiškia nulinę formą, kuri neturi geometrinių figūros duomenų. Įrašo turinio ilgis atspindi formos dalis ir viršūnes. Paimkime taško formos tipo pavyzdį, kad paaiškintume, kaip įraše yra informacijos apie tokį formos tipą.

Taškas žymi tam tikrą geografinę vietą X,Y tvarka, kur kiekviena koordinatė pavaizduota dvigubo tikslumo verte. Toliau pateiktoje lentelėje parodytas taško formos tipo išdėstymas.


|Baitai|Formos tipas|Vertė|Tipas|Skaičius|Baitų tvarka
---|---|---|---|---|---|
|0-3|Formos tipas|1|Sveikas skaičius|1|Mažas
|4-11|X|X|dvigubas|1|Mažai
|12-19|Y|Y|dvigubas|1|Mažai

Examples of other shape types can be found the ESRI technical description document.

## Nuorodos Nr.

* [ESRI Shapefile techninis aprašas](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf), ESRI


