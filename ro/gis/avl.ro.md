{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend File",
  "description":"Aflați despre formatul de fișier AVL și despre API-urile care pot crea și deschide fișiere AVL.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-ro",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Ce este un fișier AVL?

Un fișier AVL este un fișier de legendă care conține o cheie pentru o hartă generată cu software-ul ESRI ArcView GIS (Geographic Information System). Conține informații de referință simbolice utilizate în harta corespunzătoare pentru acces. Un fișier AVL poate conține mai multe informații, cum ar fi simbolul, setările de afișare, cum ar fi transparența, proprietățile de afișare dependente de scară, informațiile legate de tabelul/tabelul asociat, interogarea definiției, proprietățile de etichetare pentru straturile de caracteristici și proprietățile de afișare a adnotărilor pentru straturile de adnotare, în funcție de tip. fel de strat.

Un fișier AVL poate fi referit din fișierul [.APR](/gis/apr/) al proiectului ArcView.

## Format de fișier AVL - Mai multe informații

Fișierele AVL sunt salvate în format text simplu. Înseamnă că puteți deschide fișiere AVL în orice editor de text, cum ar fi Notepad, Notepad++ și Apple TextEdit. Odată deschis, puteți nu numai să vizualizați conținutul fișierului, ci și să le modificați.

### Diferența dintre fișierele .LYR și .AVL

 * **File Format Difference** - .lyr este un fișier binar, în timp ce .avl este un fișier text
 * **Diferență de conținut** - Un fișier .lyr conține mai multe informații decât un fișier .avl. Un fișier AVL stochează doar informații de simbolizare, în timp ce un fișier LYR stochează toate informațiile disponibile în caseta de dialog cu proprietățile stratului din ArcMap.

## Referințe

* [Diferența dintre fișierele .lyr și .avl](https://support.esri.com/en/technical-article/000005936)


