{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "shtml soubor", "formát souboru shtml", "typ souboru shtml", "soubor", "typ", "co je soubor shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML – soubor HTML se zahrnutím na straně serveru",
  "description":"Další informace o formátu souboru SHTML a rozhraních API, která mohou vytvářet a otevírat soubory SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Co je soubor SHTML?

Soubor s příponou .shtml je webová stránka, která je napsána v [HTML](/cs/web/html/) a obsahuje pokyny pro server. Může také obsahovat součásti na straně serveru podobné souborům ASP pro rychlejší načítání. Soubory na straně serveru mohou také obsahovat spustitelný kód, který může zpomalit načítání serveru než obvykle. Soubory SHTML jsou podobné HTML, ale také umožňují použití jednoduchých příkazů serveru. Tyto serverové příkazy se provádějí v jednoduchém počítačovém programovacím jazyce zvaném Server Side include (SSI). SHTML bylo do značné míry nahrazeno jinými programovacími jazyky na straně serveru, jako je [PHP](/cs/programming/php/).

## Formát souboru SHTML

Soubory SHTML jsou psány jako prostý text a používají [příkazy SSI] (https://www.w3.org/Jigsaw/Doc/User/SSI.html), které se spouštějí na straně serveru. Tyto příkazy na straně serveru lze dokonce použít k připojení k databázi pomocí databázových ovladačů a načítání uživatelských dat z tabulek.

## Příklad SHTML

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

