{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extensie", "bestand", "format", "systeem", "Cold Fusion Markup Language", "taal", "CFM-webpagina's", "CFML-engine", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"Meer informatie over CFM-bestandsindelingen en API's die CFM-bestanden kunnen maken en openen.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Wat is een CFM-bestand? ##

De webpagina's en bestanden die worden gebruikt in **Cold Fusion Markup Language** bevatten extensies van CFM en worden CFM-webpagina's genoemd. Deze scripttaal voor webontwikkeling draait op Google App Engine, .NET Framework en JVM. Het kan een programmeertaal of code van de taal bevatten. Wanneer een van zijn pagina's door de gebruiker wordt geopend, voert de webserver van ColdFusion deze uit. CFScript (dat in de buurt komt van JavaScript) of tags kunnen worden gebruikt om CFML te schrijven. CFML kan worden gebruikt voor het genereren van andere talen dan [HTML](/nl/web/html/) zoals [CSS](/nl/web/css/), [JavaScript](/nl/web/js/), [XML](/nl/web/ xml/), en meer.

Het gebruik van deze taal en tags die het ondersteunt, is meestal bij het ontwikkelen van dynamische webapplicaties. De bestanden kunnen direct online in de browser worden uitgevoerd als er een fout optreedt tijdens offline gebruik van het ontwikkelingsplatform van de applicatie.
 

CFML werkt op een manier dat specifieke serverbestandsextensies (.cfc, .cfm) worden gegeven voor verwerking aan de CFML-engine. Als de engines op Java zijn gebaseerd, wordt dit bereikt met behulp van Java-servlets. De engine van CFML verwerkt alleen functies en tags en retourneert functies en tekst buiten de CFML-tags zonder enige wijziging naar de webserver.


## Korte geschiedenis ##

In 1995 werd het voor het eerst gemaakt door een bedrijf genaamd Allaire. In 2005 heeft Adobe het overgenomen en het levert nu nog steeds diensten voor de ontwikkeling van ColdFusion. In de loop der jaren is het door veel mensen en bedrijven ontwikkeld en geüpgraded. In 2012 werd een stichting opgericht met de naam OpenCFML. Later, in 2015, verleende de voormalige Railo zijn diensten om de prestaties van CFM te verbeteren en maakte hij de middelen minder voor betere functionaliteit. De meest recente update ervan werd gelanceerd in 2020 en zal naar verwachting worden voortgezet tot 2028.

## CFM-bestandsindeling ##

De code van de CFM-bestanden en webpagina's omvat meestal de tags zoals HTML, maar met een klein verschil. Deze bestanden zijn verantwoordelijk voor het uitvoeren van verschillende bewerkingen die door ColdFusion-scripts kunnen worden uitgevoerd.
* Deze bestanden kunnen rechtstreeks worden geopend en uitgevoerd op zowel Windows als macOS met behulp van de browser van elk besturingssysteem.
* Adobe ColdFusion biedt het platform voor de ontwikkeling van webpagina's en dynamische applicaties op pc.
* Elke teksteditor zoals NotePad of een andere teksteditor in een besturingssysteem kan worden gebruikt om deze bestanden te openen, aangezien deze bestanden op tekst zijn gebaseerd.
* Wanneer een CFM-bestand wordt geopend in een teksteditor, wordt code weergegeven die bestaat uit de tags en scripts die men niet zou begrijpen tenzij hij een webontwikkelaar is.

## Voorbeeld van CFM-gebruik ##

Het volgende toont een eenvoudig gebruiksvoorbeeld CFM-bestand.

### CFM-document ###

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

## Referenties ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

