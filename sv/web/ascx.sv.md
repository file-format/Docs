{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx-fil", "ascx-filformat", "ascx-filtyp", "fil", "typ", "vad är en ascx-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX-filformat",
  "description" :"Läs mer om vad en ASCX-fil är och API:er som kan skapa och öppna ASCX-filer.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en ASCX fil?

En fil med tillägget .ascx är en användarkontroll som används som en återanvändbar komponent på webbsidor. Den refereras till på vilken ASP-webbplats som helst genom att dra den från kontrollrutan till sidan. ASCX-användarkontroller läggs till i projektet som en central källa, vilket resulterar i att alla ändringar i användarkontrollen återspeglas på hela webbplatsen. Till skillnad från ASMX-filer som definierar en mekanism för att kommunicera inom 2 objekt över internet, är ASCX-filer användarkontroller för inbäddning på sidor eller webbplats.

## ASCX filformat

ASCX-filer skrivs i vanligt textformat och kan använda kod bakom funktioner som webbsidor som slutar med .ascx.cs. Markeringskod för användarkontroller börjar med @Control-direktivet som visas i följande exempel.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Denna webbanvändarkontroll kan återanvändas på många sidor som sidfot, sidhuvud eller någon form av webbplatsnavigering. Webbenvändarkontroller har egenskaper, metoder och händelser som alla andra kontroller som gör dem användbara för att ställa in deras visuella beteende.

### Exempel på registrering av användarkontroller i web.config

För att kunna använda en enda användarkontroll på många sidor kan webbkontrollen registreras i web.config. Detta gör det möjligt att använda kontrollen över hela webbplatsen istället för att registrera sig på varje sida individuellt. Följande exempelkod definierar hur man registrerar en webbkontroll i web.config för att visas som sidfot på hela webbplatsen.

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
## Referenser

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX User Control](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

