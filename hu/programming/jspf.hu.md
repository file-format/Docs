{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP Fragment File Format",
  "description":"További információ a JSPF fájlformátumról és az API-król, amelyek JSPF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Mi az a JSPF fájl?
A .jspf kiterjesztésű fájl neve JSP fragmentum; egy másik JSP-fájlban található statikus fájl. A JSPF-fájlokat nem fordítják le önmagukban, hanem az oldal mellett, amelyben szerepeltek. Szintaxisa hasonló a Java Server Pages (JSP) kódjához. Csak egy töredéket tartalmaz a JSP-ből; nem tartalmazza a teljes JSP dokumentumot.

## JSPF fájlformátum
Ehelyett a „JSP szegmens” kifejezést használjuk, mivel a „JSP fragmentum” kifejezés túlterhelt a JSP 2.0 specifikációban. A JSP-töredékek .jsp vagy .jspf kiterjesztést is használhatnak, és vagy a **/WEB-INF/jspf** fájlba, vagy a többi statikus fájlba kell elhelyezni. A nem teljes oldalak JSP-töredékeinek .jspf kiterjesztést kell használniuk, és a **/WEB-INF/jspf** mappába kell helyezni.

### JSP vagy JSP Fragment File Organization
A JSP-fájl a következő szakaszokat tartalmazza a felsorolás sorrendjében:

1. Megjegyzések megnyitása
2. JSP-oldal direktíva(ok)
3. Opcionális címkekönyvtár-irányelv(ek)
4. Opcionális JSP-deklaráció(k)
5. HTML és JSP kód

A JSP- vagy JSPF-fájl egyaránt egy szerveroldali stílusú megjegyzéssel kezdődik, amelyet **Megnyitó megjegyzés**-nak neveznek:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Ez a megjegyzés csak a szerver oldalon látható, mert a JSP-oldal megjelenítése során eltávolítják.

## Mikor kell használni a JSP Fragment fájlt?
Ha egy JSP-oldal bizonyos, de összetett struktúrát igényel, amely más JSP-oldalakon is felhasználható, ennek egyik módja az, hogy az Összetett nézet mintájával (a Java Blueprints Patterns szakasza) darabokra bontja. Például egy JSP-oldal megjelenítési struktúrájában néha a következő logikai elrendezés található:

{{< figure src="../jspf.png" alt="JSPF fájl formátum" >}}

Ebben a helyzetben ez az összetett JSP-oldal különféle modulokká alakítható, amelyek mindegyikét külön JSP-töredéknek nevezzük. A JSP-töredékek ezután elhelyezhetők a megfelelő helyeken az összetett JSP-oldalon. Ezért a JSPF fájl akkor használatos, ha statikus include direktívákat használnak olyan oldalak beillesztésére, amelyeket önmagában nem hívna meg, a .jspf kiterjesztésű fájlokat a webalkalmazás-archívum /WEB-INF/jspf/ könyvtárába kell helyezni ( háború).

## JSPF példa
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Hivatkozások

* [A JavaServer-oldalak kódegyezményei](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

