{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","file shtml", "formato file shtml", "tipo di file shtml", "file", "tipo", "che cos'è un file shtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Lato server include file HTML",
  "description":"Scopri il formato di file SHTML e le API che possono creare e aprire file SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Che cos'è un file SHTML?

Un file con estensione .shtml è una pagina web scritta in [HTML](/it/web/html/) e include le istruzioni del server. Può anche contenere inclusioni lato server simili ai file ASP per un caricamento più rapido. I file lato server possono anche contenere codice eseguibile che può rallentare il caricamento del server del solito. I file SHTML sono simili all'HTML ma consentono anche l'uso di semplici comandi del server. Questi comandi del server vengono eseguiti in un semplice linguaggio di programmazione per computer chiamato Server Side Include (SSI). SHTML è stato ampiamente sostituito da altri linguaggi di programmazione lato server come [PHP](/it/programming/php/) include.

## Formato file SHTML

I file SHTML sono scritti in testo normale e utilizzano i [comandi SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) che vengono eseguiti sul lato server. Questi comandi lato server possono essere utilizzati anche per connettersi al database utilizzando i driver del database e recuperare i dati degli utenti dalle tabelle.

## Esempio SHTML

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

