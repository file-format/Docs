{
  "date" : "2021-08-24",
  "keywords" :[ "fișier trc", "format fișier trc", "ce este un fișier trc", "fișier", "exemplu trc", "extensie fișier trc", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier TRC și despre API-urile care pot crea și deschide fișiere TRC.",
  "title" :"TRC - Fișier de urmărire SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Ce este un fișier TRC?
Un fișier cu extensia .trc conține rezultatele urmăririi activității unei baze de date de server Miscrosoft SQL. Aceste fișiere sunt create de un software SQL Server Profiler; de obicei, pachet cu software Microsoft SQL Server. Administratorii bazei de date pot analiza o secvență de declarații ale bazei de date și pot revizui jurnalul de urmărire dacă sunt suspectate anumite erori sau avertismente. Aceste fișiere sunt de obicei localizate în folderul tipic LOG al MSSQL din directorul Fișiere de program pe un sistem de operare Windows.

## Format de fișier TRC
Formatul de fișier TRC este utilizat de SQL Server Profiler pentru a genera automat o nouă urmă a instrucțiunilor recent executate de serverul MS SQL. SQL Server Profiler utilizează șablonul implicit pentru orice urmărire nouă. Cu toate acestea, software-ul include mai multe șabloane predefinite pentru monitorizarea anumitor tipuri de evenimente. De asemenea, SQL Server Profiler poate fi folosit pentru a crea șabloane care definesc clasele de evenimente și coloanele de date de inclus în urme.

### Șabloane predefinite
Iată lista unor șabloane predefinite incluse în SQL Server Profiler:
- **SP_Counts**: Captează comportamentul de execuție a procedurii stocate în timp.
- **Standard**: punct de plecare generic pentru crearea unei urme.
- **TSQL**: Captează toate instrucțiunile Transact-SQL care sunt trimise către SQL Server de către clienți și ora emisă.
- **TSQL_Duration**: Captează toate instrucțiunile Transact-SQL trimise către SQL Server de către clienți, timpul lor de execuție și le grupează după durată.
- **TSQL_Grouped**: Utilizați pentru a investiga interogări de la un anumit client sau utilizator.
- **TSQL_Locks**: Utilizați pentru a depana blocajele, blocarea timpului de expirare și blocarea evenimentelor de escaladare.
- **TSQL_Replay**: Utilizați pentru a efectua reglaj iterativ, cum ar fi testarea benchmark-ului.
- **TSQL_SPs**: Utilizați pentru a analiza pașii componente ai procedurilor stocate.
- **Tuning**: Utilizați pentru a produce o ieșire de urmărire pe care Database Engine Tuning Advisor o poate folosi ca sarcină de lucru pentru reglarea bazelor de date.
### Corelați o urmă cu datele din jurnalul de performanță Windows
SQL Server Profiler poate fi folosit pentru a deschide un jurnal de performanță Microsoft Windows, pentru a alege contoarele care să se coreleze cu o urmărire și pentru a afișa contoarele de performanță selectate alături de urmărire în GUI MS SQL Server Profiler. Pentru a indica datele jurnalului de performanță care se corelează cu evenimentul de urmărire selectat, o bară roșie verticală în fereastra de date System Monitor din SQL Server Profiler.


## Referințe ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

