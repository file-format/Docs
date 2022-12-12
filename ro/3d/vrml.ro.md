{
  "date" : "2019-10-11",
  "keywords" :[ "fișier vrml", "format fișier vrml", "ce este un fișier vrml", "fișier", "exemplu vrml", "extensie fișier vrml", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier VRML",
  "description":"Aflați despre formatul de fișier VRML și despre API-urile care pot deschide și crea fișiere VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VRML?
Virtual Reality Modeling Language (VRML) este un format de fișier pentru reprezentarea obiectelor lumii interactive [3D](/ro/3d/) pe World Wide Web (www). Își găsește utilizarea în crearea de reprezentări tridimensionale ale scenelor complexe, cum ar fi ilustrații, definiții și prezentări de realitate virtuală. Formatul a fost înlocuit de [X3D](/ro/3d/x3d/). Multe aplicații de modelare 3D pot salva obiecte și scene în format VRML.

## Format de fișier VRML

VRML este un format de fișier text care specifică informații precum vârfurile și marginile unui poligon 3D, împreună cu informații precum culoarea suprafeței, texturile cartografice UV, strălucirea, transparența și așa mai departe. Are capacitatea de a reprezenta obiecte statice și animate, pe lângă faptul că are hyperlinkuri către alte medii, cum ar fi sunet, filme și imagini. Acest lucru permite deschiderea elementelor cu hyperlink atunci când utilizatorul face clic pe aceste obiecte.

Fișierele TVRML în terminologia comună se numesc „lumi” și au extensia .wrl. Natura textuală a acestor fișiere face posibilă reducerea dimensiunii fișierului folosind formate de compresie precum gzip, făcându-le mai favorabile pentru transferul rapid pe internet. Specificațiile de format de fișier pentru [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) acționează ca referință pentru dezvoltatori pentru crearea de aplicații compatibile pentru citirea/scrierea acestor fișiere.

## Criteriul de proiectare ##

Scopul și designul VRML se învârte în jurul următoarelor cerințe.

* **Autorabilitate** - Face posibilă dezvoltarea generatoare de aplicații și editori și importarea datelor din alte formate industriale
* **Completitudine** - Oferă toate informațiile necesare implementării și abordează un set complet de caracteristici pentru acceptarea largă în industrie
* **Composabilitate** - Capacitatea de a utiliza elemente ale VRML în combinație și, astfel, de a permite reutilizarea.
* **Extensibilitate** - Capacitatea de a adăuga elemente noi.
* **Implementabilitate** -Capabil de implementare pe o gamă largă de sisteme.
* **Potențial multi-utilizator** - Nu ar trebui să împiedice implementarea mediilor multi-utilizator.
* **Ortogonalitate** - Elementele VRML ar trebui să fie independente unele de altele, sau orice dependențe ar trebui să fie structurate și bine definite.
* **Performanță** - Elementele trebuie proiectate cu accent pe performanța interactivă pe o varietate de platforme de calcul.
* **Scalabilitate** - Elementele VRML ar trebui să fie proiectate pentru compoziții infinit de mari.
* **Practica standard** - Doar acele elemente care reflectă practica existentă, care sunt necesare pentru a sprijini practica existentă sau care sunt necesare pentru a sprijini standardele propuse ar trebui să fie standardizate.
* **Bine structurat** - Un element trebuie să aibă o interfață bine definită și un scop necondiționat simplu. Elementele multifuncționale și efectele secundare trebuie evitate.

## Referințe ##

* [VRML - După Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [Specificații de format de fișier VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

