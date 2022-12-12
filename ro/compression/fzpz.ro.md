{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier FZPZ - Fișier de piesă Fritzing",
  "description":"Aflați despre ce este un fișier FZPZ și API-urile care pot crea și deschide fișiere FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Ce este un fișier FZPZ?

Un fișier FZPZ este o componentă/parte utilizată într-un proiect de circuit electronic creat cu aplicația de prototipare și proiectare a circuitelor **Fritzing**. Este o arhivă comprimată care conține un fișier [FZP](/ro/cad/fzp/) și patru imagini [SVG](/ro/image/svg/) care descriu partea generală a Fritzing. Avantajul utilizării acestor fișiere este că utilizatorii își pot partaja fișierele FZPZ cu fiecare din punctul de vedere al reutilizarii. Partajarea pieselor FZPZ ajută la integrarea pieselor de circuit pentru a crea proiecte mai mari de PCB într-un mod rapid.

## Format de fișier FZPZ - Mai multe informații

Fișierele FZPZ sunt salvate pe disc ca arhive [ZIP](/ro/compression/zip/) comprimate. Puteți redenumi extensia din .fzpz în .zip și puteți utiliza orice utilitar standard de decompresie, cum ar fi WinZIP, pentru a extrage fișierele din arhivă.

### Informații despre structura fișierului FZPZ

După cum sa menționat, un fișier FZPZ este un fișier de arhivă care conține mai multe fișiere pentru reprezentarea unei părți utilizate în placa de circuit imprimat. FZPZ conține următoarele fișiere:

* „Patru fișiere SVG” - care reprezintă panoul piesei, schematică, PCB și imagini pictograme
* „Fișier FZP” - Un fișier XML care conține informații despre proprietățile piesei, conectorii și magistralele

Fișierele sunt de obicei denumite după cum urmează.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Referințe ##

* [Piese noi cu extensia fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

