{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"ascx faylı",
"ascx fayl formatı",
"ascx fayl növü",
"fayl",
"növü",
"ascx faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASCX fayl formatı",
  "description": "ASCX faylı və ASCX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-azx"
}
},
  "lastmod": "2020-09-10"
}

## ASCX faylı nədir?

.ascx uzantılı fayl veb-səhifələrdə təkrar istifadə edilə bilən komponent kimi istifadə edilən istifadəçi nəzarətidir. Hər hansı bir ASP veb-saytında onu idarəetmə qutusundan səhifəyə sürükləməklə istinad edilir. ASCX istifadəçi nəzarətləri layihəyə mərkəzi mənbə kimi əlavə edilir və nəticədə istifadəçi nəzarətində hər hansı dəyişiklik bütün vebsaytda əks olunur. İnternet üzərindən 2 obyekt daxilində ünsiyyət mexanizmini təyin edən ASMX fayllarından fərqli olaraq, ASCX faylları səhifələrə və ya veb-saytlara daxil etmək üçün istifadəçi nəzarətləridir.

## ASCX fayl formatı

ASCX faylları düz mətn formatında yazılır və .ascx.cs ilə bitən veb səhifələr kimi funksiyanın arxasındakı koddan istifadə edə bilər. İstifadəçi nəzarətlərinin işarələmə kodu aşağıdakı nümunədə göstərildiyi kimi @Control direktivi ilə başlayır.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Bu veb istifadəçi nəzarəti səhifə altbilgisi, başlıq və ya bir növ sayt naviqasiyası kimi bir çox səhifələrdə təkrar istifadə edilə bilər. Veb istifadəçi nəzarətləri hər hansı digər nəzarət kimi xassələrə, metodlara və hadisələrə malikdir və bu da onları vizual davranışlarını təyin etməkdə faydalı edir.

### Web.config-də istifadəçi nəzarətlərinin qeydiyyata alınması nümunəsi

Bir çox səhifələrdə tək istifadəçi nəzarətindən istifadə etmək üçün veb-nəzarət web.config-də qeydiyyata alına bilər. Bu, hər bir səhifədə ayrıca qeydiyyatdan keçmək əvəzinə bütün vebsayt üzərində nəzarətdən istifadə etməyə imkan verir. Aşağıdakı nümunə kodu veb-nəzarətin bütün vebsaytda altbilgi kimi göstərilmək üçün web.config-də necə qeydiyyata alınacağını müəyyənləşdirir.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## İstinadlar
 * [ASCX İstifadəçi Nəzarəti](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

