{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "fișier", "extensie", "format fișier", "Excel", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a ști ce este un fișier XLS și API-urile care le pot crea și deschide.",
  "title" :"Ce este formatul de fișier XLS? Aflați de la experții în format de fișiere!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Ce este un fișier XLS?

Fișierele cu extensia XLS reprezintă Excel Binary File Format. Astfel de fișiere pot fi create de Microsoft Excel, precum și de alte programe de calcul similare, cum ar fi OpenOffice Calc sau Apple Numbers. Fișierul salvat de Excel este cunoscut ca Workbook, unde fiecare registru de lucru poate avea una sau mai multe foi de lucru. Datele sunt stocate și afișate utilizatorilor în format tabel în foaia de lucru și pot cuprinde valori numerice, date text, formule, conexiuni de date externe, imagini și diagrame. Aplicații precum Microsoft Excel vă permit să exportați datele din registrul de lucru în mai multe formate diferite, inclusiv [PDF](/ro/pdf/), [CSV](/ro/spreadsheet/csv/), [XLSX](/ro/spreadsheet/xlsx/), [TXT](/ro/word-processing/txt/), [HTML](/ro/web/html/), [XPS](/ro/page-description-language/xps/) și multe altele. Formatul de fișier XLS a fost înlocuit cu un format mai deschis și mai structurat, XLSX, odată cu lansarea Microsoft Excel 2007. Cele mai recente versiuni încă oferă suport pentru crearea și citirea fișierelor XLS, deși XLSX este prima alegere de utilizare acum.

## Scurt istoric

XLS a fost creat de Microsoft pentru a fi utilizat cu Microsoft Excel și este cunoscut și sub numele de Binary Interchange File Format (BIFF). Acest tip de fișier a fost introdus pentru prima dată făcându-l parte din Excel pentru Windows în 1987. Specificațiile formatului de fișier XLS au fost făcute publice pentru prima dată în iunie 2008 ca Revizia 1. După aceea, specificațiile au fost actualizate continuu și cea mai recentă revizuire disponibilă este din august 2018 care este marcat ca Revizie 8.0. Un scurt istoric al diferitelor versiuni ale formatului de fișier XLS este următorul:

* Versiunea 7.0 (lansată cu Office 95): Această versiune de Excel a fost cea mai robustă și mai rapidă dintre toate versiunile, iar rescrierile interne ale fluxului au fost actualizate la 32 de biți.
* Versiunea 8 (lansată cu Office 97): VBA a fost introdus ca limbaj standard și etichetele în limbaj natural eliminate au fost încorporate în această versiune pentru prima dată. De asemenea, a introdus pentru prima dată un asistent de birou pentru agrafe.
* Versiunea 9 (Lansată cu Office 2000): Au existat doar modificări minore în Versiunea 9, în care asistentul de birou agrafă putea ține simultan mai multe obiecte care nu erau posibile anterior.
* Versiunea 10 (lansată cu Office XP): Această versiune nu conținea nicio îmbunătățire vizibilă.
* Versiunea 11 (lansată cu Office 2003): Actualizare majoră în versiunea 11, Excel 2003 a fost introducerea de noi tabele.

## Specificații pentru formatul fișierului XLS ##

Datele sunt aranjate într-un fișier XLS ca fluxuri binare sub forma unui fișier compus așa cum este descris în [MS-CFB]. Datele sunt stocate în fișierul compus folosind stocări, fluxuri și substreamuri care conțin informații despre conținutul și structura unui registru de lucru, inclusiv date din registru de lucru, cum ar fi definițiile foilor de lucru. Fiecare flux sau substream conține o serie de înregistrări binare. Fiecare înregistrare binară conține zero sau mai multe câmpuri structurate care conțin datele din registrul de lucru. Această secțiune oferă o scurtă prezentare generală a structurii fișierelor XLS, dar pentru specificații detaliate despre formatul fișierului, trebuie să consultați [Specificațiile de formare a fișierelor XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office). .12).aspx) document de la Microsoft.

#### Flux și substream ####

Un registru de lucru este reprezentat de fluxul registrului de lucru. Fiecare foaie de lucru dintr-un registru de lucru este reprezentată de Substreams. În plus, are un subflux al foii de diagramă, un subflux al foii macro sau un subflux al foii de dialog care urmează subfluxului global. Fiecare flux binar sau substream care conține date din registrul de lucru TREBUIE să fie scris ca o serie de înregistrări binare.

#### Record ####

Informațiile despre caracteristicile dintr-un registru de lucru sunt stocate ca o înregistrare care este o secvență de octeți cu lungime variabilă. O înregistrare binară constă din următoarele trei componente:

**Tipul de înregistrare:** Tipul de înregistrare este un întreg fără semn de doi octeți care specifică ce tip de informații este specificat de înregistrare și cum este ordonată și structurată structura datelor de înregistrare specifice acestei înregistrări. Valorile tipului de înregistrare TREBUIE să fie o valoare din Enumerarea înregistrărilor (secțiunea 2.3) sau înregistrarea TREBUIE să utilizeze arhitectura viitoare a înregistrărilor (secțiunea 2.1.6).

