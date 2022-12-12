{
  "date" : "2021-05-25",
  "keywords" :[ "DML","fișier DML", "format fișier DML", "tip fișier DML", "fișier", "tip", "ce este un fișier DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML – fișier HTML DynaScript",
  "description":"Aflați despre formatul de fișier DML și despre API-urile care pot crea și deschide fișiere DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Ce este un fișier DML?

Un fișier cu extensia .dml este un fișier de cod de pagină de script web creat cu DyanScript. DynaScript este un limbaj de scripting [HTML](/ro/web/html/) dinamic care este compatibil cu ECMAScript și oferă cele mai multe dintre aceleași caracteristici ca și alt limbaj de scripting. Este similar cu codul ColdFusion și codul Microsoft Active Server Pages (ASP). Fișierele DML pot fi deschise și vizualizate în browsere web standard similare cu alte pagini HTML.

## Format de fișier DML

Fișierele DML sunt create în format de fișier text simplu și pot fi deschise cu un editor de text pentru a vizualiza codul. Scrierea codului folosind limbajul de scripting DML poate fi folosită pentru a genera în mod dinamic HTML pe paginile DML găzduite de server. DynaScript-urile sunt construite din următoarele elemente de limbaj:


* Etichetă SCRIPT - Acestea sunt încorporate în documente ca comentarii HTML. Un comentariu HTML este marcat cu \ <!-- tag.
* Literale - Acestea sunt valori fixe în fișierele DynaScript. Exemple dintre acestea includ numere întregi precum s 123 , 0x3F , 0123, numere în virgulă mobilă, cum ar fi 456.789 , 3.2e-8, boolean, cum ar fi adevărat sau fals, și șir precum „Ploaia în Spania”
* Variabile - Variabilele DynaScript nu trebuie definite sau atribuite unui tip de date fix. O variabilă trebuie să aibă o valoare înainte de a o utiliza într-o expresie; în caz contrar, se generează un avertisment de rulare.
* Expresii - Acestea sunt combinații de variabile, valori literale, operatori și alte expresii. Partea dreaptă a unei instrucțiuni de atribuire este o expresie.
* Operatori - Aceștia operează pe una sau mai multe expresii numite operanzi. Aceștia pot fi fie ternari, binari sau unari: operatorii ternari acționează asupra a trei expresii, operatorii binari acționează asupra a două expresii și operatorii unari acționează asupra uneia.
* Declarații - Acestea controlează fluxul de scripturi, manipulează obiecte și programarea generală. În general, aceste instrucțiuni urmează sintaxa standard C și Java. Exemplele sunt bucle if-else, do-while, switch, break, continue etc., ca orice alt limbaj de scripting.
* Funcții - Funcțiile, ca orice alt limbaj de scripting, vă permit să încapsulați un set de instrucțiuni o dată într-un document ca funcție, apoi să îl utilizați de mai multe ori pe tot parcursul documentului (prin apelarea funcției). DynaScript acceptă și funcții.
* Obiecte - DynaScript este orientat pe obiecte și acceptă „obiecte” și conceptele fundamentale orientate pe obiecte de Encapsulare, Polimorfism și Moștenire.

