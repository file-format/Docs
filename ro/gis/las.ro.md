{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Format de fișier Lidar LASer",
  "description":"Aflați despre formatul de fișier LAS și despre API-urile care pot crea și deschide fișiere LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Ce este un fișier LAS?

Formatul de fișier LAS (Lidar LASer) este un format de fișier binar conceput special pentru stocarea datelor din norul de puncte lidar. A fost dezvoltat și menținut de către Societatea Americană pentru Fotogrammetrie și Teledetecție (ASPRS) ca format standardizat pentru schimbul de date și interoperabilitate Lidar.

Fișierele LAS stochează informații detaliate despre punctele lidar individuale, inclusiv coordonatele 3D ale acestora (x, y și z), valorile intensității, codurile de clasificare și atributele suplimentare. Formatul acceptă atât retur discret, cât și date lidar cu formă de undă completă, permițând stocarea mai multor retururi per impuls laser.

## Format de fișier LAS

Structura unui fișier LAS constă din trei secțiuni principale: antetul fișierului, înregistrările cu lungime variabilă (VLR) și înregistrările de date punct.

1. Antet fișier: antetul fișierului conține informații esențiale despre fișierul LAS, cum ar fi versiunea formatului de date, formatul datelor punctului, numărul de puncte, coordonatele casetei de delimitare, sistemul de referință de coordonate (CRS) și alte metadate. Acesta oferă un rezumat al datelor lidar conținute în fișier.

2. Înregistrări cu lungime variabilă (VLR): VLR-urile sunt opționale și pot stoca metadate suplimentare și informații personalizate despre datele lidar. VLR-urile permit flexibilitate în extinderea formatului pentru a se adapta cerințelor specifice ale utilizatorului. Exemplele de VLR includ informații despre sistemul de senzori, parametrii de procesare a datelor sau schemele de clasificare.

3. Înregistrări de date punctuale: Înregistrările de date punctuale stochează măsurătorile lidar efective. Fiecare înregistrare de date punct reprezintă un singur punct lidar și conține atribute precum coordonatele x, y și z, valori de intensitate, coduri de clasificare (de exemplu, sol, vegetație, clădiri) și alte atribute definite de utilizator. Înregistrările de puncte pot stoca, de asemenea, marcaje de timp, numărătoare de returnări și unghiuri de scanare.

Fișierele LAS acceptă diferite formate de date (de la 0 la 10) pentru a găzdui diferite tipuri de date lidar și nivelul de informații necesar. De exemplu, formatul 0 reprezintă un format de punct simplu cu informații de bază, în timp ce formatele de la 1 la 3 oferă date mai cuprinzătoare, inclusiv informații despre forma de undă pentru fiecare returnare.

Fișierele LAS sunt acceptate pe scară largă de software-ul și instrumentele de procesare lidar, ceea ce le face un format standard pentru schimbul și analiza de date lidar. În plus, fișierele LAS pot fi comprimate folosind tehnici de compresie fără pierderi pentru a reduce dimensiunea fișierului, păstrând în același timp fidelitatea datelor originale. Versiunea comprimată a fișierelor LAS este adesea denumită LAZ, care oferă capabilități eficiente de stocare și transfer de date.

## Referințe

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
