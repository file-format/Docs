{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","fișier shtml", "format fișier shtml", "tip fișier shtml", "fișier", "tip", "ce este un fișier shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML – Includeți fișierul HTML pe partea de server",
  "description":"Aflați despre formatul de fișier SHTML și despre API-urile care pot crea și deschide fișiere SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Ce este un fișier SHTML?

Un fișier cu extensia .shtml este o pagină web care este scrisă în [HTML](/ro/web/html/) și include instrucțiuni de server. De asemenea, poate conține includeri pe partea de server similare fișierelor ASP pentru o încărcare mai rapidă. Fișierele din partea serverului pot conține, de asemenea, cod executabil care poate face ca serverul să se încarce mai lent decât de obicei. Fișierele SHTML sunt similare cu HTML, dar permit și utilizarea unor comenzi simple de server. Aceste comenzi de server sunt efectuate într-un limbaj simplu de programare pentru computer numit Server Side Includes (SSI). SHTML a fost în mare măsură înlocuit de alte limbaje de programare pe partea de server, cum ar fi [PHP](/ro/programming/php/) include.

## Format de fișier SHTML

Fișierele SHTML sunt scrise în text simplu și folosesc [comenzile SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) care sunt executate pe partea serverului. Aceste comenzi din partea serverului pot fi folosite chiar și pentru a se conecta la baza de date folosind driverele bazei de date și pentru a prelua datele utilizatorilor din tabele.

## Exemplu SHTML

Instrucțiunile de pe partea serverului sunt utilizate în aplicații precum contorul de vizitatori ai paginii sau calendarul paginii web. Următorul exemplu, afișează primele patru coloane din primele trei linii ale bazei de date utilizatori.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Referințe

* [Partea serverului include](https://en.wikipedia.org/wiki/Server_Side_Includes)

