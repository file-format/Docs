{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "file stml", "formato file stml", "tipo di file stml", "file", "tipo", "che cos'è un file stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - File HTML SSI",
  "description":"Scopri il formato di file STML e le API che possono creare e aprire file STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Che cos'è un file STML?

Un file con estensione .stml è una pagina web con istruzioni lato server che vengono eseguite quando un utente carica la pagina nel browser web. Le pagine STML contengono codice lato server che contiene include lato server per eseguire attività che non è possibile ottenere con il semplice HTML. Sebbene simile a [HTML](/it/web/html/), STML offre più potenza eseguendo i comandi sul server, chiamati anche Server Side Include (SSI). Con l'introduzione di nuovi linguaggi di programmazione con script lato server come PHP, l'uso di STML viene ridotto sebbene sia ancora supportato da tutte le tecnologie lato server. I file STML possono essere aperti in qualsiasi editor di testo e modificati per aggiornare i comandi.

## Formato file STML

STML si basa su un semplice formato di file di testo ascii leggibile dall'uomo. Tuttavia, segue la sintassi definita ed esercitata utilizzando i [comandi SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) che vengono eseguiti sul lato server. Come qualsiasi altro linguaggio di scripting lato server, STML può utilizzare i comandi lato server per eseguire attività come il contatore dei visitatori della pagina, il calendario delle pagine Web, il recupero dei record dal database e altri simili.

## Esempio STML

Le istruzioni lato server vengono utilizzate in applicazioni come il contatore dei visitatori della pagina o il calendario delle pagine Web. Nell'esempio seguente vengono visualizzate le prime quattro colonne delle prime tre righe del database degli utenti.

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
## Riferimenti

* [Include lato server](https://en.wikipedia.org/wiki/Server_Side_Includes)

