{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "ce este un fișier cd", "cum se deschide fișierul cd", "extensie", "fișier", "fișier cd", "format fișier cd", "extensie fișier cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Fișier cu diagramă de clasă Visual Studio",
  "description":"Aflați despre formatul fișierului CD și despre API-urile care pot crea și deschide fișiere CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Ce este un fișier CD?

Un fișier cu extensia .cd este un fișier cu diagramă de clasă Visual Studio care oferă informații despre structura și relația dintre toate clasele din soluția curentă. O soluție Visual Studio (reprezentată prin [.sln](/ro/programming/sln/)) poate conține unul sau mai multe proiecte, fiecare având mai multe clase diferite. Fișierul diagramă de clase poate fi generat făcând clic dreapta pe proiect și selectând opțiunea diagramă de clase.

## Format de fișier diagramă de clasă (.cd) - Mai multe informații

Un fișier diagramă de clase este salvat în format standard de fișier XML care reprezintă clasele dintr-un proiect ca noduri XML. Dacă Visual Studio nu este disponibil, aceste fișiere cu diagrame de clasă pot fi deschise în orice program de aplicație care acceptă deschiderea fișierelor XML.

### Cum să adăugați diagrame de clasă la proiectul Visual Studio

În Visual Studio, deschideți Soluția/Proiectul pentru care doriți să adăugați diagrama de clasă. Apoi, faceți clic dreapta pe nodul proiectului și apoi alegeți Adăugare > Element nou. Sau apăsați Ctrl+Shift+A.

* Se deschide dialogul Adăugați un articol nou.

* Extindeți Elemente comune > General, apoi selectați Diagrama de clasă din lista de șabloane. Pentru proiectele Visual C++, căutați în categoria Utilitate pentru a găsi șablonul Diagrama de clasă.

### Exportați diagramele de clasă (CD) în imagini

Visual Studio permite convertirea/exportarea diagramelor de clasă în imagini precum [PNG](/ro/image/png/), [JPEG](/ro/image/jpeg/) și [BMP](/ro/image/bmp/). Aceste fișiere de diagramă de clasă exportate pot fi utilizate în scopul păstrării documentației și a pachetului de date tehnice (TDP). Pentru a converti o diagramă de clasă în imagine, următorii pași pot fi utilizați din Microsoft Visual Studio.

1. Deschideți fișierul diagramă de clasă (.cd).
1. Din meniul Diagramă de clasă sau din meniul de comenzi rapide ale suprafeței diagramei, alegeți Export diagramă ca imagine.
1. Selectați o diagramă.
1. Selectați formatul dorit.
1. Alegeți Export pentru a finaliza exportul.

## Referințe

* [Clasuri de proiectare în Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

