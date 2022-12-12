{
  "date" : "2020-03-16",
  "keywords" :[ "Fișier IGES", "Format fișier", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier IGES și despre API-urile care pot crea și deschide fișiere IGES.",
  "title" :"Format fișier IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Ce este un fișier IGES?

Un fișier cu extensia .iges este utilizat pentru a face schimb de informații de proiectare între aplicațiile de proiectare asistată de computer (CAD). IGES înseamnă Initial Graphics Exchange Specifications. Informațiile schimbate folosind IGES includ diagrame de circuit, cadru fir, suprafață cu formă liberă sau reprezentări de modelare solidă. IGES își găsește aplicațiile în desenele de inginerie tradiționale, analiza modelelor și funcțiile de producție. Formatul poate schimba atât informații de design 2D, cât și 3D între programele CAD. Fișierele IGES pot fi deschise cu mai multe aplicații CAD, cum ar fi Autodesk și CADSoftTools ABViewer. Există, de asemenea, mai multe API-uri disponibile pentru a deschide și a converti fișierele IGES în mod programatic.

## Format de fișier IGES

Fișierele IGES sunt în format text ASCII și pot fi deschise în orice editor de text pentru a vizualiza conținutul fișierului. Informațiile textuale dintr-un fișier IGES sunt reprezentate în format „Hollerith”. Un fișier IGES obișnuit poate conține mii de linii pentru a reprezenta informațiile 2D sau 3D care pot fi schimbate conform acestui format. Un fișier IGES este împărțit în cinci secțiuni, notate cu litera majusculă specifică în coloana a 73-a. Aceste secțiuni sunt secțiunile „Start” (S), „Global” (G), „Intrare date” (D), „Date parametri” (P) și „Terminare” (T). Secțiunile Introducere date și Date parametri sunt abreviate în mod obișnuit DE și, respectiv, PD.

### Antet fișier IGES

Secțiunile Start și Global conțin informații de bază despre:
* Numele fișierului și sursa acestuia
* Delimitatori pentru secțiunea Date parametri
* Autorul fișierului și alte informații generale.

Secțiunile Start și Global din documentul exemplu de pe Wikipedia sunt după cum urmează.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
După cum se poate vedea, câmpul de început conține descrieri ale fișierului care pot fi citite de om și am orice caractere în coloanele 1-72, cu linia care se termină cu antetul secțiunii și numărul rândului secțiunii. Trebuie să existe cel puțin o linie a secțiunii Start. Secțiunea globală conține date de preprocesor. De asemenea, trebuie să fie prezent în fișier și să se termine cu formatul G000000#.

### Secțiunea Introducere date (DE) și Date parametri (PD).

#### Secțiunea de introducere a datelor
Un fișier IGES este format din mai multe entități care conține informații despre datele de bază ale formatului de fișier IGES. O entitate conține informații despre diferite elemente ale unui format de date IGES și este utilizată pentru desen. Entitățile mai frecvent utilizate includ:
* Arc circular
* Curba compozită
* Arc conic
* Avionul
* Linie

Acestea sunt doar câteva și există aproximativ 150 de entități diferite în IGES. Fiecare entitate este identificată printr-un număr de tip, cum ar fi:
* ARC CIRCULAR (Tip 100)
* LINE (Tip 110)

##### Proprietăți entități

Fiecare entitate declarată are următoarele proprietăți.

|Nume câmp|Descriere|
---|---|
|Tip de entitate |Acesta este tipul de entitate descris. De exemplu, 116 descrie o entitate Punct.|
|Pocker PD |Acesta oferă locația pentru datele acestei entități în secțiunea Date parametri. Această locație este pur și simplu numărul liniei din interiorul secțiunii PD care are prima linie a datelor acestei entități.|
|Structură |Zero sau indicator către entitate de definiție. Nu se aplică pentru majoritatea entităților|
|Model de font de linie| Număr sau indicator către entitatea model de font de linie. Numărul înseamnă: * 0 Nici un model specificat (implicit) * 1 Solid * 2 Punct * 3 Fantomă * 4 Linie centrală * 5 Punct|
|Nivel| Specifică nivelurile care urmează să fie asociate cu această entitate. Permite entității să apară la mai multe niveluri|
|Vizualizare| Specifică opțiunile de vizualizare. Acestea sunt: 0 Indică vizibilitate și caracteristici egale în toate vizualizările. Indicator implicit către entitatea Vizualizare (Tip 410) pe care poate fi vizualizată din Referință la o entitate Vizualizare Asociativitate Vizibilă (Tip 402, Formular 3)
|Poner de matrice de transformare| Face referire la o entitate matrice de transformare (Tipul 124) sau este zero în mod implicit (fără transformare)|
|Asociativitatea afișajului etichetei| Face referire la o asociativitate de afișare a etichetei (Tip 402, Formular 5) care definește modul în care apare eticheta entității.|
|Număr de stare| Conține patru secțiuni a două numere. 1-2: Stare gol. Fie 00 pentru normal, fie 01 pentru gol. 3-4: Comutare entitate subordonată: este 00 pentru independent, 01 pentru dependent fizic, 02 pentru dependent logic și 03 pentru ambele. 5-6: Indicatorul de utilizare a entității: este fie 00 pentru Geometrie, 01 pentru adnotare, 02 pentru definiție, 03 pentru Altele, 04 pentru logic, 05 pentru parametri 2D și 06 pentru Geometria construcției. În cele din urmă, 7-8 este ierarhia, unde 00 indică global de sus în jos (utilizați caracteristicile acestei entități), 01 este global defer (nu utilizați caracteristicile acestei entități), iar 02 este folosiți proprietatea ierarhiei (utilizați Entitatea Hierarchy (Tip 406, Formular) 10)să determine caracteristicile grupării ierarhice).|
|Numărul secvenței| Specificat de D#, unde # este numărul liniei pentru această secțiune (nu din partea de sus a fișierului). Acesta este, de asemenea, folosit pentru a indica această entitate de introducere a datelor.|
|Tip de entitate| este specificat de două ori pe lista de entitate|
|Număr de greutate liniei| Specifică grosimea la afișarea entității. Cel mai mic este 1, 0 este implicit|
|Număr de culoare| Specifică culoarea entității. Valorile întregi permise sunt: 0 Fără culoare (implicit) 1 Negru 2 Roșu 3 Verde 4 Albastru 5 Galben 6 Magenta 7 Cyan 8 Alb|
|Numărul numărului de linii parametru| Specifică numărul de linii pe care această entitate ocupă în secțiunea Date parametri|
|Numărul formularului| Indică forma sau reprezentarea acestei entități. Modifică modul în care sunt interpretate datele parametrilor. Implicit este 0|
|Câmp rezervat| Nefolosit|
|Câmp rezervat| Nefolosit|
|Etichetă de entitate| Aplicația specificată identificator- dreapta justificată|
|Numărul indicelui| Calificator numeric pentru eticheta entității. Ambele formează împreună un identificator unic pentru entitate|
|Numărul secvenței Vezi mai sus. |Acesta va fi D#+1, deoarece fiecare entitate este specificată pe două rânduri.|

#### Secțiunea de date parametri
Secțiunea Intrări de date este urmată de secțiunea Date parametri. Listează datele pentru fiecare intrare respectivă și listează parametrii pentru entitate pe baza delimitatorilor specificați în secțiunea Global (de obicei virgule pentru a separa parametrii și un punct și virgulă pentru a încheia listarea).


## Referințe
* [IGES de la WikiPedia](https://en.wikipedia.org/wiki/IGES)

