{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX failo formatas – mokymo centro XML failas",
  "description":"Sužinokite apie TCX failo formatą ir API, kurios gali kurti ir atidaryti TCX failus.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Kas yra TCX failas?

TCX (Training Center XML) failas yra duomenų mainų formatas, naudojamas dalytis duomenimis tarp kūno rengybos įrenginių. Jis buvo pristatytas 2008 m. kartu su Garmin mokymo centro produktu. Treniruočių duomenys, pvz., širdies ritmas, bėgimo ritmas, dviračio ritmas, kalorijos ir rato laikas, yra saugomi [XML](/web/xml/) formatu TCX faile. Be to, suvestiniai duomenys apie treniruotės takelį taip pat įtraukiami į TCX failą. TCX failai yra panašūs į [FIT](/gis/fit/) failus, sukurtus naudojant Garmin sportinius nešiojamus įrenginius.

## TCX failo formatas – daugiau informacijos

TCX failai išsaugomi diske kaip XML failai, o kiekvienas įrašas išsaugomas kaip veikla. Veikla apima visus treniruotės duomenis, pvz., laiką, rato laiką, ID, širdies ritmą, intensyvumą, ritmą ir sekimo informaciją, kurioje yra pozicijų poros kartu su laiko žyme tos ilgos pozicijos, panašios į [GPX](/gis/gpx/) failų.

### TCX failo formato versijos

Yra dvi šio formato versijos su savo XML schemomis, kurias priglobia Garmin. Toliau pateikiami keli iš jų:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX duomenų protokolas

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Nuorodos Nr.

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


