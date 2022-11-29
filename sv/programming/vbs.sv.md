{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "fil", "tillägg", "filformat", "Visual Basic Script", "Programmeringsguide", "vbs exempel", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic Script File",
  "description":"Läs mer om VBS-filformat och API:er som kan skapa och öppna VBS-filer.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Vad är VBS fil?

VBS eller VBScript är kopplat till skriptutgåvan av Microsoft Visual Basic. I datormiljön tillåts användaren komma åt och kontrollera många aspekter av den. VBScript får använda en modell som heter **Component Object Model** för att utnyttja miljöns element och verktyg. Denna miljö är specificerad för att arbeta och köra VBScript.

Det fungerar som Javascript när det nås av klienten inom området webbutveckling. Den används också av servrarna för bearbetning av webbsidor. Det kan övervägas i vissa andra typer av skriptfiler som applikationer av [HTML](/sv/web/html/).


## Kortfattad bakgrund ##

Det lanserades första gången 1996, som en del av de teknologier som används av Microsoft specificerade för Windows-skript. Det utvecklades specifikt för hjälp av webbutvecklare initialt. Samma år släpptes utforskaren av Microsoft Windows med namnet Internet Explorer tillsammans med funktionerna i Visual Basic Script.

Med framstegen inom teknik och webbutveckling lanserades många versioner av VBScript tillsammans med många avancerade funktioner. Dessutom kommer detta skriptspråk under det kommande året att vara en del av Microsoft Windows med nya funktioner.

## Teknisk specifikation ##

För webbsidorna på serversidan används verktyg som **Active Server Pages** tillsammans med VBScript. Detta skriptspråk kan också användas i skriptkomponenten i Windows. Filerna för detta språk lagras med filtillägget .vbs i Windows.

Det finns många kontrollstrukturer såsom loopar som används i koden för detta språk. Den innehåller också argument som är kommandorad och kan namnges eller namnlösas. Filerna på detta språk kan enkelt lagras i mapparna eller på skrivbordet i ett Windows-operativsystem. Även om det inte finns någon specifik integrerad utvecklingsmiljö för VBScript-program som Microsoft Script Editor ger möjligheten att utveckla detta språk.

När VBScript är värd för skriptvärden för Windows, tillhandahåller det olika funktioner som är ganska vanliga för skriptspråken men som inte är tillgängliga i Visual Basic 6.0. Funktionerna som involverar enkel eller direkt åtkomst involverar nätverksskrivare, namnlösa och namngivna kommandoradsargument, stdout och stdin, nätverksresurser, Windows Management Instrumentation, användarinformation om nätverk som gruppmedlemskap och mycket mer.

## VBS filformat exempel ##

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

## Referens ##

* [VBS - av Wikipedia](https://en.wikipedia.org/wiki/VBScript)



