{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADF – ESRI ArcInfo dvejetainis tinklelio formatas",
  "description":"Sužinokite apie ADF failo formatą ir API, kurios gali kurti ir atidaryti ADF failus.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Kas yra ADF failas?

Failas su .adf plėtiniu yra rastrinio duomenų failo formatas, naudojamas ESRI programinės įrangos programose, pvz., ArcGIS, ArcView ir ArcInfo. Erdviniai duomenys saugomi kaip dvejetainis tinklelis, priklausantis ESRI. Tinklelis sudarytas iš langelių eilučių ir stulpelių, kurie gali būti sveikieji skaičiai ir slankusis kablelis. Sveikųjų skaičių tinkleliai ADF faile reiškia atskirus duomenis, o slankiojo kablelio tinkleliai – ištisinius duomenis. Kitas populiarus ESRI failo formatas yra [SHP](/gis/shp/) failas, vaizduojantis geografinę informaciją vektorinių duomenų pavidalu, kurią naudos geografinės informacijos sistemų (GIS) programos.

## ADF failo formatas – daugiau informacijos

ADF failai išsaugomi kaip dvejetainiai failai į diską dvejetainėje tinklelyje. Sveikųjų skaičių tinkleliai turi atributus, kurie saugomi vertės atributų lentelėje (PVM). Kiekviena unikali reikšmė tinklelyje turi vieną PVM įrašą, kuriame įrašas saugo unikalią vertę, o langelių skaičių tinklelyje atspindi ta vertė.

Slankaus kablelio tinkleliai PVM neturi.

### Tinklelio struktūra

ADF faile tinkleliai įgyvendinami naudojant išklotinę rastrinių duomenų struktūrą. Pagrindinis vienetas šioje rastrinėje duomenų struktūroje yra stačiakampis langelių blokas. Kiekvienas blokas yra saugomas diske ir suglaudinamas kintamo ilgio failų struktūroje, vadinamoje plytelėmis. Kiekvienas blokas saugomas kaip vienas kintamo ilgio įrašas.

GRID rastrai saugomi darbo srityse, kur darbo srityje yra vienas informacijos pakatalogis ir pokatalogis kiekvienam GRID. Yra keli failai, kuriuose nurodoma geografinė vieta ir atitinkamo tinklelio atributų duomenys. Informacijos pakatalogyje yra keli failai, kuriuose saugoma tam tikra informacija apie GRID ir kitus duomenų rinkinius, pvz., aprėptį, darbo srityje.

## Nuorodos Nr.

* [ESRI tinklelio formatas](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)



