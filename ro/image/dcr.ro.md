{
  "date" : "2021-26-08",
  "keywords" :[ "fișier dcr", "format fișier dcr", "ce este un fișier dcr", "fișier", "exemplu dcr", "extensie fișier dcr", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Fișier imagine RAW pentru cameră digitală",
  "description":"Aflați despre formatul de fișier DCR și despre API-urile care pot crea și deschide fișiere DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Ce este un fișier DCR? ##
Un fișier cu extensia dcr conține conținutul unei fotografii digitale salvate în formatul Kodak Digital Camera RAW (DCR). DCR este prescurtarea pentru **Digital Camera Raw**; conține versiunea necomprimată și fără pierderi a datelor imaginilor capturate de o cameră digitală Kodak. Fotografilor profesioniști le place să folosească aceste fișiere, deoarece stochează imagini la o calitate superioară decât formatele de imagine comprimate de calitate scăzută.

## Format de fișier DCR
DCR este un format proprietar dezvoltat de Eastman Kodak Company; denumit pur și simplu Kodak. Un fișier imagine Digital Camera Raw (DCR) conține date procesate minim de la senzorul de imagine o cameră digitală. Aceste fișiere nu sunt încă procesate și, prin urmare, nu sunt gata pentru a fi tipărite sau editate cu un editor grafic bitmap.
De obicei, un convertor brut procesează imaginea într-un spațiu de culoare intern cu o gamă largă de culori, unde pot fi realizate precizia și rafinamentul înainte de conversia într-un format de fișier raster, cum ar fi TIFF sau JPEG, pentru stocare, imprimare sau manipulare ulterioară.
### Conținutul fișierului
Structura fișierelor brute urmează adesea un model generic:
- Un antet scurt de fișier care conține un indicator al ordinii octeților fișierului.
- Metadatele senzorului camerei care sunt necesare pentru a interpreta datele imaginii senzorului, inclusiv atributele CFA, dimensiunea senzorului și profilul său de culoare.
- Metadatele imaginilor care pot fi utile pentru includerea în orice mediu CMS sau bază de date. Unele fișiere brute conțin o secțiune de metadate standardizate cu date în format Exif.
- O miniatură a imaginii.
- O conversie JPEG la dimensiune completă a imaginii, care este utilizată pentru a previzualiza fișierul pe panoul LCD al camerei.
- În cazul scanărilor de filme cinematografice, fie codul de timp, codul cheie sau numărul de cadre din secvența fișierului care reprezintă secvența de cadre dintr-o bobină scanată.
- Datele imaginii senzorului
### Datele imaginii senzorului
Fișierul brut joacă rolul în fotografia digitală similar cu filmul fotografic în fotografia de film. Fișierele brute, conțin astfel datele la rezoluție completă, citite de la fiecare dintre pixelii senzorului de imagine al camerei. Senzorul camerei este aproape în mod constant suprapus cu un CFA (Color Filter Array. Acesta poate fi folosit în conversia imaginilor cu interval dinamic înalt atunci când sunt disponibile date în format brut; ca o alternativă mai simplă la abordarea HDI cu expuneri multiple de captare a trei imagini separate.


## Referințe ##

* [Format imagine brută - De Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [Ce este un fișier DCR](https://expertphotography.com/dcr-file/)

