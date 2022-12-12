{
  "date" : "2022-02-16",
  "keywords" :[ "fișier obb", "format fișier obb", "ce este un fișier obb", "fișier", "exemplu obb", "extensie fișier obb", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier OBB - fișier Android Opaque Binary Blob",
  "description":"Aflați despre formatul de fișier OBB și despre API-urile care pot crea și deschide fișiere OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Ce este un fișier OBB?

Un fișier OBB este un fișier de extindere care conține date suplimentare care se adaugă fișierului Android [APK](/ro/compression/apk/). Magazinul Google Play nu permite să aveți un fișier APK Android cu o dimensiune mai mare de 100 MB. Dar unele aplicații pot necesita găzduire de grafică de înaltă definiție, fișiere media sau alte active mari pe lângă fișierele APK. Aici intervin tipurile de fișiere OBB. Google Play permite atașarea acestor fișiere de expansiune ca supliment la fișierul APK.

## Format de fișier OBB

Fișierele OBB sunt salvate ca fișiere binare împreună cu fișierele APK. Când un APK însoțește fișierele OBB, Google Play găzduiește fișierele de extindere pe serverul său și nu se percepe niciun cost suplimentar de la dezvoltator. Aceste fișiere suplimentare sunt stocate în spațiul de stocare partajat al dispozitivului pe cardul SD sau pe partiția montabilă pe USB atunci când aplicația este descărcată pentru instalare.

Fișierele OBB sunt descărcate și instalate la descărcare. Dar, în unele cazuri, acestea sunt descărcate pentru instalare atunci când aplicația este rulată pentru prima dată.

### OBB Dimensiunea maximă a fișierului

Magazinul Google Play vă permite să încărcați fișiere de extindere OBB cu o dimensiune de până la 2 GB. Se recomandă încărcarea fișierelor de dimensiuni mari ca fișiere [ZIP](/ro/compression/zip/) comprimate pentru o încărcare eficientă prin internet.

Aceste fișiere de expansiune pot fi găzduite fie ca fișier de expansiune principal **principal** pentru resursele suplimentare necesare aplicației, fie ca fișier de extindere a corecțiilor opționale destinat actualizărilor mici ale fișierului de expansiune principal.

## Referințe

* [Dezvoltatori Android - Fișiere de extindere](https://developer.android.com/google/play/expansion-files)

