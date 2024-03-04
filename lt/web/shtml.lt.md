{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"shtml failą",
"shtml failo formatas",
"shtml failo tipas",
"failą",
"tipo",
"kas yra shtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML – serverio pusės įtraukti HTML failą",
  "description": "Sužinokite apie SHTML failo formatą ir API, kurios gali kurti ir atidaryti SHTML failus.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-ltl"
}
},
  "lastmod": "2021-05-20"
}

## Kas yra SHTML failas?

Failas su plėtiniu .shtml yra tinklalapis, parašytas [HTML](/web/html/) ir kuriame pateikiamos serverio instrukcijos. Jame taip pat gali būti serverio įtraukimų, panašių į ASP failus, kad būtų galima greičiau įkelti. Serverio pusės failuose taip pat gali būti vykdomojo kodo, dėl kurio serveris gali būti įkeltas lėčiau nei įprastai. SHTML failai yra panašūs į HTML, tačiau jie taip pat leidžia naudoti paprastas serverio komandas. Šios serverio komandos atliekamos paprasta kompiuterio programavimo kalba, vadinama serverio pusės įeinančiais elementais (SSI). SHTML iš esmės pakeitė kitos serverio pusės programavimo kalbos, tokios kaip [PHP](/programming/php/).

## SHTML failo formatas

SHTML failai rašomi paprastu tekstu ir naudoja [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), kurie vykdomi serverio pusėje. Šios serverio pusės komandos gali būti naudojamos netgi prisijungti prie duomenų bazės naudojant duomenų bazės tvarkykles ir gauti vartotojų duomenis iš lentelių.

## SHTML pavyzdys

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


