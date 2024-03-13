{
  "date": "2021-05-20",
  "keywords": [
"stml",
"stml faylı",
"stml fayl formatı",
"stml fayl növü",
"fayl",
"növü",
"stml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML - SSI HTML faylı",
  "description": "STML fayl formatı və STML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-azl"
}
},
  "lastmod": "2021-05-20"
}

## STML faylı nədir?

.stml uzantısı olan fayl, istifadəçi veb brauzerdə səhifəni yüklədikdə yerinə yetirilən server tərəfi təlimatları olan veb səhifədir. STML səhifələrində adi HTML ilə nail olmaq mümkün olmayan tapşırıqları yerinə yetirmək üçün server tərəfini ehtiva edən server tərəfi kodu var. [HTML](/web/html/) ilə oxşar olsa da, STML Server Side Includes (SSI) adlanan serverdə əmrləri işlətməklə daha çox güc təklif edir. PHP kimi server tərəfi skriptləri ilə yeni proqramlaşdırma dillərinin tətbiqi ilə STML-in istifadəsi hələ də bütün server tərəfi texnologiyaları tərəfindən dəstəklənsə də azalır. STML faylları istənilən mətn redaktorunda açıla və əmrləri yeniləmək üçün redaktə edilə bilər.

## STML fayl formatı

STML, insanların oxuna biləcəyi sadə ascii mətn faylı formatına əsaslanır. Bununla belə, o, müəyyən edilmiş və server tərəfində icra edilən [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) istifadə edərək həyata keçirilən sintaksisə əməl edir. Hər hansı digər server tərəfi skript dili kimi, STML də səhifə ziyarətçilərinin sayğacı, veb səhifə təqvimi, verilənlər bazasından qeydlər əldə etmək və buna bənzər digər tapşırıqları yerinə yetirmək üçün server tərəfindəki əmrlərdən istifadə edə bilər.

## STML nümunəsi

Server tərəfindəki təlimatlar səhifə ziyarətçiləri sayğacı və ya veb səhifə təqvimi kimi proqramlarda istifadə olunur. Aşağıdakı misalda istifadəçilər verilənlər bazasının ilk üç sətirinin ilk dörd sütunu göstərilir.

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
## İstinadlar

* [Server Tərəfi Daxildir](https://en.wikipedia.org/wiki/Server_Side_Includes)


