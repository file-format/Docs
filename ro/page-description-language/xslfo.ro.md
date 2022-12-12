{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Obiecte de formatare XSL", "Fișier", "Extensie", "Format fișier", "Limbaj extensibil al foii de stil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Aflați despre formatul de fișier XSLFO și despre API-urile care pot crea și deschide fișiere XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier XSL-FO? ##

XSL-FO (XSL Formatting Objects) este un limbaj puternic pentru foi de stil pentru formatarea documentelor XML. Semantica formei mărginite de hârtie și imprimare este exprimată prin XSL-FO atunci când dimensiunile sunt fixe. Spre deosebire de HTML, care reprezintă semantica formei nelimitate a unei ferestre de browser cu dimensiuni variabile. Documentele XML formatate de XSL-FO sunt utilizate în principal pentru a genera fișiere PDF. XSL (Extensible Stylesheet Language) este un set de tehnologii W3C cu caracteristici complete menite să proiecteze pentru formatarea și schimbul de documente XML și XSL-FO parte a acestui limbaj. XSLT și XPath sunt, de asemenea, alte părți ale XSL.

Se propune ca documentele XML să fie mai întâi transformate în XSL-FO, PDF este un exemplu al acestui criteriu. În PDF, rezultatele sunt redate folosind XSLTfirst, apoi formatatorul XSL-FO. În acest mod, documentele XML pot fi formatate aleatoriu. Deși XSL-FO profită de avantajul utilizării proprietăților Cascading Style Sheet (CSS) și extinderea lor oricând este necesar pentru formatul real, găzduiește furnizarea de șabloane de pagină numite page master în terminologia XSL-FO. XSL-FO oferă, de asemenea, formatare pentru documente destul de sofisticate și acceptă generarea de indexuri.

## Istorie și concepte de bază ##

În ianuarie 2012, proiectul de lucru al XSL-FO a fost actualizat ultima dată, iar în noiembrie 2013, grupul său de lucru a fost închis. O foaie de stil XSL specifică prezentarea unei clase de documente XML prin descrierea modului în care o instanță a clasei este transformată într-un document XML care utilizează vocabularul de formatare. XSL-FO este un limbaj de prezentare integrat și nu are markupuri semantice care sunt utilizate în HTML. Mai mult, acest limbaj stochează toate datele documentului în sine, spre deosebire de CSS care modifică setările implicite ale unui document HTML sau XML extern.

Criteriul general de utilizare a XSL-FO este ca utilizatorul să scrie un document într-un limbaj XML, mai degrabă decât să scrie în FO. După aceea, are loc o transformare XSLT. Această transformare XSLT este responsabilă pentru conversia XML în XSL-FO. Imediat ce documentul XSL-FO este generat, acesta este apoi predat unei aplicații numită procesor FO. Procesoarele FO sunt responsabile pentru transformarea acestui document într-un document care poate fi citit, precum și într-un document imprimabil. Fișierele PDF sau PS sunt exemple ale celor mai comune rezultate ale XSL-FO. Dar nu înseamnă că procesorul FO poate produce doar aceste două tipuri de format ca ieșire. Unele procesoare FO pot ieși în fișierele RTF sau chiar poate apărea o fereastră în GUI-ul utilizatorului, această fereastră afișează secvența paginii și conținutul acestora.

Un document XSL-FO este diferit de un PDF sau un PS în sensul că nu definește în cele din urmă aspectul textului pe diferite pagini. Poate că stilează paginile și determină locurile pentru afișarea conținutului. Mai mult, un procesor FO organizează textul în limitele specificate de documentul FO. Această specificație permite chiar și diferitelor procesoare FO să se comporte în mod corespunzător cu paginile create de rezultat. Un exemplu de astfel de comportament este separarea cu silabe, puține procesoare FO pot separa cuvintele pentru a economisi spațiu atunci când o linie se întrerupe, în timp ce unele procesoare nu selectează această opțiune. Depinde de procesoare să aleagă diferiți algoritmi de separare prin silabe care se potrivesc cerințelor lor. Acești algoritmi de separare prin silabe pot fi foarte simpli sau poate mai complexi. În unele situații, specificația XSL-FO sancționează în mod explicit procesoarele FO, un anumit grad de alegere în contextul aspectului.

Această variație între procesoarele FO generează rezultate diferite, despre care procesoarele rămân adesea nepreocupate. Deoarece obiectivul general al XSL-FO este de a produce documente paginate/tipărite. Documentele XSL-FO în sine acționează de obicei ca intermediari, funcția lor principală este de a genera fie fișiere PDF, fie un document care poate fi tipărit ca rezultat care urmează să fie distribuit. În HTML/CSS sau XSL-FO, distribuirea PDF-ului ca rezultat final, mai degrabă decât introducerea limbajului de formatare, indică faptul că receptorii rămân neafectați de versatilitatea rezultată, care este produsă din cauza diferențelor dintre interpreții limbajului de formatare. Pe de altă parte, este evident că nu există o modalitate ușoară, că un document poate îndeplini diferitele nevoi ale destinatarilor, de exemplu dimensiunea variabilă a paginii sau dimensiunea dorită a fontului sau adaptarea pentru pagină sau imprimare.

## Format de fișier XSLFO ##

Documentele SL-FO sunt practic documente XML, dar nu urmează nicio schemă. În locul său, documentele SL-FO urmează sintaxa definită în specificația propriului limbaj. Există două secțiuni necesare în fiecare document XSL-FO:

1. O secțiune care specifică o listă de aspecte de pagină etichetate.
1. O secțiune cu toate detaliile datelor documentului, cu marcaj, care determină afișarea conținutului pe diferite pagini prin diverse machete de pagină.

Proprietățile paginii sunt menționate în aspectul paginii, care poate defini organizarea textului, pentru a respecta convențiile pentru limba specifică. În plus, dimensiunea paginii, marginile acestora și secvențele de pagini (care sancționează diferite proprietăți pentru paginile pare și impare) sunt, de asemenea, definite de aspectul paginii.

Porțiunea de date a documentului este împărțită într-o serie de fluxuri, în care fiecare flux este conectat la un aspect de pagină. Fluxurile includ o listă de blocuri în ele. Această listă de blocuri poate conține caracteristici de marcare inline sau o listă de date text, sau poate ambele în același timp. Marginile documentului pot afișa, de asemenea, numerele paginilor sau titlurile capitolelor. Funcționalitatea ambelor blocuri și elementele inline rămâne aceeași ca în CSS, totuși unele reguli de umplutură și marjă sunt diferite între FO și CSS.

Direcția de orientare a paginii este specificată în întregime pentru extinderea blocurilor și a liniilor, făcând astfel documentele FO să funcționeze în limbi diferite de engleză. Limbajul specificației FO folosește cuvintele început și sfârșit mai degrabă decât stânga și dreapta pentru descrierea direcțiilor. Regulile de bază de marcare a conținutului și de cascadă ale XSL-FO sunt preluate din CSS. Limbajul XSL-FO este de acord cu următoarele specificații.

## Coloane multiple ##

O pagină poate avea mai multe coloane și blocuri și se poate extinde de la o coloană la alta în mod implicit. Mai multe pagini au permisiunea de a avea lățimi și numere diferite de coloane. Toate caracteristicile FO urmează limitele unei pagini cu mai multe coloane.

### Liste ###

O listă XSL-FO este stabilită de două seturi de blocuri aranjate obraz după madă. Conceptual, într-o listă, un bloc din stânga indică un număr, un marcator sau un șir de text, în timp ce blocul din partea dreaptă poate funcționa așa cum era anticipat. Numerotarea listelor XSL-FO se face de obicei de XSLT.

### Mese ###

Un tabel FO este similar cu un tabel HTML/CSS. Utilizatorul poate selecta rândurile de date, informațiile de stil, culoarea de fundal pentru fiecare celulă individuală. Folosind informații de stil distincte, utilizatorul are privilegiul de a selecta primul rând ca rând de antet de tabel. Procesorul FO poate fi informat în mod explicit despre specificația de spațiu a fiecărei coloane sau pentru a se potrivi automat textul din tabel.

### Indexare ###

XSL-FO 1.1 are caracteristici care ajută la generarea unui index prin referirea elementelor marcate corespunzător.

### Beneficii ###

* Potrivit pentru publicarea bazată pe conținut
* Ușurință în utilizare
* Cost scăzut

## Referințe ##

* [Ce este XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Obiecte de formatare XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

