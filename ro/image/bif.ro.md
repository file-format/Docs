{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier BIF - Format de imagine întreg diapozitiv Ventana",
  "description":"Aflați despre formatul de fișier BIF și despre API-urile care pot crea și deschide fișiere BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Ce este un fișier BIF?

Un fișier BIF este un fișier imagine raster care conține imaginea specimenului de diapozitiv. Constă în mai multe imagini TIFF care sunt combinate prin aplicații de vizualizare a diapozitivelor într-o singură imagine compozită. Fișierele BIF sunt create de scanerul digital de diapozitive Ventana Medical System și sunt pe deplin compatibile cu varianta BigTIFF a definiției [TIFF](/ro/image/tiff/) v 6.0.

## Format de fișier BIF

Un fișier BIF este salvat ca fișier imagine binar și este format din până la 200.000 x 200.000 pixeli. Acest lucru poate duce la dimensiuni mari ale fișierelor, depășind limita de dimensiune de 4 GB impusă de pointerii de fișiere pe 32 de biți definiți de standardul TIF. Cu indicatorii de fișiere pe 64 de biți, totuși, această barieră de dimensiune a fișierului este depășită de varianta BigTIFF a standardului TIFF.

### Cine folosește fișierul BIF?

Fișierele BIF sunt utilizate de scanerele digitale de diapozitive pentru a scana și a crea copii digitale ale specimenelor de diapozitive. Dacă sunteți patolog, puteți deschide aceste fișiere BIF în aplicații de vizualizare a diapozitivelor. Cu un nivel mare de detalii și date de înaltă rezoluție, puteți mări și micșora o imagine de diapozitiv pentru a vizualiza secțiunile specimenului în mai multe sau mai puține detalii. Fișierul de metadate [XML](/ro/web/xml/) prezent în aceste fișiere definește modul în care imaginile trebuie combinate și imaginea care ar trebui utilizată ca miniatură a fișierului.

## Cum se deschide fișierul BIF?

Puteți deschide fișiere BIF cu:

* OpenSlide (multplatform)
* ImageJ (multiplatformă)
* NetScope Viewer (Windows)

## Referințe ##

* [Carta albă Roche Digital Pathology BIF](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

