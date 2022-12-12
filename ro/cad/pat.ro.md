{
  "date" : "2020-03-16",
  "keywords" :[ "Fișier PAT", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul fișierului PAT și despre API-urile care pot crea și deschide fișiere PAT.",
  "title" :"Format fișier PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Ce este un fișier PAT?

Un fișier cu extensia .pat este un fișier CAD care este utilizat de software-ul AutoCAD. Aplicațiile care pot deschide fișiere PAT folosesc modelul de hașura stocat în aceste fișiere obțin informații despre textura/umplerea unei zone. Modelele conținute oferă informații despre aspectul materialului obiectelor desenate. Fișierele PAT pot fi deschise în aplicații precum Autodesk AutoCAD, CorelDRAW Graphics Suite și Ketron Software. Fișierele PAT pot fi convertite în diferite formate de imagine, cum ar fi JPG, PNG, BMP etc.

## Format de fișier PAT

Fișierele PAT sunt scrise în format text simplu și pot fi deschise în orice editor de text. Modelele de hașura din aceste fișiere sunt bazate pe vector și urmează sintaxa prezentată în documentația AutoCAD.

Toate modelele încep la punctul 0,0, modelul este calculat pentru a acoperi limita de hașurare.

### Definiția modelului

Toate definițiile modelelor constau din următoarele câmpuri:
* Un „\*” principal
* Un nume - Numele nu poate avea spații, semne de punctuație, paranteze sau bare oblice.
* O descriere

Formatul standard pentru modelele de hașurare este `<\*><name> <, descriere>`. Numele și descrierea sunt separate prin virgulă, iar descrierile nu pot depăși lungimea rândului de optzeci de caractere. Modelele de hașurare sunt definite după aceste informații.

### Exemple de modele de hașurare
Urmează un exemplu de model pătrat
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Un alt exemplu care arată modelul paralelogramului este următorul.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Referințe ##

* [Hash Patterns by Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

