{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier TCX – Fișier XML Centrul de instruire",
  "description":"Aflați despre formatul de fișier TCX și despre API-urile care pot crea și deschide fișiere TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Ce este un fișier TCX?

Un fișier TCX (Training Center XML) este un format de schimb de date folosit pentru a partaja date între dispozitivele de fitness. A fost introdus în 2008 cu produsul Garmin Training Center. Datele de antrenament, cum ar fi ritmul cardiac, cadența de alergare, cadența bicicletei, caloriile și timpul pe tur sunt stocate în format [XML](/ro/web/xml/) în fișierul TCX. În plus, în fișierul TCX sunt incluse și date rezumative despre traseul de antrenament. Fișierele TCX sunt similare cu fișierele [FIT](/ro/gis/fit/) care sunt create cu dispozitive Garmin sport.

## Format de fișier TCX - Mai multe informații

Fișierele TCX sunt salvate pe disc ca fișiere XML cu fiecare înregistrare salvată ca activitate. O activitate cuprinde toate datele unui antrenament, cum ar fi timpul, timpul turului, ID, ritmul cardiac, intensitatea, cadența și informațiile despre pistă, care conține perechile de poziții împreună cu marcajul de timp pentru acea poziție lat-long similară cu [GPX] (/ro/gis/gpx/) fișiere.

### Versiuni de format de fișier TCX

Există două versiuni ale acestui format cu propriile scheme XML găzduite de Garmin. Următoarele sunt câteva dintre ele:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protocolul de date TCX

O versiune rapidă a formatului TCX XML este disponibilă pe Github ca [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referințe ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

