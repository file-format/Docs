{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "bestand", "extensie", "bestandsindeling", "Visual Basic Script", "Programmeerhandleiding", "vbs voorbeeld", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic-scriptbestand",
  "description":"Meer informatie over VBS-bestandsindeling en API's die VBS-bestanden kunnen maken en openen.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Wat is een VBS-bestand?

VBS of VBScript is verbonden met de scripteditie van Microsoft Visual Basic. In de computeromgeving mag de gebruiker veel aspecten ervan openen en beheren. VBScript mag een model met de naam **Component Object Model** gebruiken om gebruik te maken van de elementen en hulpmiddelen van de omgeving. Deze omgeving is gespecificeerd voor het werken en uitvoeren van VBScript.

Het lijkt op Javascript wanneer het door de klant wordt gebruikt op het gebied van webontwikkeling. Het wordt ook door de servers gebruikt voor de verwerking van webpagina's. Het kan worden overwogen in sommige andere typen scriptbestanden, zoals toepassingen van [HTML](/nl/web/html/).


## Korte geschiedenis ##

Het werd voor het eerst gelanceerd in 1996, als onderdeel van de door Microsoft gebruikte technologieën voor Windows Scripts. Het is in eerste instantie speciaal ontwikkeld voor de hulp van webontwikkelaars. In hetzelfde jaar werd de ontdekkingsreiziger van Microsoft Windows genaamd Internet Explorer uitgebracht, samen met de functies van Visual Basic Script.

Met de vooruitgang in technologie en webontwikkeling werden vele versies van VBScript samen met vele geavanceerde functies gelanceerd. Bovendien zal deze scripttaal komend jaar met nieuwe features onderdeel uitmaken van Microsoft Windows.

## Technische specificatie ##

Voor de webpagina's aan de serverzijde worden de tools zoals **Active Server Pages** samen met VBScript gebruikt. Deze scripttaal kan ook worden gebruikt in de scriptcomponent van Windows. De bestanden van deze taal worden in Windows opgeslagen met de extensie .vbs.

Er zijn veel besturingsstructuren zoals lussen die in de code van deze taal worden gebruikt. Het bevat ook argumenten die op de opdrachtregel staan en al dan niet benoemd kunnen worden. De bestanden van deze taal kunnen eenvoudig worden opgeslagen in de mappen of op het bureaublad van een Windows-besturingssysteem. Hoewel er geen specifieke geïntegreerde ontwikkelomgeving voor VBScript is, bieden programma's zoals Microsoft Script Editor de mogelijkheid om deze taal te ontwikkelen.

Wanneer VBScript wordt gehost door de Script-host van Windows, biedt het verschillende functies die vrij algemeen zijn voor de scripttalen, maar die niet beschikbaar zijn in Visual Basic 6.0. De functies die gemakkelijke of directe toegang met zich meebrengen, zijn netwerkprinters, niet nader genoemde en benoemde opdrachtregelargumenten, stdout en stdin, netwerkshares, Windows Management Instrumentation, gebruikersinformatie van netwerken zoals groepslidmaatschap en nog veel meer.

## Voorbeeld VBS-bestandsindeling ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Referentie ##

* [VBS - door Wikipedia](https://en.wikipedia.org/wiki/VBScript)



