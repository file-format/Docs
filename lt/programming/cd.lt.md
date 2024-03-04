{
  "date": "2020-01-10",
  "keywords": [
"cd",
".cd",
"kas yra cd failas",
"kaip atidaryti cd failą",
"pratęsimas",
"failą",
"cd failą",
"cd failo formatas",
"cd failo plėtinys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CD – Visual Studio klasės diagramos failas",
  "description": "Sužinokite apie CD failo formatą ir API, kurios gali kurti ir atidaryti CD failus.",
  "linktitle": "CD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-ltd"
}
},
  "lastmod": "2021-06-24"
}

## Kas yra CD failas?

Failas su plėtiniu .cd yra Visual Studio klasių diagramos failas, kuriame pateikiama informacija apie struktūrą ir ryšį tarp visų dabartinio sprendimo klasių. Visual Studio sprendime (atstovaujame [.sln](/programming/sln/)) gali būti vienas ar daugiau projektų, kurių kiekvienas turi kelias skirtingas klases. Klasių diagramos failą galima sugeneruoti dešiniuoju pelės mygtuku spustelėjus projektą ir pasirinkus klasių diagramos parinktį.

## Klasės diagramos (.cd) failo formatas – daugiau informacijos

Klasių diagramos failas išsaugomas standartiniu XML failo formatu, kuris projekte pateikia klases kaip XML mazgus. Jei Visual Studio nėra, šiuos klasių diagramos failus galima atidaryti bet kurioje taikomojoje programoje, kuri palaiko XML failų atidarymą.

### Kaip pridėti klasių diagramas prie Visual Studio projekto

Visual Studio atidarykite sprendimą / projektą, kuriam norite pridėti klasės diagramą. Tada dešiniuoju pelės mygtuku spustelėkite projekto mazgą ir pasirinkite Pridėti > Naujas elementas. Arba paspauskite Ctrl + Shift + A.

 * Atsidaro dialogo langas Pridėti naują elementą.

 * Išskleiskite Bendrieji elementai > Bendra, tada šablonų sąraše pasirinkite Klasės diagrama. Visual C++ projektams ieškokite Utility kategorijos, kad rastumėte klasės diagramos šabloną.

### Eksportuokite klasių diagramas (CD) į vaizdus

Visual Studio leidžia konvertuoti / eksportuoti klasių diagramas į vaizdus, tokius kaip [PNG](/image/png/), [JPEG](/image/jpeg/) ir [BMP](/image/bmp/). Šie eksportuoti klasių diagramų failai gali būti naudojami dokumentacijai ir techninių duomenų paketo (TDP) įrašų saugojimo tikslais. Norėdami konvertuoti klasės diagramą į vaizdą, Microsoft Visual Studio galite atlikti šiuos veiksmus.

1. Atidarykite klasės diagramos (.cd) failą.
1. Klasės diagramos meniu arba diagramos paviršiaus nuorodų meniu pasirinkite Eksportuoti diagramą kaip vaizdą.
1. Pasirinkite diagramą.
1. Pasirinkite norimą formatą.
1. Pasirinkite Eksportuoti, kad baigtumėte eksportuoti.

## Nuorodos

* [Dizaino pamokos programoje Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)


