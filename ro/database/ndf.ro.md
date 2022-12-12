{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MDF și despre API-urile care pot crea și deschide fișiere NDF.",
  "title" :"Format fișier NDF - Fișier bază de date master SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier NDF?

Un fișier cu extensia .ndf este un fișier de bază de date secundar utilizat de [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) pentru a stoca datele utilizatorului. NDF este un fișier de stocare secundar, deoarece serverul SQL stochează datele specificate de utilizator în fișierul de stocare primar cunoscut sub numele de [MDF](/ro/database/mdf/). Fișierul de date NDF este opțional și este definit de utilizator pentru a gestiona stocarea datelor în cazul în care fișierul MDF principal utilizează tot spațiul alocat. De obicei, este stocat pe un disc separat și se poate răspândi pe mai multe dispozitive de stocare. Prezența fișierelor MDF este necesară pentru a deschide fișierele NDF.

## Format de fișier NDF

Formatul de fișier NDF nu este diferit de [MDF](/ro/database/mdf) și folosește paginile ca unitate fundamentală de stocare a datelor. fiecare pagină începe cu antet de 96 de octeți care include:

* ID-ul paginii
* Tip de structură
* Numărul de înregistrări din pagini
* Indicatori către paginile anterioare și următoare

### Structura fișierului NDF

Un fișier MDF are următoarea structură de date.

* Pagina 0: Antet
* Pagina 1: Primul PFS
* Pagina 2: Primul GAM
* Pagina 3: Primul SGAM
* Pagina 4: nefolosit
* Pagina 5: nefolosit
* Pagina 6: Primul DCM
* Pagina 7: Primul BCM

#### Antet fișier NDF

Pagina cu numărul 0 al tuturor fișierelor conține un antet care stochează metadate despre fișier.

#### Spațiu liber în pagină (PFS)
PFS identifică starea de alocare și determină cantitatea de spațiu liber.

* Bit 1: indică dacă pagina este alocată sau nu.
* Bit 2: indică dacă pagina este dintr-o măsură mixtă.
* Bit 3: Indică faptul că această pagină este o pagină IAM.
* Bit 4: Indică faptul că această pagină conține înregistrări fantomă
* Biți de la 5 la 7: o valoare combinată de trei biți, care indică caracterul complet al paginii, după cum urmează:
* 0: Pagina este goală
* 1: Pagina este plină cu 1–50%.
* 2: Pagina este plină cu 51–80%.
* 3: Pagina este plină în proporție de 81–95%.
* 4: Pagina este plină 96–100%.

## Pagina Fișier de date

Paginile dintr-un fișier de date SQL Server încep de la zero (0) și cresc secvențial. Fiecare fișier este recunoscut printr-un număr unic de identificare a fișierului. Perechea ID-ul fișierului și numărul paginii identifică în mod unic o pagină dintr-o bază de date. Un exemplu care arată numerele paginilor dintr-o bază de date este ca în imaginea următoare.

{{< figure src="../ndf.png" alt="Formatul fișierului bazei de date NDF" >}}

Acest exemplu arată numerele de pagină dintr-o bază de date care are un fișier de date primar de 4 MB și un fișier de date secundar de 1 MB.

## Referințe

* [Fișiere și grupuri de fișiere baze de date](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Detașarea și atașarea bazei de date - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analizarea anatomiei fișierelor de date SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

