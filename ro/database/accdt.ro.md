{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier ACCDT și despre API-urile care pot crea și deschide fișiere ACCDT.",
  "title" :"ACCDT - Microsoft Access 2007 Template Database File Format",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Ce este un fișier ACCDT?

Un fișier cu extensia .accdt este un fișier șablon de bază de date Microsoft Access care conține elemente de bază de date predefinite. Aceste elemente sunt o colecție de structuri care definesc aplicațiile unei baze de date, cum ar fi schemele bazei de date pentru stocarea datelor, descrierea aspectului pentru vizualizările datelor și metadatele care descriu baza de date. Fiind fișiere șablon, fișierele ACCDT pot fi folosite pentru a crea baze de date pe baza setărilor șablonului disponibile în acestea. Fișierele bazei de date rezultate sunt salvate ca fișiere [ACCDB](/ro/database/accdb/) și populate cu date în tabele. Microsoft Access 2007 și versiunile ulterioare pot deschide fișiere ACCDT.

## Format de fișier ACCDT

Fișierele șablon ACCDT se bazează pe specificațiile Office Open XML și toate datele sunt conținute într-un pachet ZIP. Informațiile privind structura și conținutul bazei de date sunt conținute în fișierele [XML](/ro/web/xml/) și fișierele text și sunt legate între ele prin relații. Puteți redenumi un fișier ACCDT în extensia [.zip](/ro/compression/zip/) și puteți utiliza orice software de compresie pentru a extrage conținutul arhivei ZIP.

### Structura fișierului

Fișierele ACCDT sunt pachete care conțin o colecție de părți conexe. Fiecare **parte** stochează informații despre conținutul unei aplicații de bază de date folosind XML, text și formate binare, care includ:

* Obiecte baze de date
* Metadate asociate
* Structura pachetului

#### Pachet

Un pachet este o arhivă [ZIP](/ro/compression/zip/) care conține mai multe părți și este conformă cu convențiile de ambalare deschisă specificate în [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). Fișierele ACCDT trebuie să conțină cel puțin o parte a metadatelor șablonului care ar trebui să fie ținta unei relații. Această metadată a șablonului este partea de pornire a unui fișier ACCDT.

#### Partea

O parte este un flux de octeți care are un tip asociat pentru specificarea naturii și tipului de conținut stocat în ea. Enumerarea părților specifică părțile valide, tipurile de conținut valide și relațiile necesare între toate părțile dintr-un pachet.

#### Relație

„Relația pachetului” - unde ținta este o parte și sursa este pachetul ca întreg.

`Relație parte-la-parte` - unde ținta este o parte și sursa este o parte a pachetului.

„Relație explicită” - în cazul în care o resursă este referită din conținutul unei părți sursă prin referirea unui element de relație prin valoarea atributului său ID.

„Relație implicită” - o relație care nu este explicită.

„Relație internă” - în care ținta este o parte a pachetului.

`Relație externă` - unde ținta este o resursă externă care nu se află în pachet.

## Referințe ##

* [Format de fișier șablon de acces](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

