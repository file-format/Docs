{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier FIT-Fișier de activitate Garmin",
  "description":"Aflați despre formatul de fișier FIT și despre API-urile care pot crea și deschide fișiere FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Ce este un fișier FIT?

Un fișier FIT este un fișier GIS creat de dispozitivele sport Garmin wearable. Este folosit pentru a înregistra activitățile persoanei când se mișcă purtând aceste dispozitive. Datele de activitate includ locația și ora înregistrate de dispozitivul GPS. Fișierele FIT sunt, de asemenea, folosite pentru a transfera datele de activitate înregistrate folosind API-uri web. Acesta este motivul pentru care fișierele FIT sunt cel mai frecvent utilizat format de fișier pentru partajarea datelor de fitness cu alte platforme de fitness. Alte formate comune de fișiere includ [GPX](/ro/gis/gpx/), TCX și [KML](/ro/gis/kml/).

## Format de fișier FIT - Mai multe informații

Fișierele FIT sunt salvate pe disc ca fișiere binare cu informațiile înregistrate de dispozitivele Garmin pentru activitate. Informațiile stocate în interiorul unui fișier FIT includ:

* Data și ora
* Tipuri de sport
* Date lap și împărțite
* Traseu GPS
* Datele senzorului
* Evenimente pentru sesiune activă

Datele de activitate pot fi înregistrate în fișier în timp real sau exportate odată ce înregistrarea activității este finalizată.

### Mesaje de activitate FIT

Un fișier de activitate FIT poate include unele tipuri de mesaje necesare. Următoarele sunt mesajele necesare pentru un fișier de activitate.

|Mesaj|Scop|
---|---|
|Id fișierul| Mesajul File ID este necesar pentru toate tipurile de fișiere FIT și este de așteptat să fie primul mesaj din fișier. Pentru fișierele de activitate, proprietatea Type ar trebui să fie setată la 4.|
|Activitate| Este necesar un singur mesaj de activitate într-un fișier de activitate FIT. În mesajul Activitate sunt incluse proprietățile Local Timestamp și Session Count. Timpul local este utilizat pentru a determina decalajul fusului orar care poate fi aplicat tuturor marcajelor de timp din fișier. Majoritatea dispozitivelor înregistrează fișiere FIT în timp real, iar numărul de sesiuni va fi necunoscut până la sfârșitul înregistrării. Din această cauză, mesajul Activitate va fi adesea ultimul mesaj din fișier.|
|Sesiune| Fișierele de activitate vor conține unul sau mai multe mesaje de sesiune. Un mesaj de sesiune este un tip de mesaj Rezumat. Ora de pornire, Timpul total scurs, Timpul total al temporizatorului și Timpul de timp sunt câmpuri obligatorii pentru toate mesajele rezumate.|
|Poala| Mesajele Lap reprezintă ture sau intervale din cadrul sesiunii. Un mesaj Lap este un tip de mesaj Rezumat. Ora de pornire, Timpul total scurs, Timpul total al temporizatorului și Timpul de timp sunt câmpuri obligatorii pentru toate mesajele rezumate.|
|Înregistrare| Mesajele de înregistrare includ coordonatele GPS, viteza, distanța, ritmul cardiac, puterea etc.|

## Resurse utile fișierului FIT

* [Decodificarea fișierelor de activitate FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Codificarea fișierelor de activitate FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referințe ##

* [Fișier de activitate FIT](https://developer.garmin.com/fit/file-types/activity/)

