
{
  "date": "2023-01-05",
  "keywords": [
"fișier pov",
"format de fișier pov",
"ce este un fișier pov",
"fişier",
"exemplu pov",
"extensia fișierului pov",
"extensie",
"format"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Aflați despre formatul de fișier POV și despre API-urile care pot deschide și crea fișiere POV.",
  "title": "POV - Fișierul persistenței vederii",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-rov"
}
},
  "lastmod": "2023-01-05"
}

## Ce este un fișier POV?

Un fișier POV este un fișier text simplu care conține instrucțiuni pentru software-ul de urmărire a razelor POV-Ray. Aceste instrucțiuni sunt scrise într-un limbaj de scripting special care este specific POV-Ray. Specifică scena care urmează să fie redată, inclusiv obiectele 3D, materialele, iluminarea și alte proprietăți care definesc aspectul scenei. Fișierele POV folosesc un limbaj de scripting special care este specific POV-Ray și poate fi folosit pentru a crea scene 3D complexe și detaliate. Extensia de fișier pentru un fișier POV este de obicei .pov” sau .povray”. Când deschideți un fișier POV în POV-Ray, software-ul citește instrucțiunile din fișier și le folosește pentru a genera o imagine redată a scenei.

Fișierele .pov sunt adesea folosite de artiști și designeri pentru a crea grafică 3D și animații pentru o varietate de aplicații, inclusiv film, televiziune, jocuri video și materiale de marketing.

## Format de fișier POV

Fișierul **.pov** începe de obicei cu o serie de instrucțiuni **#include**, care sunt folosite pentru a include biblioteci de culori, texturi predefinite și alte resurse care pot fi utilizate în scenă. Apoi, fișierul definește obiectele, materialele și alte proprietăți ale scenei folosind o serie de blocuri. Există multe alte tipuri de obiecte, materiale și alte proprietăți pe care le puteți specifica într-un fișier .pov și puteți utiliza bucle și instrucțiuni condiționale pentru a crea scene mai complexe și mai detaliate.

## Aplicații software pentru POV

Formatul de fișier .pov este utilizat de software-ul de urmărire a razelor POV-Ray, astfel încât aplicația principală pentru deschiderea fișierelor .pov este software-ul POV-Ray însuși. Puteți descărca cea mai recentă versiune a POV-Ray de pe site-ul oficial la https://www.povray.org/.

Pe lângă POV-Ray, există o serie de alte aplicații care pot deschide și edita fișiere .pov, inclusiv:

- BRL-CAD: Un software de modelare 3D open-source care poate importa și exporta fișiere .pov
- MeshLab: Un software de procesare a rețelelor 3D care poate importa și exporta fișiere .pov
- Blender: Un popular software de grafică 3D open-source care poate importa și exporta fișiere .pov

Pot exista și alte aplicații software care pot deschide și fișiere .pov, așa că poate doriți să încercați să utilizați un instrument de vizualizare a fișierelor sau un instrument de conversie dacă nu puteți deschide un fișier .pov cu aplicațiile de mai sus.

## Exemplu POV

De exemplu, iată un exemplu de fișier .pov care definește o scenă cu un singur cilindru albastru:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

În acest exemplu, blocul camerei specifică poziția și orientarea camerei în scenă, blocul `light_source` declară o sursă de lumină și specifică poziția și culoarea acesteia, iar blocul `cilindru` declară un obiect cilindru și specifică punctele finale ale acestuia, raza și proprietățile materialului. Când deschideți acest fișier .pov în software-ul POV-Ray, va reda o imagine a unui singur cilindru albastru.

## Referințe
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Site web de documentare POV-Ray](http://www.povray.org/documentation/)

