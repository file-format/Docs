{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"shtml faylı",
"shtml fayl formatı",
"shtml fayl növü",
"fayl",
"növü",
"shtml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML - Server tərəfində HTML faylı daxildir",
  "description": "SHTML fayl formatı və SHTML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-azl"
}
},
  "lastmod": "2021-05-20"
}

## SHTML faylı nədir?

.shtml uzantısı olan fayl [HTML](/web/html/) dilində yazılmış və server təlimatlarını ehtiva edən veb səhifədir. O, həmçinin daha sürətli yükləmə üçün ASP fayllarına bənzər server tərəfini ehtiva edə bilər. Server tərəfi faylları həmçinin serverin adi haldan daha yavaş yüklənməsini təmin edən icra edilə bilən koddan ibarət ola bilər. SHTML faylları HTML-yə bənzəyir, lakin onlar həm də sadə server əmrlərindən istifadə etməyə imkan verir. Bu server əmrləri Server Side Includes (SSI) adlı sadə kompüter proqramlaşdırma dilində yerinə yetirilir. SHTML əsasən [PHP](/programming/php/) daxil olmaqla digər server tərəfi proqramlaşdırma dilləri ilə əvəz edilmişdir.

## SHTML fayl formatı

SHTML faylları düz mətnlə yazılır və server tərəfində icra edilən [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) istifadə olunur. Bu server tərəfi əmrləri verilənlər bazası drayverlərindən istifadə edərək verilənlər bazasına qoşulmaq və cədvəllərdən istifadəçilərin məlumatlarını almaq üçün istifadə edilə bilər.

## SHTML nümunəsi

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


