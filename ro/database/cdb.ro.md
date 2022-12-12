{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "extensie", "fișier cdb", "format fișier cdb", "Tip fișier bază de date", "Format fișier bază de date", "ce este un fișier cdb"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier CDB și despre API-urile care pot crea și deschide fișiere CDB.",
  "title" :"CDB - Fișier constant de bază de date",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Ce este un fișier CDB?
Fișierele CDB sunt utilizate în aplicații critice, cum ar fi e-mailul. CDB înseamnă „constant database”, un pachet rapid, fiabil și simplu pentru crearea sau citirea bazelor de date constante. Înlocuirea bazei de date este sigură împotriva blocărilor sistemului. Utilizatorii nu trebuie să întrerupă o pauză în timpul unei rescrieri. CDB funcționează ca o matrice asociativă (pe disc), mapând cheile la valori și permite stocarea mai multor valori într-o singură cheie.

## Format de fișier CDB
Formatul de fișier CDB stochează numere, decalaje, lungimi și valori hash în format little endian ca numere întregi nesemnate pe 32 de biți. Cheile și datele sunt considerate a fi șiruri de octeți opace, fără tratament special. La începutul bazei de date, antetul de dimensiune fixă reprezintă 256 de tabele hash, listând poziția lor în fișier și lungimea lor în sloturi. De obicei, datele sunt stocate ca o secvență de înregistrări, fiecare înregistrare stochează lungimea cheii, lungimea datelor, cheia și datele. Nu există reguli de sortare sau aliniere. Înregistrările sunt urmate de un set de 256 de tabele hash de lungimi diferite. Deoarece zero este o lungime validă, pot fi mai puțin de 256 de tabele hash stocate fizic în baza de date, dar nu există nimic considerat a fi 256 de tabele. Tabelele hash constă dintr-o serie de sloturi, fiecare dintre acestea conținând o valoare hash și un offset de înregistrare. „Sloturile goale” au un offset de zero.

### Structura
Baza de date CDB constă dintr-un întreg set de date într-un singur fișier de computer. Acesta conține trei părți:
- Un antet de dimensiune fixă
- Date
- Un set de tabele hash.

Căutările sunt disponibile numai pentru cheile exacte. Căutările acționează folosind următorul algoritm:

- Strânge cheia.
- Stabiliți la ce tabel hash și slot ar trebui să fie localizată această înregistrare.
- Testați slotul indicat în tabelul hash.

Pentru căutări de chei cu mai multe valori, pot fi găsite valori suplimentare prin simpla reluare a căutării la următorul interval.

#### Caracteristici

Structura bazei de date CDB oferă mai multe caracteristici:

##### Căutări rapide
O căutare de succes într-o bază de date imensă necesită în mod normal doar două accesări la disc, iar o căutare nereușită necesită doar una.
##### Ofertă redusă
O bază de date folosește 2048 de octeți, 24 de octeți per înregistrare și spațiul pentru chei și date.
##### Fără limite aleatorii
CDB poate gestiona orice bază de date de până la 4 gigaocteți. Deoarece nu există alte restricții, înregistrările nici nu trebuie să se încadreze în memorie. Bazele de date sunt stocate într-un format independent de mașină.
##### Înlocuire rapidă a bazei de date atomice
Comanda **cdbmake** poate rescrie o întreagă bază de date în două ordine de mărime, mai rapid decât alte pachete de hashing.
##### Dumpări rapide ale bazei de date
**cdbdump** poate tipări conținutul unei baze de date în format compatibil cu cdbmake.


## Referințe ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [Specificație CDB](http://cr.yp.to/cdb.html)

