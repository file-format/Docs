{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier NSF și despre API-urile care pot crea și deschide fișiere NSF.",
  "title" :"Format de fișier NSF - Format de bază de date Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier NSF?

Un fișier cu extensia .nsf (Notes Storage Facility) este un format de fișier de bază de date utilizat de [software-ul IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), care era cunoscut anterior ca Lotus Notes. Acesta definește schema pentru a stoca diferite tipuri de obiecte, cum ar fi e-mailuri, întâlniri, documente, formulare și vizualizări. Toate aceste informații sunt conținute într-un singur fișier NSF pentru colaborare în afaceri similar cu un fișier PST/OST. Unele dintre aplicațiile care pot deschide fișiere NSF includ IBM Lotus Notes și IBM Domino.

## Specificații de format de fișier NSF

Fișierele NSF sunt de natură binară, iar specificațiile lor sunt disponibile de către Joachim Metz pe [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Conform acestor detalii, un fișier NSF cuprinde:

* Antet fișier
* Antetul bazei de date

În plus, este format din:

* Superbloc
* Bloc descriptor al găleții
* Bitmap
* Înregistrare relocare găleată Vector
* Rezumat găleți
* Găleți non-rezumat


### Antet fișier NSF

Antetul fișierului NSF are o dimensiune de 6 octeți. Se compune din:

|Offset|Dimensiune|Valoare|Descriere|
---|---|---|---|
0|2|0x1a 0x00|Semnătura|
2|4| |Dimensiunea antetului bazei de date|

### Antetul bazei de date

Antetul bazei de date NSD conține următoarele valori confirmate.

* Informații baza de date
* Identificator baze de date (DBID)
* Informații de replicare
* Indicatori tampon pentru informațiile bazei de date
* Titlu
* Categorii
* Clasa
* Clasa de design (numele șablonului)
* Identificatori de note speciale
* Captuseala
* Informații baza de date 2
* Informații baza de date 3
* Informații baza de date 4
* Informații baza de date 5
* Captuseala
* Identificator de instanță a bazei de date (DBIID)
* Istoricul replicărilor

## Referințe

* [Format NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

