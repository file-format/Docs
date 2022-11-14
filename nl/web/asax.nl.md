{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax-bestand", "asax-bestandsformaat", "asax-bestandstype", "bestand", "type", "wat is een asax-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET-servertoepassingsbestand",
  "description" :"Leer te weten wat een ASAX-bestand is en wat API's zijn die ASAX-bestanden kunnen maken en openen.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Wat is een ASAX-bestand?

Een bestand met de extensie .asax is een bestand dat wordt gebruikt door ASP.NET-toepassingen die zich aan de serverkant bevinden. Het bevat code voor het reageren op gebeurtenissen op toepassingsniveau en op sessieniveau die worden gegenereerd door ASP.NET of door HTTP-modules. Dit omvat ook het afhandelen van bepaalde gebeurtenissen wanneer de toepassing wordt gestart of afgesloten. ASAX-bestanden zijn optioneel en er wordt slechts één ASAX-bestand toegevoegd aan webapplicaties om de gebeurtenissen en fouten op applicatieniveau op globaal niveau af te handelen. In tegenstelling tot ASPX-pagina's bevatten ASAX-bestanden geen code om de functionaliteit van de applicatie te implementeren.

## ASAX-bestandsindeling

ASAX-bestanden zijn geschreven in platte tekstbestandsindeling en zijn leesbaar voor mensen. Het meest gebruikte ASAX-bestand is Global.asax dat zich in de hoofdmap van een ASP.NET-toepassing bevindt. Webservers zijn geconfigureerd om inkomende oproepen naar dit bestand te weigeren om gebruikers te verbieden de code van dit bestand te downloaden of te bekijken.

### Global.ASAX - Een voorbeeld van ASAX-bestandsindeling

Een enkel ASAX-bestand bestaat uit meerdere secties die zijn geschreven om de gebeurtenissen op toepassingsniveau af te handelen. Deze zijn als volgt.

* **Applicatierichtlijnen** - Toepassingsrichtlijnen zijn tags die worden gebruikt om optionele toepassingsspecifieke instellingen te definiëren die door de ASP.NET-parser moeten worden gebruikt bij het verwerken van het Global.asax-bestand. Deze richtlijnen bevinden zich aan het begin van het Global.asax-bestand en worden als volgt gedefinieerd.

```
<%@ richtlijn attribuut=waarde [attribuut=waarde … ]%>
```
* **Code-declaratieblokken** - Code-declaratieblokken worden gebruikt om secties van servercode te definiëren die zijn ingesloten in ASP.NET-toepassingsbestanden binnen de \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - Deze definiëren de inline code of expressies die worden uitgevoerd wanneer de pagina wordt weergegeven. De twee stijlen van codeweergaveblokken omvatten inline code en inline-expressies. De eerste wordt gebruikt om op zichzelf staande regels of codeblokken te definiëren, terwijl de laterale wordt gebruikt als een snelkoppeling voor het aanroepen van de Write-methode.

## Referenties

* [Overzicht HTTP-handlers en HTTP-modules](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax-syntaxis](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

