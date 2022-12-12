{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "fișier", "extensie", "format", "ce este un fișier cda", "muzică", "format fișier cda", "specificație format fișier cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier CDA și despre API-urile care pot crea, converti și deschide fișiere CDA.",
  "title" :"CDA - Fișier de comandă rapidă a piesei audio CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Ce este un fișier CDA?

Un fișier cu extensia .cda este un fișier stub mic generat de Microsoft Windows pentru fiecare piesă audio de pe un CD audio. Aceste fișiere conțin informații obișnuite, cum ar fi timpul de melodie și o comandă rapidă Windows care permite utilizatorilor să acceseze melodiile audio specifice. Fișierele CDA nu sunt muzică, dar indică un fișier muzical existent undeva în spațiul de stocare. O putem spune ca o scurtătură a unui fișier audio care se află pe un CD.

## Format de fișier CDA

Formatul de fișier CDA este folosit pentru a spune unui computer ce fișier audio să fie redat pe un CD. Deci, fișierele CDA devin inutile separate de un CD pe care îl reprezintă. Fișierele CDA sunt considerate de obicei resurse RIFF. Există o singură bucată care se numește „CDDA” și conține un singur bloc de date numit „FMT” în versiunea curentă a fișierului .cda. Acest bloc are o lungime de 24 de octeți. Identificatorul creat de Windows este utilizat de unitatea CD aferentă Windows 95 și Windows 98, iar playerul său nu se poate conecta la FreeDB sau CDDB. Pentru ca acesta să poată afișa titlul melodiei și numele artistului, pe care trebuie să le introduceți manual aceste informații în fișierul cdplayer.ini.

### Organizarea unui fișier CDA

Următorul tabel prezintă informații despre decalajele tipice:
| offset | lungime | continut |
---|---|---|
| 0x00 | 4 | cele 4 caractere ASCII „RIFF” |
| 0x04 | 4 | dimensiunea următoarei bucăți: întotdeauna 36 (44 - 8), pe 4 octeți (ordine Intel) |
| 0x08 | 4 | identificator de bucată: cele 4 caractere ASCII „CDDA” |
| 0x0C | 4 | cele 3 caractere ASCII „fmt” urmate de un spațiu |
| 0x10 | 4 | lungimea fragmentului: întotdeauna 24, pe 4 octeți (ordine Intel) |
| 0x14 | 2 | versiunea formatului CD, pe 2 octeți (comanda Intel). În mai 2006, întotdeauna egal cu 1. |
| 0x016 | 2 | numărul intervalului, pe 2 octeți (ordine Intel). Prima piesă are numărul 1. |
| 0x18 | 4 | identificator calculat de Windows pentru cdplayer.exe. |
| 0x1c | 4 | range offset, în număr de cadre (ordine Intel) |
| 0x20 | 4 | durata piesei, numărul total de cadre (ordine Intel) |
| 0x24 | 1 | poziție gamă: cadre |
| 0x25 | 1 | poziție interval: secunde |
| 0x26 | 1 | poziție interval: minute |
| 0x27 | 1 | un octet nul (valoare binară 0) |
| 0x28 | 1 | durata pistei: cadre |
| 0x29 | 1 | durata traseului: secunde |
| 0x2a | 1 | durata traseului: minute |
| 0x2b | 1 | un octet nul (valoare binară 0) |

## Referințe

* [Fișier .cda - După Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

