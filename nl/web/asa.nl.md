{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "bestandsindeling", "bestandstype", "wat is een .asa-bestand" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP-configuratiebestand",
  "description" :"Meer informatie over wat een ASA-bestand is en API's die ASA-bestanden kunnen maken en openen.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Wat is een ASA-bestand?

Een ASA-bestand is een configuratiebestand, gemaakt voor [ASP](/nl/web/asp/)/ASP.NET-projecten. Het bevat declaraties van variabelen, bevat en functies die bedoeld zijn om op Globaal niveau in de applicatie toegankelijk te zijn. Alle pagina's in het project hebben toegang tot deze variabelen en functies, zodat ze niet opnieuw hoeven te worden geschreven. Een voorbeeld hiervan is de Global.asa-pagina die is opgeslagen in de hoofdmap om toegankelijk te zijn voor andere ASP-websitepagina's. Global.asa-bestanden zijn optioneel, maar indien gebruikt, kan elke toepassing slechts één Global.asa-bestand hebben.

## ASA-bestandsindeling - Meer informatie

ASA-bestanden zijn platte tekstbestanden met de volgende informatie.

* Toepassingsgebeurtenissen
* Sessie-evenementen
* \<object> verklaringen
* TypeBibliotheekaangiften
* de #include-richtlijn

## ASA-bestandsvoorbeeld

Een Global.asa-bestand kan er ongeveer zo uitzien.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referenties

* [ASP Global.asa-bestand - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

