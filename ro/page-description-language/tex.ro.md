{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier TEX",
  "description":"Aflați despre formatul de fișier TEX și despre API-urile care pot crea și deschide fișiere TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier TEX? ##

**TeX** este un limbaj care cuprinde programare, precum și funcții de marcare, utilizate pentru a tipări documente. Donald Knuth de la Universitatea Stanford, este creatorul acestui sistem de tipărire plin de resurse. În întreaga lume, TeX este alegerea supremă a autorilor și a editorilor pentru a produce documente tehnice de înaltă calitate. TeX efectuează o muncă remarcabilă de formatare a expresiilor matematice complexe. Împreună cu un fotocompozitor de înaltă calitate, TeX concurează cu rezultatele generate de cele mai bune sisteme tradiționale de tipărire. Prin urmare, sunt considerate cele mai clasice sisteme tipografice digitale.

Fișierele de intrare TeX se bazează pe codul ASCII, permițând astfel partajarea manuscriselor între scriitori, manageri de publicații și critici. O mare varietate de medii de calcul, aproape fiecare platformă modernă și multe platforme mai vechi acceptă TeX. Mai mult, TeX este un software gratuit, disponibil pentru o gamă largă de consumatori. Multe instalări UNIX folosesc atât UNIX troff, cât și TeX ca sistem de formatare pentru diferite scopuri. Alte sarcini de tipare sunt realizate extraordinar sub formă de pachete LaTeX, ConTeXt și alte macro-pachete.

## Scurt istoric ##

TeX a fost proiectat și scris de Donald Knuth în 1978. Guy Steele de la Massachusetts Institute of Technology a revizuit intrarea/ieșirea TeX pentru a-l face să ruleze sub sistemul de operare incompatibil, cum ar fi Timesharing System (ITS). Prima versiune de TeX a fost dezvoltată sub sistemul de operare WAITS de la Stanford în limbajul de programare (SAIL) și testată pentru a rula pe un PDP-10. Knuth a introdus ideea de programare alfabetizată pentru versiunile avansate. Programarea alfabetizată este o modalitate de a genera cod sursă compilabil și tipărire (în TeX) pentru documentația încrucișată folosind fișierul original. Limbajul folosit pentru dezvoltarea acestor versiuni avansate de TeX se numește WEB, un amestec de programe DEC PDP-10 Pascal pentru a asigura portabilitatea.

O nouă versiune revizuită a TeX publicată în 1982 și a fost numită TeX82. Schimbarea majoră este înlocuirea algoritmului inițial de separare cu silabe cu algoritmul nou scris de Frank Liang. Pentru a asigura portabilitatea pe diferite platforme, în loc să folosească virgulă mobilă, TeX82 utilizează aritmetica în virgulă fixă împreună cu un limbaj de programare real, complet turing. În 1989, a fost lansată o nouă versiune de TeX și Metafont. Deci, versiunea 3.0 a TeX facilitează intrările pe 8 biți, permițând 256 de caractere diferite în text. După versiunea 3, actualizările sunt notate prin adăugarea unei cifre suplimentare la sfârșitul zecimalei, de exemplu, versiunea curentă a TeX este indicată ca 3.14159265. Această versiune a fost actualizată ultima dată 12-1-2014.

## Intrare TeX ##

Un fișier de intrare în TEX poate fi pregătit cu un editor de text folosind text obișnuit. Spre deosebire de un procesor de text tipic, acest fișier de intrare nu permite orice caracter de control invizibil. Un fișier poate fi încorporat într-un alt fișier, care conține definiții macro și definiții auxiliare care îmbunătățesc capacitățile TeX. Dacă o instalare TeX vine cu orice fișiere macro, informațiile locale despre TeX demonstrează despre utilizarea fișierelor macro. Forma standard de TeX, integrează o combinație de macrocomenzi și alte definiții cunoscute sub numele de TEX simplu.

Pe baza cunoașterii precise a dimensiunilor tuturor caracterelor și simbolurilor, calculează organizarea optimă a literelor pe linie și a liniilor pe pagină. În momentul procesării documentului, este produs un fișier .dvi, unde „dvi” înseamnă „device independent”. Programele de driver de dispozitiv sunt necesare pentru imprimarea sau previzualizarea documentului cu extensia dvi. În zilele noastre, generarea dvi este ocolită de un pdf-TeX folosit în mod obișnuit. Nu sunt disponibile cunoștințe anterioare despre fonturi în cadrul instalării TeX, astfel încât fișierele externe de font, care fac parte din mediul local TeX, sunt folosite pentru a obține informații pentru document.

## Sistem de compunere ##

Aproximativ 300 de primitive (comenzi) pot fi înțelese de sistemul de bază TeX. Primitivele sunt comenzi de nivel scăzut, prin urmare un utilizator obișnuit le folosea rar în mod direct și majoritatea funcționalității este realizată de fișierele de format. Aceste fișiere de format sunt imagini de memorie preîncărcate ale TeX, care sunt urmate de încărcarea colecțiilor mari de macro-uri. Formatul original implicit al limbii, adică TeX simplu, adaugă aproximativ 600 de comenzi.

O bară oblică inversă grupată cu acolade indică începutul comenzilor TeX. Deoarece TeX este un limbaj bazat pe macro și token, aproape toate caracteristicile sintactice ale TeX pot fi modificate în timpul rulării, inclusiv cele definite de utilizator, cu excepția token-urilor neextensibile care sunt apoi executate. Expansiunea în sine este practic fără probleme. Unele comenzi trebuie să vină după un argument care ajută la explicarea funcției unei comenzi. De exemplu, comanda \vskip îi direcționează pe TEX să sară în jos/în sus pe pagină, urmat de un argument care determină cât spațiu să omite.

## Versiunile ##

LaTeX este formatul cel mai des folosit, care a fost dezvoltat inițial de Leslie Lamport. LaTeX integrează diferite stiluri de documente pentru fișiere, litere, cărți și diapozitive și oferă referințe și numerotare automată pentru diferite secțiuni și expresii matematice. AMS-TeX este un alt format popular, dezvoltat de Societatea Americană de Matematică.

AMS-TeX oferă comenzi mult mai ușor de utilizat, care pot fi redefinite de jurnale pentru a se potrivi cu stilul lor local. LaTeX poate beneficia de avantajele AMS-TeX folosind „pachetele” AMS, care sunt apoi denumite AMS-LaTeX. ConTeXt este un alt format scris de Hans Hagen folosit în principal pentru desktop publishing.

Software-ul TeX oferă mai multe caracteristici care erau indisponibile sau de calitate inferioară în alte sisteme de tipărire la momentul creării sale. Unele dintre caracteristicile inovatoare ale acestui limbaj se bazează pe algoritmi interesanți derivați din tezele studenților lui Knuth. În timp ce alte programe de tipărire încorporează acum caracteristici utile ale TeX în programele lor.

## Referințe ##

* [Sistem de compunere TeX](https://en.wikipedia.org/wiki/TeX)

