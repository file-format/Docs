{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier CGM",
  "description":"Aflați despre formatul de fișier CGM și despre API-urile care pot crea și deschide fișiere CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier CGM? ##

Computer Graphics Metafile (CGM) este un format de metafișier standard internațional gratuit, independent de platformă, pentru stocarea și schimbul de grafică vectorială (2D), grafică raster și text. CGM folosește o abordare orientată pe obiect și multe prevederi de funcție pentru producția de imagini. CGM folosește aceste caracteristici orientate pe obiecte pentru remodelarea elementelor grafice pentru a reda o imagine. Un metafișier conține informații necesare care definesc alte fișiere. În CGM, un fișier sursă bazat pe text conține toate elementele grafice care pot fi compilate ulterior într-un fișier binar. Practic, CGM este o modalitate de a facilita schimbul de date grafice 2D, independent de orice platformă sau dispozitiv anume.

Formatul CGM oferă diferite elemente pentru a îndeplini funcții și semnifică obiecte pentru a ajusta primitivele geometrice și informațiile grafice. Deși CGM a fost înlocuit de alte formate pentru a afișa arte grafice pe paginile web, deoarece nu este bine susținut de paginile web, încă foarte popular printre aplicațiile industriale, aeronautice și alte aplicații tehnice. Deși World Wide Web Consortium a dezvoltat WebCGM, o abordare alternativă pentru utilizarea CGM pe Web. Implementarea CGM primară a fost o ilustrare a secvenței de operații de bază ale sistemului Graphical Kernel System (GKS). Nu a fost foarte mult adoptat în design-urile profesionale, dar a fost înlocuit în mare măsură de alte formate, cum ar fi DXF și SVG.

## Istorie ##

CGM s-a dovedit a fi un standard internațional în 1987 (ISO 8632-1987) și a fost, de asemenea, adoptat ca standard național în Marea Britanie de către BSI și în SUA de către ANSI. După o serie de modificări în 1991, un standard revizuit de CGM a fost lansat în 1992 (ISO 8632:1992). În 2001, World Wide Web Consortium a dezvoltat WebCGM cu o capacitate îmbunătățită de a fi utilizat cu paginile web. În 2007 a fost lansată a doua versiune a WebCGM, iar cea de-a treia versiune a fost lansată în 2010, cu capabilități îmbunătățite.

## Format fișier CGM ##

Metafișierele de grafică computerizată sunt în principiu baze de date pentru informații grafice și oferă mijloacele pentru capturarea, stocarea și transmiterea datelor grafice. În consecință, trebuie să existe o componentă de sistem grafic pentru crearea bazei de date simultan cu execuția unei aplicații în format metafișier. În cele mai multe cazuri, această componentă este generatorul de metafile. În plus, este nevoie de o altă componentă care să poată prelua, interpreta și reda date grafice într-un metafișier. Această nevoie este îndeplinită de prezența unui interpret de metafișier. Următoarea figură reprezintă mediul de lucru grafic al metafișierului.

Relația CGM cu alte componente ale unui sistem grafic tipic este ilustrată în figura de mai sus. De asemenea, este evident din figură că funcționalitatea metafișierului nu depinde de rezultatul final al dispozitivului.

În general, există două categorii de metafișier: **captura de secțiune** și **captura de imagine**. Funcționalitatea principală a metafișierului de captare a imaginii este capturarea de definiții multiple de imagini independente de dispozitiv. În timp ce metafișierele de capturare a sesiunii folosesc interfața de sistem pentru a captura dialogul de ieșire într-un sistem grafic. CGM aparține categoriei de metafișiere de captare a imaginilor statice. CGM oferă o aranjare bine organizată a componentelor cu o structură pe două niveluri.

1. Descriptor de metafișier
1. Un grup de imagini logic independente

Fiecare imagine este o colecție de descriptori de imagine și un corp de imagine care include o definiție a imaginii. descriptorul de metafișier definește informații descriptive care se aplică în mod egal tuturor imaginilor acelui metafișier. Aceste informații ajută interpretul să analizeze corect un metafișier și să recunoască resursele necesare pentru redarea corectă a unei imagini. Deși descriptorul de imagine include și informațiile descriptive, el poate recunoaște doar imaginea în care se află descriptorul. În acest format de fișier, fiecare definiție a imaginii este autonomă și suverană din punct de vedere logic. Ele sunt independente de toate celelalte definiții de imagine dintr-un fișier. Imediat după interpretarea meta-descriptorului, imaginile pot fi accesate și interpretate aleatoriu. Schimbarea stării imaginilor anterioare nu are niciun efect asupra succesorilor lor. Această independență a imaginii este o altă caracteristică proeminentă a CGM. CGM constă în spațiu de coordonate care sunt coordonate carteziene 2D numite coordonate dispozitiv virtual și pot fi reprezentate prin număr sau precizie reprezentând intervalul și granularitatea. CGM specifică atât selecția directă a culorilor, cât și selecția bazată pe index. În primul, specificatorul de culoare constă dintr-un triplu RGB, în timp ce mai târziu, specificatorul de culoare indică un index într-un tabel de culori.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
