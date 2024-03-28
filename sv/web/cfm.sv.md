{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "tillägg", "fil", "format", "system", "Cold Fusion Markup Language", "språk", "CFM-webbsidor", "CFML-motor", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"Läs mer om CFM-filformat och API:er som kan skapa och öppna CFM-filer.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Vad är en CFM fil? ##

Webbsidorna och filerna som används i **Cold Fusion Markup Language** innehåller tillägg av CFM och kallas CFM-webbsidor. Detta skriptspråk för webbutveckling körs på Google App Engine, .NET framework och JVM. Det kan innehålla ett programmeringsspråk eller kod för språket. När någon av dess sidor nås av användaren, kör ColdFusions webbserver den. CFScript (som är nära JavaScript) eller taggar kan användas för att skriva CFML. CFML kan användas för att generera andra språk förutom [HTML](/sv/web/html/) som [CSS](/sv/web/css/), [JavaScript](/sv/web/js/), [XML](/sv/web/xml/), och mer.

Användningen av detta språk och taggar som det stöder är främst vid utveckling av dynamiska webbapplikationer. Filerna kan köras direkt i webbläsaren online om något fel uppstår under offlineanvändning av plattformen för utveckling av applikationen.
 

CFML fungerar på ett sätt att specifika serverfiltillägg (.cfc, .cfm) ges för bearbetning till CFML-motorn. Om motorerna är baserade på Java, uppnås det med hjälp av Java-servlets. CFML-motorn bearbetar endast funktioner och taggar och den returnerar funktioner och text utanför CFML-taggarna till webbservern utan någon förändring.


## Kortfattad bakgrund ##

1995 skapades det först av ett företag vid namn Allaire. 2005 förvärvade Adobe det och det tillhandahåller tjänster för att utveckla ColdFusion fortfarande. Under åren som gått har det utvecklats och uppgraderats av många människor och företag. 2012 lanserades en stiftelse vid namn OpenCFML. Senare, 2015, tillhandahöll den tidigare Railo sina tjänster för att förbättra prestandan för CFM och gjorde resurserna färre för bättre funktionalitet. Den senaste uppdateringen av den lanserades 2020 som tillkännages att den kommer att fortsätta till 2028.

## CFM-filformat ##

Koden för CFM-filerna och webbsidorna består mestadels av taggar som HTML men med en liten skillnad. Dessa filer är ansvariga för att utföra olika operationer som ColdFusion-skript gör det möjligt att köra.
* Dessa filer kan nås och köras direkt på både Windows och macOS med hjälp av webbläsaren i alla operativsystem.
* Adobe ColdFusion tillhandahåller plattformen för utveckling av webbsidor och dynamiska applikationer på PC.
* Alla textredigerare som NotePad eller någon annan textredigerare i ett operativsystem kan användas för att öppna dessa filer eftersom dessa filer är textbaserade.
* När en CFM-fil öppnas i en textredigerare visar den kod som består av taggar och skript som man inte skulle förstå om han inte är en webbutvecklare.

## CFM-användningsexempel ##

Följande visar ett enkelt användningsexempel CFM-fil.

### CFM-dokument ###

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

## Referenser ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

