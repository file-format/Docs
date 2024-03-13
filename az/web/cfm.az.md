{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"uzadılması",
"fayl",
"format",
"sistemi",
"Cold Fusion İşarələmə Dili",
"dil",
"CFM veb səhifələri",
"CFML mühərriki",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM - Cold Fusion Markup",
  "description": "CFM faylları yarada və aça bilən CFM fayl formatı və API-lər haqqında öyrənin.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-azm"
}
},
  "lastmod": "2021-07-13"
}

## CFM faylı nədir? ##

**Cold Fusion Markup Language**-də istifadə olunan veb-səhifələr və fayllar CFM-in genişlənmələrini ehtiva edir və CFM veb səhifələri adlanır. Bu veb inkişaf skript dili Google App Engine, .NET framework və JVM üzərində işləyir. O, proqramlaşdırma dilini və ya dilin kodunu ehtiva edə bilər. İstifadəçi onun səhifələrindən hər hansı birinə daxil olduqda, ColdFusion veb-serveri onu yerinə yetirir. CFML yazmaq üçün CFScript (JavaScript-ə yaxındır) və ya teqlərdən istifadə edilə bilər. CFML [HTML](/web/html/) dilindən başqa, [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/) və sair dilləri yaratmaq üçün istifadə edilə bilər.

Bu dilin və onun dəstəklədiyi teqlərdən istifadə daha çox dinamik veb proqramların işlənib hazırlanmasındadır. Proqramın inkişaf platformasının oflayn istifadəsi zamanı hər hansı bir xəta baş verərsə, fayllar birbaşa brauzerdə onlayn olaraq işlədilə bilər.
 
CFML elə işləyir ki, xüsusi server fayl uzantıları (.cfc, .cfm) CFML mühərrikinə emal üçün verilir. Mühərriklər Java-ya əsaslanırsa, buna Java servletlərindən istifadə etməklə nail olunur. CFML mühərriki yalnız funksiyaları və teqləri emal edir və CFML teqlərindən kənar funksiyaları və mətni heç bir dəyişiklik etmədən veb serverə qaytarır.


## Qısa tarix ##

1995-ci ildə ilk dəfə Allaire adlı korporasiya tərəfindən yaradılmışdır. 2005-ci ildə Adobe onu əldə etdi və o, hələ də ColdFusion-u inkişaf etdirmək üçün xidmətlər göstərir. İllər keçdikcə bir çox insanlar və şirkətlər tərəfindən inkişaf etdirildi və təkmilləşdirildi. 2012-ci ildə OpenCFML adlı fond fəaliyyətə başladı. Daha sonra, 2015-ci ildə keçmiş Railo CFM performansını yaxşılaşdırmaq üçün xidmətlərini təqdim etdi və daha yaxşı funksionallıq üçün resursları daha az etdi. Ən son yeniləməsi 2020-ci ildə istifadəyə verildi və 2028-ci ilə qədər davam edəcəyi açıqlandı.

## CFM Fayl Format ##

CFM fayllarının və veb səhifələrin kodu əsasən HTML kimi etiketlərdən ibarətdir, lakin cüzi fərqlə. Bu fayllar ColdFusion skriptlərinin işə salmağa imkan verdiyi müxtəlif əməliyyatların yerinə yetirilməsinə cavabdehdir.
* Bu fayllara istənilən əməliyyat sisteminin brauzerindən istifadə etməklə birbaşa Windows və macOS-da daxil olmaq və işlətmək olar.
* Adobe ColdFusion kompüterdə veb səhifələrin və dinamik proqramların inkişafı üçün platforma təqdim edir.
* NotePad və ya əməliyyat sistemindəki hər hansı digər mətn redaktoru kimi istənilən mətn redaktoru bu faylları açmaq üçün istifadə edilə bilər, çünki bu fayllar mətn əsaslıdır.
* Hər hansı bir CFM faylı mətn redaktorunda açıldıqda, o, veb tərtibatçısı olmasa, birinin başa düşməyəcəyi teqlərdən və skriptlərdən ibarət kodu göstərir.

## CFM İstifadə Nümunəsi ##

Aşağıda sadə istifadə nümunəsi CFM faylı göstərilir.

### CFM Sənədi ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## İstinadlar ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

