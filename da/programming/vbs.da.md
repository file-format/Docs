{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"fil",
"udvidelse",
"filformat",
"Visual Basic Script",
"Programmeringsvejledning",
"vbs eksempel",
"Microsoft Visual Basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS - Visual Basic Script-fil",
  "description": "Lær om VBS filformat og API'er, der kan oprette og åbne VBS filer.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-das"
}
},
  "lastmod": "2021-08-24"
}

## Hvad er VBS fil?

VBS eller VBScript er forbundet med script-udgaven af Microsoft Visual Basic. I computermiljøet har brugeren lov til at få adgang til og kontrollere mange aspekter af det. VBScript har tilladelse til at bruge en model ved navn **Component Object Model** til at benytte miljøets elementer og værktøjer. Dette miljø er specificeret til at arbejde og køre VBScript.

Det fungerer som Javascript, når det tilgås af klienten inden for webudvikling. Det bruges også af serverne til behandling af websider. Det kan overvejes i nogle andre typer scriptfiler, såsom applikationer af [HTML](/web/html/).


## Kort historie ##

Det blev først lanceret i 1996, som en del af de teknologier, der bruges af Microsoft, specificeret til Windows Scripts. Det blev oprindeligt specielt udviklet til hjælp fra webudviklere. Samme år blev Explorer af Microsoft Windows ved navn Internet Explorer frigivet sammen med funktionerne i Visual Basic Script.

Med fremskridtene inden for teknologi og webudvikling blev mange versioner af VBScript sammen med mange avancerede funktioner lanceret. Desuden vil dette scriptsprog i det kommende år være en del af Microsoft Windows med nye funktioner.

## Teknisk specifikation ##

Til websiderne på serversiden bruges værktøjer som **Active Server Pages** sammen med VBScript. Dette scriptsprog kan også bruges i scriptkomponenten i Windows. Filerne på dette sprog er gemt med en .vbs-udvidelse i Windows.

Der er mange kontrolstrukturer såsom sløjfer, der bruges i koden for dette sprog. Det inkluderer også argumenter, der er kommandolinje og kan være navngivne eller unavngivne. Filerne på dette sprog kan simpelthen gemmes i mapperne eller på skrivebordet i et Windows-operativsystem. Selvom der ikke er noget specifikt integreret udviklingsmiljø for VBScript-programmer som Microsoft Script Editor, giver det mulighed for udvikling af dette sprog.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. De funktioner, der involverer nem eller direkte adgang, involverer netværksprintere, unavngivne og navngivne kommandolinjeargumenter, stdout og stdin, netværksdelinger, Windows Management Instrumentation, brugeroplysninger om netværk som gruppemedlemskab og meget mere. 

## VBS filformat eksempel ##

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

## Reference ##

* [VBS - af Wikipedia](https://en.wikipedia.org/wiki/VBScript)




