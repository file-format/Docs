{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier GCF și despre API-urile care pot crea și deschide fișiere GCF.",
  "title" : "GCF File - Nadeo Game GCF Format",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-ro",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Ce este un fișier GCF?

Un fișier .gcf este un fișier cache de joc folosit de platforma de jocuri Steam. Conține date despre joc, cum ar fi texturi, modele și alte fișiere care sunt utilizate de joc. Aceste fișiere sunt stocate pe computerul utilizatorului și sunt folosite pentru a reduce cantitatea de date care trebuie descărcate la actualizarea sau instalarea unui joc. Fișierele .gcf pot fi folosite și pentru a crea copii de siguranță ale instalării unui joc sau pentru a transfera un joc între computere.

Fișierele GCF pot fi citite și scrise de Biblioteca de programare C++ Open Source, **HLLib**.

## Format de fișier GCF

Fișierele GCF sunt salvate pe disc ca fișiere binare. GCF a fost folosit inițial ca acronim pentru Grid Cache File (numele de cod timpuriu al Steam a fost Grid), dar mai târziu a fost luat drept Game Cache File. Un fișier GCF este un fișier de arhivă care stochează jocurile Steam. Tot conținutul oficial este descărcat ca fișiere GCF. Fișierele GCF pot fi, de asemenea, partajate între jocuri.

NOTĂ: GCF este predecesorul lui [VPK file format](/game/vpk/).
## Referințe

* [Software Valve](https://www.valvesoftware.com/en/)

* [Format fișier GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib - Bibliotecă de programare C++ cu sursă deschisă pentru citirea fișierelor GCF](https://developer.valvesoftware.com/wiki/HLLib)


