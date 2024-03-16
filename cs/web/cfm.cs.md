{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "rozšíření", "soubor", "formát", "systém", "Cold Fusion Markup Language", "jazyk", "webové stránky CFM", "CFML engine", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"Další informace o formátu souboru CFM a rozhraních API, která mohou vytvářet a otevírat soubory CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Co je soubor CFM? ##

Webové stránky a soubory používané v **Cold Fusion Markup Language** obsahují rozšíření CFM a nazývají se webové stránky CFM. Tento skriptovací jazyk pro vývoj webu běží na Google App Engine, .NET framework a JVM. Může obsahovat programovací jazyk nebo kód jazyka. Když uživatel vstoupí na kteroukoli z jeho stránek, webový server ColdFusion ji spustí. K zápisu CFML lze použít CFScript (který je blízký JavaScriptu) nebo značky. CFML lze použít pro generování jiných jazyků kromě [HTML](/cs/web/html/) jako [CSS](/cs/web/css/), [JavaScript](/cs/web/js/), [XML](/cs/web/xml/) a další.

Využití tohoto jazyka a tagů, které podporuje, je většinou při vývoji dynamických webových aplikací. Soubory lze spouštět přímo v prohlížeči online, pokud dojde k chybě při offline používání platformy pro vývoj aplikace.
 

CFML funguje tak, že specifické serverové přípony souborů (.cfc, .cfm) jsou dány ke zpracování CFML motoru. Pokud jsou motory založeny na Javě, je toho dosaženo pomocí Java servletů. Engine CFML zpracovává pouze funkce a tagy a beze změny vrací funkce a text mimo CFML tagy na webový server.


## Stručná historie ##

V roce 1995 byla poprvé vytvořena společností Allaire. V roce 2005 ji získal Adobe a poskytuje služby pro vývoj ColdFusion dodnes. V průběhu let jej vyvinulo a upgradovalo mnoho lidí a společností. V roce 2012 byla spuštěna nadace s názvem OpenCFML. Později, v roce 2015, bývalý Railo poskytl své služby ke zlepšení výkonu CFM a snížil zdroje pro lepší funkčnost. Jeho nejnovější aktualizace byla spuštěna v roce 2020 a je oznámeno, že bude pokračovat až do roku 2028.

## Formát souboru CFM ##

Kód souborů CFM a webových stránek většinou obsahuje značky jako HTML, ale s malým rozdílem. Tyto soubory jsou zodpovědné za provádění různých operací, které skripty ColdFusion umožňují spouštět.
* K těmto souborům lze přistupovat a spouštět je přímo ve Windows i macOS pomocí prohlížeče libovolného operačního systému.
* Adobe ColdFusion poskytuje platformu pro vývoj webových stránek a dynamických aplikací na PC.
* K otevření těchto souborů lze použít jakýkoli textový editor, jako je Poznámkový blok nebo jakýkoli jiný textový editor v operačním systému, protože tyto soubory jsou textové.
* Když je jakýkoli soubor CFM otevřen v textovém editoru, zobrazí se kód, který se skládá ze značek a skriptů, kterým by člověk nerozuměl, pokud není webový vývojář.

## Příklad použití CFM ##

Následující obrázek ukazuje jednoduchý příklad použití souboru CFM.

### Dokument CFM ###

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

## Reference ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

