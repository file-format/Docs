{
  "date" : "2021-05-20",
  "keywords" :[ "stml","fișier stml", "format fișier stml", "tip fișier stml", "fișier", "tip", "ce este un fișier stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Fișier HTML SSI",
  "description":"Aflați despre formatul de fișier STML și despre API-urile care pot crea și deschide fișiere STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Ce este un fișier STML?

Un fișier cu extensia .stml este o pagină web cu instrucțiuni pe partea serverului care sunt executate atunci când un utilizator încarcă pagina în browser web. Paginile STML conțin codul de pe partea de server care conține includeri de pe partea de server pentru a efectua sarcini care nu sunt posibile cu HTML simplu. Deși similar cu [HTML](/ro/web/html/), STML oferă mai multă putere prin rularea comenzilor pe server, numite și Server Side Includes (SSI). Odată cu introducerea de noi limbaje de programare cu scripting server, cum ar fi PHP, utilizarea STML este redusă, deși este încă acceptată de toate tehnologiile server side. Fișierele STML pot fi deschise în orice editor de text și editate pentru actualizarea comenzilor.

## Format de fișier STML

STML se bazează pe un format simplu de fișier text ASCII, care poate fi citit de om. Cu toate acestea, urmează sintaxa așa cum a fost definită și exercitată folosind [comenzile SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) care sunt executate pe partea serverului. La fel ca orice alt limbaj de scripting pe partea serverului, STML poate folosi comenzile pe partea serverului pentru a efectua sarcini precum contorul de vizitatori ai paginii, calendarul paginii web, preluarea înregistrărilor din baza de date și altele similare.

## Exemplu STML

Instrucțiunile din partea serverului sunt utilizate în aplicații precum contorul de vizitatori ai paginii sau calendarul paginii web. Următorul exemplu, afișează primele patru coloane din primele trei linii ale bazei de date utilizatori.

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

