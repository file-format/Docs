{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","fișier", "format", "tip fișier", "extensie","ce este un fișier 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier 3DS și despre API-urile care pot deschide și crea fișiere 3DS.",
  "title" :"Format fișier 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este fișierul 3DS?

Un fișier cu extensia .3ds reprezintă formatul de fișier mesh 3D Sudio (DOS) utilizat de Autodesk 3D Studio. Autodesk 3D Studio se află pe piața formatelor de fișiere 3D din anii 1990 și acum a evoluat la 3D Studio MAX pentru a lucra cu modelarea, animația și randarea 3D. Un fișier 3DS conține date pentru reprezentarea 3D a scenelor și imaginilor și este unul dintre formatele de fișiere populare pentru importul și exportul de date 3D. Se ia în considerare informații precum locațiile camerei, datele Mesh, informațiile despre iluminare, configurațiile ferestrelor de vizualizare, datele grupului de netezire, referințele bitmap și atributele pentru a crea vârfuri și poligoane pentru redarea unei scene.

## Format de fișier 3DS - Mai multe informații
La baza sa, 3DS este un format de fișier binar și urmează o structură predefinită pentru stocarea și preluarea datelor. Formatul de fișier binar permite formatul de fișier 3DS mai rapid și mai mic în comparație cu formatele de fișiere bazate pe text. Datele din interiorul unui fișier 3DS sunt stocate sub formă de bucăți.

### 3DS Chunk

Fiecare bucată dintr-un fișier 3DS este un bloc de date care conține un ID, lungimea blocului pentru locația blocului următor și datele în sine. ID-ul fragmentului permite cititorilor de format de fișiere 3DS să sară peste blocurile pe care nu le recunosc. De asemenea, ajută la extensibilitatea formatului. Fiecare bucată stochează informații legate de forme, iluminare și informații de vizualizare care, împreună, redau scena. Bucățile sunt aranjate într-o structură ierarhică într-un fișier 3DS și seamănă cu arborele XML Document Object în reprezentare.

**Chink ID:** Primii doi octeți ai unei bucăți reprezintă un identificator de porțiune care permite cititorului de fișiere să decidă dacă îl ia în considerare în timpul citirii sau să îl ignore.

**Lungimea fragmentului:** ID-ul fragmentului este urmat de un număr întreg de 4 octeți (în little-endian) care reprezintă lungimea fragmentului. Această lungime include, de asemenea, lungimea datelor, lungimea sub-blocurilor și antetul de 6 octeți.

**Payload:** Lungimea fragmentului este urmată de octeții de date reali pentru fragment, urmați de sub-porțiunele sale în aceeași structură ierarhică care poate fi extinsă la mai multe niveluri.

### Structura unei bucăți

Structura ierarhică a unei bucăți simple este prezentată mai jos:

**O bucată**

|început|sfârșit|dimensiune|nume
--- | --- | --- | ---
|0|1|2|Chunk ID
|2|5|4|Următoarea bucată

Bucățile au o ierarhie impusă acestora, care este identificată prin ID-ul său. Un fișier 3ds are ID-ul fragmentului primar 4D4Dh. Aceasta este întotdeauna prima bucată a fișierului. Cu în bucățile primare sunt bucățile principale.

**Bucăți principale**

|id|Descriere
--- | ---
|3D3D|Începutul datelor rețelei de obiecte.
|B000|Începutul datelor keyframer.

Indicatorul Next Chunk de după blocul ID indică următoarea bucată principală.
Direct după o bucată principală este o altă bucată. Acesta ar putea fi orice alt tip de bucată permisă în domeniul său de aplicare principal.
Pentru descrierea Mesh (3D3D), acestea ar putea fi orice multipli de.

**Subporțiuni din 3D3D - Bloc de plasă**


|id|Descriere
--- | ---
|1100|necunoscut
|1200|Culoarea fundalului.
|1201|necunoscut
|1300|necunoscut
|1400|necunoscut
|1420|necunoscut
|1450|necunoscut
|1500|necunoscut
|2100|Bloc de culoare ambientală
|2200|ceaţă?
|2201|ceaţă?
|2210|ceaţă?
|2300|necunoscut
|3000|necunoscut
|4000|Bloc de obiecte
|7001|necunoscut
|AFFF|necunoscut

**Subchunks of 4000 - Object Description Block**
Primul element al Subchunk 4000 este un șir ASCIIZ al numelui obiectelor.
Amintiți-vă că un obiect poate fi o plasă, o lumină sau o cameră.

|id|Descriere
--- | ---
|4010|necunoscut
|4012|umbra?
|4100|Obiect poligon triunghiular
|4600|Lumina
|4700|Camera

## Referințe

* [Formate de fișiere de geometrie - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS - După Wikipedia](https://en.wikipedia.org/wiki/.3ds)

