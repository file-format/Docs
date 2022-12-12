{
  "date" : "2019-10-11",
  "keywords" :[ "fișier wmf", "format fișier wmf", "ce este un fișier wmf", "fișier", "exemplu wmf", "extensie fișier wmf", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafile Format",
  "description":"Aflați despre formatul de fișier WMF și despre API-urile care pot crea și deschide fișiere WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier WMF?

Fișierele cu extensia WMF reprezintă Microsoft Windows Metafile (WMF) pentru stocarea datelor vectoriale, precum și a imaginilor în format bitmap. Pentru a fi mai precis, WMF aparține categoriei de formate de fișiere vectoriale a formatelor de fișiere grafice, care este independent de dispozitiv. Windows Graphical Device Interface (GDI) folosește funcțiile stocate într-un fișier WMF pentru a afișa o imagine pe ecran. O versiune mai îmbunătățită a WMF, cunoscută sub numele de Enhanced Meta Files (EMF), a fost publicată mai târziu, ceea ce face formatul mai bogat în funcții. Practic, WMF sunt similare cu SVG.

## Specificații format fișier WMF ##

Un fișier WMF se referea la formatul de fișier pe 16 biți la momentul lansării sale cu Windows 3.0. Formatul de fișier constă dintr-o serie de înregistrări cu lungime variabilă care conțin comenzi de desenare grafică, definiții de obiecte și proprietăți. Deoarece fișierele WMF se bazează pe comenzi redate către GDI pentru desenarea imaginii, este cunoscută și ca înregistrare digitală a imaginii care poate fi redată pentru a reproduce acea imagine. Specificațiile complete ale formatului de fișier ale WMF sunt disponibile online și ar trebui să fie consultate pentru dezvoltarea de aplicații care să funcționeze cu fișierele WMF. Un fișier WMF este organizat în:

* Înregistrare antet WMF
* Înregistrare(e) WMF
* Înregistrare WMF la sfârșitul fișierului

### Înregistrare antet WMF ###

**Înregistrarea META_HEADER** conține informații care definesc caracteristicile metafișierului, inclusiv:

* Tipul metafișierului
* Versiunea metafișierului
* Mărimea metafișierului
* Numărul de obiecte definite în metafișier
* Mărimea celei mai mari înregistrări unice din metafișier

### Înregistrare antet plasabilă WMF ###

**Înregistrarea META_PLACEABLE** conține informații extinse despre imagine, inclusiv:

* Un dreptunghi de delimitare
* Dimensiunea unității logice, pentru scalare
* O sumă de verificare, pentru validare

### Înregistrare WMF ###

Înregistrările WMF au un format generic, care este specificat în documentul de specificații. Fiecare înregistrare WMF conține următoarele informații:

* Dimensiunea recordului
* Funcția de înregistrare
* Parametri, dacă există, pentru funcția de înregistrare

## Referințe ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

