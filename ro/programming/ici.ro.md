{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "fișier", "extensie", "format fișier", "implementare ICI", "Ghid de programare", "exemplu ici", "limbaj de programare ICI", "module ale ICI", "model de date al ICI ", "documentația ICI", "limba ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI – Fișier limbaj de programare",
  "description":"Aflați despre formatul de fișier ICI și despre API-urile care pot crea și deschide fișiere ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Ce este un fișier ICI?

Un limbaj de programare de uz general, care este interpretat și conține mai multe caracteristici, cum ar fi tastarea dinamică, împreună cu tipurile de date flexibile, este cunoscut sub numele de limbaj de programare ICI (nu un acronim). Este considerat a fi similar cu limbajul [Perl](/ro/programming/pl/). Acest limbaj ICI cuprinde constructe de control al fluxului și, de asemenea, conține unii operatori ai limbajului C. Nu este un limbaj orientat pe obiecte, dar unele dintre caracteristicile OOP pot fi atinse printr-o metodă specifică de moștenire cunoscută sub numele de suprastructuri. Similar cu [C](/ro/programming/c), acest limbaj de programare ICI are aceeași interfață de sistem și o bibliotecă standard pentru funcții încorporate.


## Scurt istoric ##

La sfârșitul anilor 1980, a fost dezvoltat de Tim Long ca un limbaj de programare interpretat de uz general. Cele mai multe dintre caracteristicile acestui limbaj sunt similare cu C și, de asemenea, poate realiza unele dintre caracteristici prin aplicarea unor metode speciale. Această limbă este deținută ca domeniu public și este disponibilă ca limbă revânzabilă și nimeni nu este obligat să menționeze de unde a obținut codul sursă. Documentația ICI se află sub dreptul de autor al Canon Information System Research Australia.

## Specificatii tehnice ##

Există două tipuri diferite de date utilizate în această limbă. Aceste două sunt tipuri de date primitive și agregate. Ambele includ expresii diferite în funcție de compoziția lor predefinită în limbă. Diferite module, cum ar fi imbricate și subrutine, sunt acceptate de acest limbaj. Deoarece unele dintre proprietățile sale sunt similare cu Perl, acesta are o integrare strictă cu expresiile regulate.

Seturile sunt limitate să fie eterogene și imbricate. Aceste seturi oferă suport pentru operațiunile de seturi utilizate în mod obișnuit, cum ar fi Unirea și Intersecția etc. Este folosit în mare parte ca limbaj de dragul implementării de bază pentru aplicațiile deținute de organizații multinaționale.

Aproape toate tipurile de programe pot fi scrise în acest limbaj și în mare parte programele specifice care implică structuri complexe de date sunt scrise în limbajul de programare ICI. Aplicațiile pot implica implementarea ICI într-un mod în care ar trebui să fie scrise în ea. Porțiunile funcționale ale aplicației pot fi implementate de modulele ICI. Limbajul ICI seamănă oarecum cu limbajul C, dar modelul de date al ICI este un nivel destul de superior și diferit cu tipuri precum dicționare (struct), seturi, matrice dinamice, expresii regulate și șiruri (reale).


## Exemplu de format de fișier ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referință ##

* [Limbajul de programare ICI](http://atrn.org/ici/doc/ici.html)



