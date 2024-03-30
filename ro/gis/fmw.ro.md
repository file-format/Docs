{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier FMW - Format de fișier FME Workbench",
  "description":"Aflați despre formatul de fișier FMW și despre API-urile care pot crea și deschide fișiere FMW.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-ro",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Ce este un fișier FMW?

Un fișier FMW este un fișier de proiect creat cu software-ul FME Workbench (vine ca parte din suita FME Desktop) care este utilizat pentru transformarea datelor spațiale. Conține setări definite de utilizator utilizate pentru manipularea datelor spațiale, cum ar fi seturi de date de intrare, proprietăți de traducere, proiecții și setări de ieșire. Setările de manipulare a datelor spațiale sunt stocate ca aspect vizual și sunt ușor de editat și salvat din nou.

Puteți deschide fișiere FMW utilizând [Safe Software FME Desktop](https://fme.safe.com/platform/).

## Format de fișier FMW - Mai multe informații

Fișierele FMW sunt stocate pe disc ca fișiere binare și pot fi citite numai folosind software-ul FME Desktop. De asemenea, software-ul poate citi date dintr-un număr de formate de baze de date relaționale și, de asemenea, acceptă o serie de formate de date.

### Informații rapide FMW

|Fapt|Valoare|
---|---|
|Cititor/Scriitor|Cititor|
|Nivel de licență|Bază|
|Dependențe|Niciuna|
|Tip de set de date|Fișier|
|Tip de caracteristică|Fixat|
|Extensii de fișiere tipice|.fmw|
|Asistență pentru traduceri automate|Da|
|Atribute definite de utilizator|Nu|
|Suport pentru sistemul de coordonate|Nu|
|Suport generic pentru culori|Nu|
|Index spațial|Nr|
|Schema necesară|Nu|
|Asistență pentru tranzacții|Nu|
|Atribut tip geometrie|Niciunul|
|Suport codificare|Nu|

### Suport pentru geometrie FMW

|Geometrie|Suportat?|
---|---|
|agregat|nu|
|cercuri|nu|
|arc de cerc|nu|
|poligon gogoasa|nu|
|arc eliptic|nu|
|elipse|nu|
|linie|nu|
|niciuna|da|
|punctul|nu|
|poligon|nu|
|raster|nu|
|solid|nu|
|suprafata|nu|
|text|nu|
|valori z|nu|


## Referințe

* [Safe Software FME Desktop](https://fme.safe.com/platform/)
* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
