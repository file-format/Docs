{
  "date" : "2021-12-09",
  "keywords" :[ "aro", "fișier .aro", "format fișier aro", "un tip de fișier", "fișier", "tip", "ce este un fișier .aro" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ARO - Fișier aplicație web SteelArrow",
  "description" :"Aflați despre ce este un fișier ARO și API-urile care pot crea și deschide fișiere ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Ce este un fișier ARO?

Un fișier ARO este un fișier de pagină web pe partea serverului care este generat cu aplicația web SteelArrow. Conține [HTML](/ro/web/html/) și etichete și scripturi SteelArrow. Acestea sunt executate pe server pentru a genera o pagină de răspuns completă înainte de a le trimite către browserul utilizatorului. Fișierele ARO conțin aproape 95% din conținut HTML, în timp ce restul este format din cod SteelArrow. Pentru ca fișierele ARO să funcționeze pentru dvs., serverul de aplicații web SteelArrow ar trebui să fie instalat și rulat pe mașina serverului web.

## Format de fișier ARO

Fișierele ARO sunt scrise într-un fișier HTML cu limbaj de marcare cu cod JavaScript încorporat și applet-uri Java. [Etichetele SteelArrow](http://www.steelarrow.com/docs/basics1.aro) sunt elementele de bază pentru dezvoltarea paginilor web. Deși acestea nu schimbă afișarea paginii, sunt folosite pentru a umple pagina cu date. În plus, ele pot fi utilizate și pentru a controla ieșirea cu instrucțiuni condiționate.

### Exemplu de etichetă ARO

The<SAOUTPUT> Eticheta ARO le permite dezvoltatorilor să scoată valorile datelor în orice loc dintr-un script. De exemplu, poate fi folosit pentru a obține rezultatul tabelului PARAM cu<SAOUTPUT VALUE=PARAM[]> care poate fi afișat în HTML<BODY> etichetă.

## Referințe

* [Etichete SteelArrow](http://www.steelarrow.com/docs/basics.aro)

