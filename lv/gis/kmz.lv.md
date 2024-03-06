{
  "date": "2019-10-11",
  "keywords": [
"kmz fails",
"kas ir kmz fails",
"failu",
"kmz piemērs",
"kmz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ — KML ZIP faila formāts",
  "description": "Uzziniet par KMZ failu formātu un API, kas var izveidot un atvērt KMZ failus.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-lvz"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir KMZ fails?

KMZ (KML Zipped) fails ir ZIP faila [KML](/gis/kml/) attēlojums, kas satur ģeotelpisko informāciju, kas ir skatāma ĢIS lietojumprogrammās, piemēram, Google Earth. Informācija par vietas atzīmēm failā tiek attēlota kā platums un garums kopā ar pielāgotu nosaukumu. Vienu iepakotu KMZ failu var viegli koplietot ar citiem lietotājiem. KMZ faili var ietvert arī 3D modeļa datus modeļa ģeogrāfiskai attēlošanai. KMZ failu var atvērt pakalpojumā Google Maps, saglabājot failu tiešsaistes vietā un pēc tam ierakstot URL Google Maps meklēšanas lodziņā.

## Faila struktūra ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Varat eksportēt datus no Google Earth, piemēram, lietojumprogrammas, tieši KMZ faila formātā. Galvenā KML faila nosaukums ir **doc.kml**. Iepakojot KMZ failu, tam var pievienot vairāk nekā vienu KML failu, taču tas nesniegs nekādu labumu, jo Google Earth, atverot KMZ failu, meklē pirmo KML failu un nolasa to. Tas ignorē visus citus arhīvā atrastos KML failus. Lai pārliecinātos, ka Google Earth nolasa vēlamo KML failu, KMZ failā ieteicams ievietot tikai vienu KML failu.

Attēli, modeļi, faktūras, skaņas faili un citi resursi, uz kuriem ir atsauce doc.kml failā, tiek ievietoti citā galvenās mapes apakšmapē. Tas var būt saistīts arī ar zināmu sarežģītību atkarībā no atbalsta failu skaita. Saites uz šiem resursiem var būt relatīvas atsauces vai absolūtas atsauces.

### Relatīvās atsauces ###

Ja resursi ir novietoti blakus galvenajam doc.kml galvenajā mapē esošajā apakšmapē, relatīvā atsauce var norādīt uz šiem atbalsta failiem, kā parādīts nākamajā piemērā (tikai ikonai).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolūtā atsauce ###

Absolūti var atsaukties arī uz resursiem. Absolūtās atsauces satur pilnu saistītā faila URL. Kad faili tiek ievietoti centrālajā serverī, absolūtā atsauce nodrošina, ka tie paliek nepārprotami salīdzinājumā ar relatīvajām atsaucēm. Nav ieteicams pilnībā atsaukties uz lokālo failu, jo šīs saites pārtrūks, kad faili tiek pārvietoti uz jaunu sistēmu. Absolūtās atsauces piemērs ir šāds:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Skatīt arī ##

* [GeoJSON](/gis/geojson/)


## Atsauces Nr.

* [Google Earth un KMZ faili](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


