{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extension", "file", "format", "system", "Cold Fusion Markup Language", "language", "CFM web pages", "CFML engine", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"További információ a CFM fájlformátumról és az API-król, amelyek CFM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Mi az a CFM fájl? ##

A **Cold Fusion Markup Language**-ban használt weboldalak és fájlok CFM-kiterjesztéseket tartalmaznak, és CFM-weblapoknak nevezik őket. Ez a webfejlesztési szkriptnyelv a Google App Engine-en, a .NET-keretrendszeren és a JVM-en fut. Tartalmazhat egy programozási nyelvet vagy a nyelv kódját. Amikor a felhasználó hozzáfér valamelyik oldalához, a ColdFusion webszervere végrehajtja azt. A CFScript (amely közel áll a JavaScripthez) vagy címkék használhatók CFML írásához. A CFML a [HTML](/hu/web/html/) nyelven kívül más nyelvek létrehozására is használható, például [CSS](/hu/web/css/), [JavaScript](/hu/web/js/), [XML](/hu/web/) xml/), és így tovább.

Ezt a nyelvet és az általa támogatott címkéket leginkább dinamikus webalkalmazások fejlesztésére használják. A fájlok közvetlenül online futtathatók a böngészőben, ha az alkalmazás fejlesztési platformjának offline használata során hiba történik.
 

A CFML úgy működik, hogy meghatározott szerverfájl-kiterjesztéseket (.cfc, .cfm) kap a CFML-motor feldolgozása. Ha a motorok Java alapúak, akkor ez Java szervletekkel érhető el. A CFML motorja csak függvényeket és címkéket dolgoz fel, a CFML címkéken kívüli függvényeket és szövegeket pedig változtatás nélkül visszaküldi a webszervernek.


## Rövid története ##

1995-ben először egy Allaire nevű vállalat hozta létre. 2005-ben az Adobe megvásárolta, és jelenleg is nyújt szolgáltatásokat a ColdFusion fejlesztéséhez. Az elmúlt évek során sok ember és cég fejlesztette és korszerűsítette. 2012-ben indult egy alapítvány OpenCFML néven. Később, 2015-ben a korábbi Railo nyújtotta szolgáltatásait a CFM teljesítményének javítása érdekében, és csökkentette az erőforrásokat a jobb funkcionalitás érdekében. A legújabb frissítés 2020-ban jelent meg, amely a tervek szerint 2028-ig folytatódik.

## CFM fájlformátum ##

A CFM fájlok és weboldalak kódja többnyire olyan címkéket tartalmaz, mint a HTML, de kis eltéréssel. Ezek a fájlok felelősek a ColdFusion szkriptek által lehetővé tett különféle műveletek végrehajtásáért.
* Ezek a fájlok közvetlenül elérhetők és futtathatók Windows és macOS rendszeren is, bármely operációs rendszer böngészőjével.
* Az Adobe ColdFusion platformot biztosít weboldalak és dinamikus alkalmazások PC-n történő fejlesztéséhez.
* Bármely szövegszerkesztő, például a NotePad vagy bármely más operációs rendszer szövegszerkesztője használható ezen fájlok megnyitásához, mivel ezek a fájlok szövegalapúak.
* Ha bármely CFM-fájlt megnyitunk egy szövegszerkesztőben, az olyan kódot jelenít meg, amely címkékből és szkriptekből áll, amelyeket az ember nem értene meg, hacsak nem webfejlesztő.

## CFM használati példa ##

Az alábbiakban egy egyszerű használati példa látható a CFM fájlra.

### CFM dokumentum ###

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

## Referenciák ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

