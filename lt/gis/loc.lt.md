{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"failą",
"pratęsimas",
"Dokumento formatas",
"GPS vieta",
"Kelio taškas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC – GPS vietos failo formatas",
  "description": "Sužinokite apie LOC failo formatą ir API, kurios gali kurti ir atidaryti LOC failus.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-ltc"
}
},
  "lastmod": "2021-07-18"
}

## Kas yra LOC failas?

Failas su plėtiniu .loc yra GPS vietos failas, kuriame yra geoerdvinės vietos kaip kelio taškai. Kelio taškas yra platumos ir ilgumos reikšmių pora, nurodanti vietą, kurią naudoja geografinės informacijos sistemos (GIS) programos. GPS žemėlapių sudarymo programos, pvz., DeLorme Topo, naudoja LOC failus, kad galėtų skaityti ir rodyti informaciją, esančią šiuose LOC failuose, kaip galutinių vartotojų pasirenkamus sluoksnius. Be to, jie naudojami keistis GPS duomenimis tarp programų. LOC failus galima atidaryti naudojant tokias programas kaip [TopoGrafix EasyGPS](https://www.easygps.com/), kurios rodo tokių failų turinį kaip sluoksnius ir duomenis, pavaizduotus žemėlapyje atitinkamoje geografinėje vietoje.

## LOC failo formatas – daugiau informacijos

LOC failai turi panašumų į [GPX](/gis/gpx/) failus, bet išsaugomi kitu formatu. Jie išsaugomi kaip [XML](/web/xml/) failai, kuriuose kelio taškų turinys ir susijusi informacija yra struktūrinėse žymose. Kadangi XML yra apibendrinta kalba, skirta keistis duomenimis tarp skirtingų programų, tai palengvina keitimąsi LOC duomenimis su kitomis programomis.

## LOC failo formatas – pavyzdys

Toliau pateikiama vieno kelio taško antraštė ir tekstas iš LOC failo. Kaip matyti, antraštės informacijoje yra duomenų vietos šaltinis. Kelio taške yra tokia informacija kaip ID ir susiję turinio duomenys, susieti su kelio tašku. Galiausiai, maršruto taškas yra platumos ir ilgumos reikšmių rinkinys ir tekstas, susietas su šiuo konkrečiu kelio tašku.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Nuorodos

* [TopGraphic EasyGPS](https://www.easygps.com/)


