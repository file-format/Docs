{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADF - ESRI ArcInfo Binary Grid Format",
  "description":"Lisätietoja ADF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ADF-tiedostoja.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf-fi",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Mikä on ADF-tiedosto?

Tiedosto, jonka pääte on .adf, on rasteridatatiedostomuoto, jota käyttävät ESRI-ohjelmistosovellukset, kuten ArcGIS, ArcView ja ArcInfo. Paikkatiedot tallennetaan binääriruudukkona, joka on natiivi ESRI:lle. Ruudukko koostuu soluriveistä ja -sarakkeista, jotka voivat olla sekä kokonaislukuja että liukulukuja. ADF-tiedoston kokonaislukuruudukot edustavat erillistä tietoa ja liukulukuruudukot jatkuvat tiedot. Toinen suosittu ESRI-tiedostomuoto on [SHP](/gis/shp/)-tiedosto, joka edustaa paikkatietoa vektoritietojen muodossa Geographic Information Systems (GIS) -sovellusten käyttöön.

## ADF-tiedostomuoto – lisätietoja

ADF-tiedostot tallennetaan binääritiedostoina levylle binääriruudukossa. Kokonaislukuruudukoilla on attribuutteja, jotka on tallennettu arvomääritetaulukkoon (VAT). Jokaisella ruudukon yksilöllisellä arvolla on yksi ALV-tietue, johon tietue tallentaa yksilöllisen arvon ja ruudukon solujen lukumäärää edustaa tämä arvo.

Liukulukuruudukoissa ei ole arvonlisäveroa.

### Verkkorakenne

ADF-tiedoston sisällä ruudukot on toteutettu käyttämällä laatoitettua rasteritietorakennetta. Tämän rasteritietorakenteen perusyksikkö on suorakaiteen muotoinen solulohko. Jokainen lohko on tallennettu levylle ja pakattu vaihtuvapituiseen tiedostorakenteeseen, jota kutsutaan ruuduksi. Jokainen lohko tallennetaan yhdeksi muuttuvapituiseksi tietueeksi.

GRID-rasterit tallennetaan työtiloihin, joissa työtila sisältää yhden tieto-alihakemiston ja alihakemiston jokaista GRIDiä varten. On olemassa useita tiedostoja, jotka määrittävät maantieteellisen sijainnin ja määrittävät vastaavan ruudukon tiedot. Info-alihakemisto sisältää useita tiedostoja, jotka säilyttävät tiettyjä tietoja GRIDistä ja muista tietojoukoista, kuten kattavuudesta, työtilassa.

## Viitteet ##

* [ESRI-ruudukkomuoto](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)



