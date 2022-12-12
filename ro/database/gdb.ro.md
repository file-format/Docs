{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier GDB - Fișier de geodatabase de fișiere ESRI",
  "description":"Aflați despre formatul de fișier GDB și despre API-urile care pot crea și deschide fișiere GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Ce este un fișier GDB?

Fișierul ESRI Geodatabase (FileGDB) este o colecție de fișiere dintr-un folder pe disc care dețin date geospațiale conexe, cum ar fi seturi de date de caracteristici, clase de caracteristici și tabele asociate. Este necesar ca anumite alte fișiere să fie păstrate alături de fișierul .gdb în același director pentru ca acesta să funcționeze. Interogările pot fi executate în fișierul .gdb pentru a gestiona datele spațiale și non-spațiale.

## Format de fișier GDB - Mai multe informații

Geodatabasele de fișiere sunt formate din șapte tabele de sistem plus datele utilizatorului. Datele utilizatorului pot fi stocate în următoarele tipuri de seturi de date:

* Clasa de caracteristici
* Setul de date de caracteristici
* Set de date mozaic
* Catalog raster
* Set de date raster
* Set de date schematice
* Tabel (nespațial)
* Cutii de scule

Seturile de date de caracteristici pot conține clase de caracteristici, precum și următoarele tipuri de seturi de date:

* Atasamente
* Adnotare legată de caracteristici
* Rețele geometrice
* Seturi de date de rețea
* Tesaturi pentru pachete
* Clasuri de relații
* Terenuri
* Topologii

Dimensiunea maximă implicită a seturilor de date din bazele geografice de fișiere este de 1 TB. Dimensiunea maximă poate fi mărită la 256 TB pentru seturi de date mari (de obicei raster). Acest lucru este controlat de un cuvânt cheie de configurare. Consultați Cuvinte cheie de configurare pentru geodatabase de fișiere pentru mai multe informații.

Geodatabasele de fișiere pot conține, de asemenea, subtipuri și domenii și pot participa la replicarea checkout/check-in și la replici unidirecționale.

O geodatabase de fișiere poate fi accesată simultan de mai mulți utilizatori. Dacă utilizatorii editează, trebuie să editeze seturi de date diferite.

## Specificații de format de fișier GDB ##

Fișierul GDB este formatul proprietar ESRI și specificațiile sale nu sunt disponibile public. Din acest motiv, detaliile formatului fișierului pentru FIle GDB nu au putut fi documentate nicăieri în afară de unele surse care au făcut-o [parțial](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) prin inginerie inversă .

## Referințe ##

* [Specificații FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

