{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Fișier de schimb de date LIDAR comprimat",
  "description":"Aflați despre formatul de fișier LAZ și despre API-urile care pot crea și deschide fișiere LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Ce este un fișier LAZ?

Formatul de fișier LAZ este o versiune comprimată a formatului de fișier LAS (Lidar LASer), care este conceput special pentru stocarea datelor din norul de puncte lidar. Fișierele LAZ păstrează aceleași date și structură ca fișierele LAS, dar folosesc tehnici de compresie fără pierderi pentru a reduce dimensiunea fișierului, păstrând în același timp fidelitatea datelor originale.

## Format de fișier LAZ - Scurt istoric

Formatul de fișier LAZ a fost dezvoltat pentru a răspunde cererii tot mai mari de stocare și transmitere eficiente a seturilor de date mari lidar. Prin comprimarea fișierelor LAS, fișierele LAZ își reduc semnificativ dimensiunea, făcându-le mai ușor de gestionat și transferat. Comprimarea este realizată prin utilizarea unei combinații de diferiți algoritmi, cum ar fi codarea entropică și codificarea cu lungime variabilă, pentru a reprezenta atributele punctului lidar într-o formă mai compactă.

## Format de fișier LAZ

În ciuda compresiei, fișierele LAZ păstrează capacitatea de a restabili complet datele LAS originale fără nicio pierdere de informații. Aceasta înseamnă că, odată ce un fișier LAZ este decomprimat, acesta poate fi procesat și analizat în același mod ca un fișier LAS necomprimat. Procesul de compresie și decompresie se realizează de obicei folosind software sau biblioteci specializate care acceptă formatul LAZ.

Formatul de fișier LAZ menține compatibilitatea cu fișierele LAS, asigurând interoperabilitatea între software-ul lidar și instrumentele de procesare. Aceasta înseamnă că aplicațiile care pot citi și procesa fișiere LAS pot gestiona de obicei fișierele LAZ fără nicio modificare. În plus, fișierele LAZ includ în continuare antetul fișierului, înregistrările cu lungime variabilă (VLR) și înregistrările de date punctuale, păstrând aceeași structură ca fișierele LAS.

## Avantajele formatului de fișier LAZ

**Dimensiune redusă a fișierului:** compresia LAZ reduce semnificativ dimensiunea fișierelor seturi de date lidar, făcându-le mai ușor de gestionat și mai ușor de stocat și transferat.

**Integritatea datelor:** compresia LAZ este fără pierderi, ceea ce înseamnă că datele decomprimate sunt o replică exactă a datelor LAS originale, asigurând nicio pierdere de informații sau precizie.

**Interoperabilitate:** fișierele LAZ sunt compatibile cu fișierele LAS, permițând integrarea perfectă cu software-ul și fluxurile de lucru existente lidar.

**Procesare eficientă:** Datorită dimensiunii lor reduse, fișierele LAZ pot fi încărcate și procesate mai rapid, îmbunătățind timpul general de procesare și analiză.

Formatul de fișier LAZ a fost adoptat pe scară largă în comunitatea lidar ca standard pentru stocarea și schimbul de date lidar comprimate. Oferă un echilibru între compresia eficientă a datelor și integritatea datelor, permițând manipularea mai ușoară a seturilor de date lidar mari, menținând în același timp acuratețea și calitatea datelor originale.

## Referințe

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