**Dimensiunea înregistrării**: dimensiunea înregistrării este un număr întreg fără semn de doi octeți care specifică numărul de octeți care specifică dimensiunea totală a datelor înregistrării. Mărimea înregistrării TREBUIE să fie mai mare sau egală cu 0 și TREBUIE să fie mai mică sau egală cu 8224.

**Date de înregistrare:** Componenta de date de înregistrare conține câmpuri care corespund unui anumit tip de înregistrare și cuprind restul înregistrării. Ordinea și structura câmpurilor pentru un anumit tip de înregistrare sunt specificate în secțiunea corespunzătoare pentru acel tip de înregistrare. Dimensiunea componentei de date de înregistrare TREBUIE să fie egală cu dimensiunea înregistrării. Câmpurile din componenta de date de înregistrare pot conține valori simple, matrice de valori, structuri ale mai multor câmpuri, matrice de câmpuri și matrice de structuri.

#### Tabel de celule ####

Celulele sunt blocurile fundamentale ale unui registru de lucru care stochează conținutul registrului de lucru, cum ar fi text, formule și date numerice. Celulele mențin înregistrarea datelor stocate printr-o structură de date numită Cell Table. Tabelul de celule în sine este stocat în secvența de înregistrări care se conformează regulilor CELLTABLE definite în documentul de specificații. Este format dintr-o serie de blocuri de rând în care rândurile sunt aranjate în blocuri de rând. Fiecare bloc de rânduri conține rânduri de la primul rând care conține date până la ultimul rând care conține date.

Formatarea datelor sau a rândurilor este salvată într-o înregistrare Rând pentru fiecare bloc de rând. Fiecare celulă care conține date sau formatare individuală a celulei este reprezentată de o înregistrare. Formatarea asociată cu o celulă poate fi derivată din formatarea celulei individuale, formatarea rândurilor, formatarea coloanelor sau formatul implicit al celulei. Ordinea de prioritate pentru formatare este formatarea celulelor individuale cu cea mai mare prioritate, urmată de formatarea rândurilor, apoi formatarea coloanei și apoi formatul implicit al celulei. Celulele care nu conțin date și nu conțin formatare individuală nu sunt salvate.

#### Formule ####

O formulă este o secvență de valori, referințe de celule, nume, funcții sau operatori dintr-o celulă care împreună produc o nouă valoare. Formulele sunt stocate într-o reprezentare tokenizată cunoscută sub numele de „expresii analizate”. O expresie analizată este convertită într-o formulă textuală în timpul rulării pentru afișare și editare de utilizator. Formulele celulelor sunt specificate de înregistrarea Formulă. Formulele matrice sunt specificate de înregistrarea Array. Formulele partajate sunt specificate de înregistrarea ShrFmla.

#### Grafice ####

Foaia de diagramă specifică o diagramă, un grafic care afișează date sau relațiile dintre seturi de date într-o formă vizuală și o memorie cache a datelor diagramei, o copie locală a datelor care sunt utilizate în datele diagramei lipsește sau dacă există linkuri către sursele de date sunt sparte. Graficul specifică grupuri de una sau două axe, un set de axe pe care sunt trasate datele din diagramă și setul de serii, linii de tendință și bară de eroare specificate în diagramă. Fiecare grup de axe specifică unul până la patru grupuri de diagrame care specifică tipul de vizualizare utilizat pentru afișarea datelor. Fiecare serie, linie de tendință și bară de eroare specifică un grup de diagrame cu care este asociat.

#### Metadate ####

Metadatele sunt date suplimentare asociate cu o anumită celulă sau cu conținutul acesteia. Metadatele sunt înregistrate în BIFF8 numai în scopuri de extensibilitate viitoare.

#### Tabele pivot ####

Un PivotTable este un mecanism pentru rezumarea datelor sursă pentru a obține o imagine de ansamblu asupra distribuției acestor date. Într-un tabel pivot, coloanele aplicabile ale datelor sursă devin câmpuri care pot fi folosite pentru a rezuma datele. Când datele sursă ale tabelului pivot sunt date sursă OLAP, ierarhiile OLAP și alte entități OLAP devin câmpuri în tabelul pivot.
Un PivotTable are două părți majore, un PivotCache și o vizualizare PivotTable. Pot exista mai multe vizualizări PivotTable bazate pe un singur PivotCache non-OLAP.

#### Stiluri ####

Această prezentare generală descrie modul în care sunt specificate informațiile de formatare și protecție pentru celulele dintr-o foaie (1). Formatarea celulelor este compusă din mai multe seturi de proprietăți:

* Proprietățile fontului (bold, italic, culoarea fontului, dimensiunea fontului etc...)
* Proprietăți de umplere (culoare prim-plan, culoare de fundal, model, gradient etc...)
* Proprietăți de aliniere (aliniere stânga, centru, dreapta etc...)
* Proprietăți chenar (stânga, dreapta, sus, jos, gros sau subțire, culoare etc...)
* Proprietăți de formatare a numărului (data, ora, numărul de zecimale etc...)
* Proprietăți de protecție (blocat, ascuns, etc...)

Aceste proprietăți, în ansamblu, descriu modul în care o anumită celulă este afișată și tipărită.

## Referințe ##

* [[MS-XLS] - Structura formatului fișierului binar Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Format de fișier binar al fișierului compus](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

