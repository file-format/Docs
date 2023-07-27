{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Format fișier", "CAD", "Deschide", "Creare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DWG și despre API-urile care pot crea și deschide fișiere DWG.",
  "title" :"Format fișier DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DWG?

Fișierele cu extensia DWG reprezintă fișiere binare proprietare utilizate pentru a conține date de proiectare 2D și 3D. La fel ca DXF, care sunt fișiere ASCII, DWG reprezintă formatul de fișier binar pentru desenele CAD (Computer Aided Design). Conține imagini vectoriale și metadate pentru reprezentarea conținutului fișierelor CAD. Există vizualizatoare gratuite disponibile pentru vizualizarea fișierelor DWG pe sistemul de operare Windows, cum ar fi DWG TrueView gratuit de la Autodesk. Există și alte aplicații terțe care acceptă accesarea fișierelor DWG. Fișierele DWG conțin informații create de utilizator și includ:

* Designuri
* Date geometrice
* Hărți și fotografii

Acest format este utilizat pe scară largă de arhitecți, ingineri și designeri pentru diverse scopuri de proiectare.

## Scurt istoric ##

Formatul de fișier DWG a evoluat cu timpul de la introducerea sa oficială în 1982. O scurtă prezentare a evenimentelor trecute din perspectiva istoriei este următoarea.

**1982:** Autodesk a licențiat formatul de fișier DWG, care a fost dezvoltat de Mike Riddle în 1970, ca bază pentru AutoCAD.

**1998:** Odată cu lansarea AutoCAD R14.01, Autodesk a adăugat verificarea fișierelor printr-o funcție numită DWGCHECK care a încorporat o sumă de control criptată și un cod de produs, numit WaterMark de Autodesk, în fișierele DWG create de program.

**2006:** Autodesk a modificat AutoCAD 2007, pentru a include „Tehnologia TrustedDWG” pentru a încorpora șirul de text „Autodesk DWG. Acest fișier este un DWG de încredere salvat ultima dată de o aplicație Autodesk sau de o aplicație cu licență Autodesk” în fișierele DWG. Scopul acestui lucru a fost de a ajuta utilizatorii de software Autodesk să se asigure că aceste fișiere au fost create de o aplicație Autodesk sau RealDWG, ceea ce ar trebui să ajute cu siguranță la reducerea riscului de incompatibilități.

## Structura fișierului ##

DWG a fost unul dintre formatele de fișiere utilizate pe scară largă de o serie de aplicații și are o structură de fișiere robustă. Deoarece DWG este un format de fișier binar, nu poate fi citit de om ca formatul de fișier simplu ASCII [DXF](/ro/cad/dxf/). Fișierele DWG includ de obicei informații despre coordonatele imaginii și orice metadate asociate cu acestea. [Specificațiile] complete (https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) în format de fișier DWG sunt disponibile pentru descărcare de către OpenDesign. Structura fișierului formatului de fișier DWG este rezumată după cum urmează.

**Header**: antetul fișierului constă din variabile DWG Header și informații despre Cyclic Redundancy Check (CRC) care sunt utilizate pentru detectarea erorilor. Fiecare subsecțiune este un vector specializat în care se folosesc diferite lungimi de biți pentru a reprezenta diferite etichete. De exemplu, primii 6 biți ai variabilei DWG Header reprezintă șirul de versiune.

**Definiții de clasă:** Un fișier DWG poate conține numeroase clase, în funcție de scopul specific al fișierului .dwg. Informații precum dimensiunea metadatelor de clasă ale zonei de date ale clasei, numărul clasei și suma de control, în plus față de altele.

**Șablon**: Acesta este opțional și pentru versiunile R15 și R15, această secțiune se află sub secțiunea Spațiu liber obiect.

**Padding**: metadatele sunt sufixate și postfixate cu un anumit număr de octeți, ceea ce face ca versiunile mai vechi de software AutoCAD să fie compatibile cu noul format de fișier DWG.

**Date imagini**: metadatele pentru această secțiune depind de tipul .dwg specific. Pentru utilizatorii R14 și R15, această secțiune este opțională.

**Date obiect**: Datele obiect constau dintr-o listă completă de entități de tabel, intrări de dicționar etc. corespunzătoare listei existente de obiecte.

**Harta obiectului**: Locația fiecărui obiect din fișier este specificată în această secțiune a fișierului. Majoritatea metadatelor din această secțiune sunt mânere de fișiere care joacă un rol în identificarea și redarea din nou a obiectului.

**Spațiu liber pentru obiecte**: Această secțiune este opțională pentru toți utilizatorii

**Al doilea antet**: o copie a secțiunii antetului fișierului către sfârșitul fișierului DWG

## Referințe ##

* [Specificații de format de fișier DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Specificația fișierului DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - După Wikipedia](https://en.wikipedia.org/wiki/.dwg)

