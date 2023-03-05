{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "soubor stml", "formát souboru stml", "typ souboru stml", "soubor", "typ", "co je soubor stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML soubor",
  "description":"Další informace o formátu souboru STML a rozhraních API, která mohou vytvářet a otevírat soubory STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Co je soubor STML?

Soubor s příponou .stml je webová stránka s instrukcemi na straně serveru, které se provádějí, když uživatel načte stránku ve webovém prohlížeči. Stránky STML obsahují kód na straně serveru, který obsahuje serverovou část, která zahrnuje provádění úloh, které není možné dosáhnout pomocí prostého HTML. Ačkoli je STML podobný [HTML](/cs/web/html/), nabízí větší výkon spuštěním příkazů na serveru, nazývaných také Server Side Within (SSI). Se zavedením nových programovacích jazyků se skriptováním na straně serveru, jako je PHP, se používání STML omezilo, i když je stále podporováno všemi technologiemi na straně serveru. Soubory STML lze otevřít v libovolném textovém editoru a upravit pro aktualizaci příkazů.

## Formát souboru STML

STML je založen na formátu prostého textového souboru ASCII, který je čitelný pro člověka. Dodržuje však syntaxi, jak je definována a prováděna pomocí [příkazů SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html), které se spouštějí na straně serveru. Stejně jako jakýkoli jiný skriptovací jazyk na straně serveru může STML používat příkazy na straně serveru k provádění úkolů, jako je počítadlo návštěvníků stránky, kalendář webových stránek, načítání záznamů z databáze a podobné další.

## Příklad STML

Instrukce na straně serveru se používají v aplikacích, jako je počítadlo návštěvnosti stránky nebo kalendář webové stránky. Následující příklad zobrazuje první čtyři sloupce z prvních tří řádků databáze uživatelů.

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
## Reference

* [Zahrnuje stranu serveru](https://en.wikipedia.org/wiki/Server_Side_Includes)

