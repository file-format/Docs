{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extensie", "fișier", "format", "web", "certificat", "limbă"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER – Format de fișier certificat",
  "description":"Aflați despre formatul de fișier CER și despre API-urile care pot crea și deschide fișiere CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Ce este un fișier CER? ##

Un fișier cu extensia .cer este responsabil pentru stocarea unor informații despre certificatul de proprietar și cheia publică specifică. Acest format de fișiere nu poate stoca cheile private și are capacitatea de a stoca un singur certificat, care este x509. Autoritățile de certificare securizate special sunt cele care aparțin HTTPS, un protocol de încredere și securizat pentru navigare
CER este un certificat al serverului dvs. De obicei, este primit de autoritatea de certificare pentru domeniu. CER este considerat în mare parte la fel cu [CRT](/ro/web/crt/), deși ambele au același format de certificat SSL, dar sunt extensii de nume de fișier diferite.
Acestea pot fi utilizate pe sistemele de operare prin simpla deschidere a unui browser și verificarea securității browserului sau a site-ului web utilizat.

## Scurt istoric ##

În 1995, Thawte a devenit prima autoritate de certificare pentru rezolvarea problemei certificatelor publice SSL (secured socket link) din SUA. După aceea, există o serie de astfel de autorități care au fost înființate între 1995 și 2020.

## Format de fișier CER ##

Aceste fișiere pot fi simplu
* PKC S#7 cuprinde codificarea ASCII Base64
* Extensiile sale de fișiere sunt p7b sau p7cZ
* Pentru conținutul binar, certificatul ar fi DER sau pkcs12/pfx.
Există multe tipuri de fișiere de certificate cu anumite specificații unice:
* .pem, atunci când o organizație usThawteificate care înlănțuiește acest format este bine cunoscut pentru a crea certificate
* .arm, atunci când metoda de extragere a unei certificări asistență autosemnată, este necesară, formatul specificat în acest scop este .arm. Este reprezentat în codificare ASCII de bază 64.
* .der, Constă din date binare. Aceasta înseamnă că poate fi folosit doar pentru un singur certificat
* .pfx (PKC512), Constă dintr-o cheie privată corespunzătoare unui certificat emis de CA sau unui certificat autosemnat. Acest format este bine cunoscut pentru conversia unei implementări SSL în cealaltă.


