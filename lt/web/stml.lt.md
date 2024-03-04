{
  "date": "2021-05-20",
  "keywords": [
"stml",
"stml failą",
"stml failo formatas",
"stml failo tipas",
"failą",
"tipo",
"kas yra stml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML – SSI HTML failas",
  "description": "Sužinokite apie STML failo formatą ir API, kurios gali kurti ir atidaryti STML failus.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-ltl"
}
},
  "lastmod": "2021-05-20"
}

## Kas yra STML failas?

Failas su plėtiniu .stml yra tinklalapis su serverio pusės instrukcijomis, kurios vykdomos, kai vartotojas įkelia puslapį žiniatinklio naršyklėje. STML puslapiuose yra serverio pusės kodas, kuriame yra serverio pusės priemonės, skirtos atlikti užduotis, kurių neįmanoma atlikti naudojant paprastą HTML. Nors STML yra panašus į [HTML](/web/html/), jis suteikia daugiau galios vykdydamas komandas serveryje, dar vadinamas serverio pusės įtraukimu (SSI). Įdiegus naujas programavimo kalbas su serverio scenarijais, pvz., PHP, STML naudojimas sumažėjo, nors jį vis dar palaiko visos serverio pusės technologijos. STML failus galima atidaryti bet kuriame teksto rengyklėje ir redaguoti, kad būtų atnaujintos komandos.

## STML failo formatas

STML yra pagrįstas paprastu ascii teksto failo formatu, kurį skaito žmogus. Tačiau ji atitinka sintaksę, kaip apibrėžta ir naudojama naudojant [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), kuri vykdoma serverio pusėje. Kaip ir bet kuri kita serverio pusės scenarijų kalba, STML gali naudoti serverio komandas, kad atliktų tokias užduotis kaip puslapio lankytojų skaitiklis, tinklalapio kalendorius, nuskaityti įrašus iš duomenų bazės ir panašiai.

## STML pavyzdys

Serverio pusės instrukcijos naudojamos tokiose programose kaip puslapio lankytojų skaitiklis arba tinklalapio kalendorius. Šiame pavyzdyje rodomi pirmieji keturi pirmųjų trijų vartotojų duomenų bazės eilučių stulpeliai.

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
## Nuorodos

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)


