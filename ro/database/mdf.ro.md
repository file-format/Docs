{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MDF și despre API-urile care pot crea și deschide fișiere MDF.",
  "title" :"Format fișier MDF - Fișier bază de date master SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier MDF?

Un fișier cu extensia .mdf este un fișier de bază de date principal utilizat de [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) pentru a stoca datele utilizatorului. Este de o importanță primordială deoarece toate datele sunt stocate în acest fișier. Fișierul MDF stochează datele utilizatorilor în baze de date relaționale în coloane de formulare, rânduri, câmpuri, indecși, vizualizări și tabele. SQL Server permite setarea setărilor de autogrow și autoshrink pentru a avea un impact pozitiv asupra performanței bazei de date. Fișierele MDF pot fi încărcate și atașate la o bază de date folosind Microsoft SQL Server. Fișierele MDF au tipul Mime Application/octet-stream.

## Format de fișier MDF

Unitatea fundamentală de stocare a datelor în SQL Server este o pagină. O pagină de stocare atribuită bazei de date este împărțită în pagini logice numerotate de la 0 la n. O singură pagină începe cu un antet de 96 de octeți care cuprinde ID-ul paginii, tipul de structură căruia îi aparține pagina, numărul de înregistrări din pagină și indicatorii către paginile anterioare și următoare.

### Structura fișierului

Un fișier MDF are următoarea structură de date.

* Pagina 0: Antet
* Pagina 1: Primul PFS
* Pagina 2: Primul GAM
* Pagina 3: Primul SGAM
* Pagina 4: nefolosit
* Pagina 5: nefolosit
* Pagina 6: Primul DCM
* Pagina 7: Primul BCM

#### Antet fișier

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

## Referințe

* [Fișiere și grupuri de fișiere baze de date](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Detașarea și atașarea bazei de date - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analizarea anatomiei fișierelor de date SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

