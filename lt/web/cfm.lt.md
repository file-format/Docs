{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Cold Fusion žymėjimo kalba",
"kalba",
"CFM tinklalapiai",
"CFML variklis",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM – šaltojo sintezės žymėjimas",
  "description": "Sužinokite apie CFM failo formatą ir API, kurios gali kurti ir atidaryti CFM failus.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-ltm"
}
},
  "lastmod": "2021-07-13"
}

## Kas yra CFM failas? ##

**Cold Fusion Markup Language** naudojamuose tinklalapiuose ir failuose yra CFM plėtinių ir jie vadinami CFM tinklalapiais. Ši žiniatinklio kūrimo scenarijų kalba veikia Google App Engine, .NET framework ir JVM. Jame gali būti programavimo kalba arba kalbos kodas. Kai vartotojas pasiekia bet kurį iš jo puslapių, ColdFusion žiniatinklio serveris jį vykdo. CFML rašymui gali būti naudojamas CFScript (tai artimas JavaScript) arba žymos. CFML gali būti naudojamas kuriant kitas kalbas, išskyrus [HTML](/web/html/), pvz., [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/) ir kt.

Ši kalba ir jos palaikomos žymos dažniausiai naudojamos kuriant dinamines žiniatinklio programas. Failus galima tiesiogiai paleisti naršyklėje prisijungus, jei naudojant programos kūrimo platformą neprisijungus įvyksta klaida.
 
CFML veikia taip, kad CFML varikliui apdoroti suteikiami konkretūs serverio failų plėtiniai (.cfc, .cfm). Jei varikliai yra pagrįsti Java, tai pasiekiama naudojant Java servletus. CFML variklis apdoroja tik funkcijas ir žymas, o funkcijas ir tekstą, nepriklausančią CFML žymoms, grąžina žiniatinklio serveriui be jokių pakeitimų.


## Trumpa istorija ##

1995 m. ją pirmą kartą sukūrė korporacija, pavadinta Allaire. 2005 m. Adobe jį įsigijo ir iki šiol teikia ColdFusion kūrimo paslaugas. Bėgant metams jį sukūrė ir atnaujino daugybė žmonių ir įmonių. 2012 m. buvo įkurtas fondas pavadinimu OpenCFML. Vėliau, 2015 m., buvęs Railo teikė savo paslaugas, kad pagerintų CFM našumą ir sumažino išteklių geresniam funkcionalumui. Paskutinis jo atnaujinimas buvo paleistas 2020 m., kuris, kaip skelbiama, tęsis iki 2028 m.

## CFM failo formatas ##

CFM failų ir tinklalapių kodą dažniausiai sudaro tokios žymos, kaip HTML, bet su nedideliu skirtumu. Šie failai yra atsakingi už įvairių operacijų, kurias leidžia vykdyti ColdFusion scenarijai, atlikimą.
* Šiuos failus galima pasiekti ir paleisti tiesiogiai tiek Windows, tiek MacOS, naudojant bet kurios operacinės sistemos naršyklę.
* Adobe ColdFusion suteikia platformą tinklalapiams ir dinaminėms programoms kompiuteryje kurti.
* Šiems failams atidaryti galima naudoti bet kurį teksto rengyklę, pvz., Notepad arba bet kurį kitą teksto rengyklę operacinėje sistemoje, nes šie failai yra pagrįsti tekstu.
* Kai bet kuris CFM failas atidaromas teksto rengyklėje, jame rodomas kodas, kurį sudaro žymos ir scenarijai, kurių nesuprastų, nebent jis būtų žiniatinklio kūrėjas.

## CFM naudojimo pavyzdys Nr.

Toliau pateikiamas paprastas CFM failo naudojimo pavyzdys.

### CFM dokumentas ###

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

## Nuorodos Nr.

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

