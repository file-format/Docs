{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier CUBE - Fișier Gaussian Cube - Ce este fișierul .cube și cum se deschide?",
  "description" : "Aflați despre fișierul Gaussian Cube și cum să îl deschideți.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-ro-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Ce este un fișier CUBE?

Formatul de fișier CUBE, cunoscut și sub numele de fișier Gaussian Cube (.cube) este utilizat în chimia computațională pentru stocarea datelor moleculare, în special a informațiilor despre densitatea electronilor rezultate din calculele chimiei cuantice. Acest format este asociat în mod obișnuit cu **pachetul software gauss**, care este utilizat pe scară largă pentru efectuarea de calcule ab initio a structurii electronice.

Fișierele Gaussian Cube stochează date tridimensionale, reprezentând de obicei densitatea electronică sau alte proprietăți ale moleculelor, obținute prin calcule de chimie cuantică. Fișierul conține o secțiune antet cu metadate (cum ar fi originea, numărul de puncte de date de-a lungul fiecărei axe și spațierea), urmată de grila de valori numerice care reprezintă proprietatea de interes (de exemplu, densitatea de electroni) în fiecare punct al grilei din spațiu.

Fișierul Gaussian Cube (.cube) este un fișier text simplu cu structură specifică. Antetul conține informații despre sistemul molecular și grila de date, iar valorile datelor sunt aranjate în format de grilă tridimensională. Fișierele Gaussian Cube sunt adesea folosite pentru a vizualiza proprietățile moleculare folosind software-ul de vizualizare moleculară. Programe precum **VMD (Visual Molecular Dynamics)** sau **PyMOL** pot citi fișiere Gaussian Cube pentru a afișa suprafețele moleculare, densitatea electronilor sau alte proprietăți calculate.

## Exemplu simplificat de fișier Gaussian Cube:

```
Exemplu de fișier cub
Generat de Gaussian
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (valorile datelor pentru densitatea electronilor la fiecare punct al grilei)
```

## Despre gaussian

Gaussian este o suită de aplicații software pentru chimia cuantică și chimia computațională. Accentul principal al lui Gaussian este pe metodele de chimie cuantică ab initio, care sunt abordări foarte precise, dar intensive din punct de vedere computațional, pentru studierea structurii electronice a moleculelor. Software-ul este utilizat pe scară largă în medii de cercetare și academice pentru diverse aplicații, inclusiv prezicerea proprietăților moleculare, studierea mecanismelor de reacție și explorarea structurilor moleculare.

## Despre NWChem

NWChem este un software de chimie computațională open-source conceput pentru simulări de înaltă performanță de chimie cuantică. Folosește metode ab initio, cum ar fi Hartree-Fock și teoria funcțională a densității, acceptă calculul paralel pentru calcule eficiente pe clustere și găsește aplicații în diverse domenii științifice, inclusiv chimia computațională, biochimia și știința materialelor. NWChem este cunoscut pentru versatilitatea sa, permițând cercetătorilor să studieze diferite sisteme chimice, iar natura sa open-source încurajează contribuțiile comunității și personalizarea.

## Despre VMD

VMD, care înseamnă Visual Molecular Dynamics, este un program puternic și utilizat pe scară largă de vizualizare moleculară pentru afișarea, analizarea și animarea traiectoriilor dinamicii moleculare (MD), precum și a structurilor moleculare statice. Este deosebit de popular în domeniile chimiei computaționale, biologiei moleculare și bioinformaticii structurale. VMD excelează la vizualizarea structurilor moleculare, oferind redări 3D de înaltă calitate ale moleculelor și complexelor moleculare. Acceptă o varietate de formate de fișiere moleculare.

## Despre PyMOL

PyMOL este un sistem de vizualizare moleculară și un instrument software utilizat pentru vizualizarea tridimensională a structurilor moleculare. Este deosebit de popular în domeniile biologiei structurale, bioinformaticii și chimiei computaționale. PyMOL oferă redări 3D de înaltă calitate ale structurilor moleculare, permițând utilizatorilor să vizualizeze și să exploreze forme, suprafețe și interacțiuni ale macromoleculelor biologice.

## Cum se deschide fișierul CUBE?

Fișierul CUBE poate fi deschis și referit folosind următoarele programe.

- **NWChem** (gratuit) pentru (Windows, MAC, Linux)

## Referințe
* [Format de fișier Gaussian Cube](https://paulbourke.net/dataformats/cube/)
