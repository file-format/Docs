{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx-bestand", "ascx-bestandsformaat", "ascx-bestandstype", "bestand", "type", "wat is een ascx-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX-bestandsindeling",
  "description" :"Meer informatie over wat een ASCX-bestand is en API's die ASCX-bestanden kunnen maken en openen.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een ASCX-bestand?

Een bestand met de extensie .ascx is een gebruikersbesturingselement dat wordt gebruikt als een herbruikbaar onderdeel op webpagina's. Er wordt op elke ASP-website naar verwezen door het van de controlebox naar de pagina te slepen. ASCX-gebruikersbesturingselementen worden als centrale bron aan het project toegevoegd, wat ertoe leidt dat elke wijziging in de gebruikersbesturing op de hele website wordt weergegeven. In tegenstelling tot ASMX-bestanden die een mechanisme definiëren om binnen 2 objecten via internet te communiceren, zijn ASCX-bestanden gebruikerscontroles voor het insluiten in pagina's of websites.

## ASCX-bestandsindeling

ASCX-bestanden zijn geschreven in platte tekst en kunnen code achter functies gebruiken, zoals webpagina's die eindigen op .ascx.cs. Markup-code van gebruikersbesturingselementen begint met @Control-richtlijn, zoals weergegeven in het volgende voorbeeld.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Dit besturingselement voor webgebruikers kan op veel pagina's worden hergebruikt, zoals paginavoettekst, koptekst of een soort sitenavigatie. Bedieningselementen voor webgebruikers hebben eigenschappen, methoden en gebeurtenissen zoals elke andere controle, waardoor ze nuttig zijn bij het instellen van hun visuele gedrag.

### Voorbeeld van het registreren van gebruikersbesturing in web.config

Om een enkele gebruikersbesturing op veel pagina's te gebruiken, kan de webbesturing worden geregistreerd in web.config. Dit maakt het mogelijk om de controle over de hele website te gebruiken in plaats van je op elke pagina afzonderlijk te registreren. De volgende voorbeeldcode definieert hoe u een webbesturingselement in web.config registreert om als voettekst op de hele website weer te geven.

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
## Referenties

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX-gebruikersbediening](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

