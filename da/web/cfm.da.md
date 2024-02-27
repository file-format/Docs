{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"udvidelse",
"fil",
"format",
"system",
"Cold Fusion Markup Language",
"Sprog",
"CFM-websider",
"CFML motor",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM - Cold Fusion Markup",
  "description": "Lær om CFM-filformat og API'er, der kan oprette og åbne CFM-filer.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-dam"
}
},
  "lastmod": "2021-07-13"
}

## Hvad er en CFM fil? ##

Websiderne og filerne, der bruges i **Cold Fusion Markup Language** indeholder udvidelser af CFM og kaldes CFM-websider. Dette webudviklingsscriptsprog kører på Google App Engine, .NET framework og JVM. Det kan indeholde et programmeringssprog eller kode for sproget. Når nogen af dens sider tilgås af brugeren, udfører ColdFusions webserver det. CFScript (som er tæt på JavaScript) eller tags kan bruges til at skrive CFML. CFML kan bruges til at generere andre sprog bortset fra [HTML](/web/html/) som [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/) og flere.

Brugen af dette sprog og tags, som det understøtter, er for det meste i udvikling af dynamiske webapplikationer Filerne kan køres direkte i browseren online, hvis der opstår fejl under offline brug af platformen til udvikling af applikationen.
 
CFML fungerer på en måde, at specifikke server filtypenavne (.cfc, .cfm) gives til behandling til CFML-motoren. Hvis motorerne er baseret på Java, opnås det ved hjælp af Java-servlets. CFML-motoren behandler kun funktioner og tags, og den returnerer funktioner og tekst uden for CFML-tags til webserveren uden ændringer.


## Kort historie ##

I 1995 blev det først oprettet af et selskab ved navn Allaire. I 2005 købte Adobe det, og det leverer tjenester til udvikling af ColdFusion stadig nu. I årenes løb blev det udviklet og opgraderet af mange mennesker og virksomheder. I 2012 blev en fond ved navn OpenCFML lanceret. Senere, i 2015, leverede den tidligere Railo sine tjenester for at forbedre ydeevnen af CFM og gjorde ressourcerne færre til bedre funktionalitet. Den seneste opdatering af den blev lanceret i 2020, som er annonceret til at fortsætte indtil 2028.

## CFM-filformat ##

Koden til CFM-filer og websider består for det meste af tags som HTML, men med en lille forskel. Disse filer er ansvarlige for at udføre forskellige handlinger, som ColdFusion-scripts gør det muligt at køre.
* Disse filer kan tilgås og køres direkte på både Windows og macOS ved hjælp af browseren på ethvert operativsystem.
* Adobe ColdFusion giver platformen til udvikling af websider og dynamiske applikationer på pc.
* Enhver teksteditor som NotePad eller enhver anden teksteditor i et operativsystem kan bruges til at åbne disse filer, da disse filer er tekstbaserede.
* Når en CFM-fil åbnes i en teksteditor, viser den kode, der består af de tags og scripts, som man ikke ville forstå, medmindre han er en webudvikler.

## Eksempel på CFM-brug ##

Det følgende viser et simpelt brugseksempel CFM-fil.

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

## Referencer ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

