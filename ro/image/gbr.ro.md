{
  "date" : "2019-10-11",
  "keywords" :[ "fișier gbr", "format fișier gbr", "ce este un fișier gbr", "fișier", "exemplu gbr", "extensie fișier gbr", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier GBR - Format de fișier Gerber pentru PCB",
  "description":"Aflați despre formatul de fișier GBR și despre API-urile care pot crea și deschide fișiere GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GBR?

Un fișier cu extensia .gbr este un format de fișier imagine Gerber pentru schimbul de transfer de date de proiectare a plăcilor de circuite imprimate (PCB). A fost dezvoltat de Ucamco. Datele de proiectare PCB sunt componenta principală cerută de industria de fabricație pentru manipulare. Un fișier GRB conține date PCB, cum ar fi straturi de cupru, mască de lipit, legenda și date de foraj și traseu. Poate fi utilizat pentru a transfera date, cum ar fi caracteristicile de fabricație a PCB-ului, inclusiv grosimea sau finisajul într-un format standardizat. Toate sistemele de proiectare PCB scot fișiere Gerber care pot fi gestionate de sistemele de fabricare PCB. Fișierele GBR au devenit acum standardul de facto pentru transferul de date de proiectare a plăcilor de circuite imprimate (PCB). Ucamco a oferit un [vizor online gratuit](https://gerber-viewer.ucamco.com/) pentru a deschide și a vizualiza formatele de fișiere GBR.

## Format de fișier GBR

GBR este un format UTF-8 care poate fi citit de om, care constă din doar 27 de comenzi. Datorită acestei liste scurte de comenzi și a compactității sale, GBR este ușor de depanat. Gerber în esență este un format vectorial deschis pentru imagini binare 2D. Metainformațiile sunt transferate împreună cu imaginile prin Atribute. Un singur fișier GRB specifică o singură imagine și nu necesită interpretarea niciunui fișier însoțitor sau parametri externi. O imagine are nevoie de un singur fișier. Folosește caractere ASCII pe 7 biți pentru toate comenzile și numele definite în specificație care sunt imprimabile. Aceasta acoperă în totalitate generarea completă de imagini.

### Exemplu de fișier GBR

Urmează un exemplu de fișier Gerber care creează un cerc cu diametrul de 1,5 mm centrat pe origine. Există o comandă pe linie.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referințe

* [Format Gerber](https://www.ucamco.com/en/gerber)

