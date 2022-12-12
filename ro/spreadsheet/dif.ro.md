{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "fișier", "extensie", "format fișier", "Fișier de schimb de date", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este o extensie de fișier DIF și API-urile care pot crea și deschide fișiere DIF.",
  "title" :"DIF – Format de fișier de schimb de date",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier DIF?

DIF înseamnă Data Interchange Format care este folosit pentru a importa/exporta date de foi de calcul între diferite aplicații. Acestea includ Microsoft Excel, OpenOffice Calc, StarCalc și multe altele. Stochează datele conținute într-o singură foaie de calcul, care este singura limitare a acestui format de fișier.

## Scurt istoric al formatului de fișier DIF ##

Formatul de fișier DIF a fost dezvoltat de Software Arts, Inc. la începutul anilor 1980. Specificațiile de format de fișier pentru DIF au fost incluse în VisiCalc, care a fost primul program de calcul pentru computere personale. Aceste specificații erau protejate prin drepturi de autor în 1981 și erau marcă înregistrată a Software Arts Products Corp.

## Format fișier DIF ##

DIF stochează conținutul foii de calcul într-un fișier text ASCII care permite vizualizarea și editarea acestuia cu un editor de text. Formatul își deține locul în lista de formate de serializare a datelor pentru caracteristicile sale de schimb de date. Un fișier DIF este format din 2 secțiuni; un antet și date.

Totul în DIF este reprezentat de o bucată de 2 sau 3 linii. Anteturile primesc o bucată de 3 linii; date, 2.

* Bucățile de antet încep cu un identificator de text care este cu majuscule, numai caractere alfabetice și mai puțin de 32 de litere. Următoarea linie trebuie să fie o pereche de numere, iar a treia linie trebuie să fie un șir între ghilimele.
* Bucățile de date încep cu o pereche de numere, iar linia următoare este un șir între ghilimele sau un cuvânt cheie.

### Valori ###

O valoare ocupă două linii, prima o pereche de numere și a doua fie un șir, fie un cuvânt cheie. Primul număr al perechii indică tipul:

* −1 – tip directivă, al doilea număr este ignorat, următoarea linie este unul dintre aceste cuvinte cheie:
** BOT – începutul tuplului (începutul rândului)
** EOD – sfârșitul datelor
* 0 – tip numeric, valoarea este al doilea număr, următoarea linie este unul dintre aceste cuvinte cheie:
** V – valabil
** NA – nu este disponibil
** EROARE – eroare
** TRUE – valoare booleană adevărată
** FALSE – valoare booleană falsă
* 1 – tip șir, al doilea număr este ignorat, următorul rând este șirul între ghilimele duble

### Bucățiune antet DIF ###

Partea antetului unui fișier DIF constă dintr-o linie de identificare urmată de cele două linii ale unei valori. Valorile numerice din bucățile de antet folosesc doar un șir gol în loc de cuvintele cheie de valabilitate. Detaliile acestor porțiuni de antet sunt următoarele.

* TABEL - urmează o valoare numerică a versiunii, a doua linie dezafectată a valorii conține un comentariu generator
* VECTORI - numărul de coloane urmează ca valoare numerică
* TUPLES - numărul de rânduri urmează ca valoare numerică
* DATE - după o valoare numerică inactivă 0 urmează datele pentru tabel, fiecare rând precedat de o valoare BOT, întregul tabel terminat cu o valoare EOD

### Exemplu DIF ###

Următorul exemplu arată conținutul unei foi de lucru simple și reprezentarea ei DIF echivalentă.


|Nume|Vârsta
---|---|
|Bob|34
|Foaie|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referințe ##

* [ DIF - De Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

