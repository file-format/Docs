{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "extension", "file format", "Visual Basic Script", "Programming Guide", "vbs example", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic-Skriptdatei",
  "description":"Erfahren Sie mehr über das VBS-Dateiformat und APIs, die VBS-Dateien erstellen und öffnen können.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Was ist eine VBS-Datei?

VBS bzw. VBScript ist mit der Script Edition von Microsoft Visual Basic verbunden. In der Computerumgebung darf der Benutzer auf viele Aspekte zugreifen und diese steuern. VBScript darf ein Modell namens **Component Object Model** verwenden, um die Elemente und Tools der Umgebung zu nutzen. Diese Umgebung ist für das Arbeiten und Ausführen von VBScript spezifiziert.

Es dient ähnlich wie Javascript, wenn es vom Client im Bereich der Webentwicklung aufgerufen wird. Es wird auch von den Servern für die Verarbeitung von Webseiten verwendet. Es kann in einigen anderen Arten von Skriptdateien wie Anwendungen von [HTML](/de/web/html/) berücksichtigt werden.


## Kurze Geschichte ##

Es wurde erstmals 1996 als Teil der von Microsoft verwendeten Technologien für Windows-Skripts eingeführt. Es wurde ursprünglich speziell für die Hilfe von Webentwicklern entwickelt. Im selben Jahr wurde der Explorer von Microsoft Windows namens Internet Explorer zusammen mit den Funktionen von Visual Basic Script veröffentlicht.

Mit dem Fortschritt in Technologie und Webentwicklung wurden viele Versionen von VBScript zusammen mit vielen erweiterten Funktionen eingeführt. Darüber hinaus wird diese Skriptsprache im kommenden Jahr mit neuen Features Bestandteil von Microsoft Windows sein.

## Technische Spezifikation ##

Für die serverseitigen Webseiten werden Tools wie **Active Server Pages** zusammen mit VBScript verwendet. Diese Skriptsprache kann auch in der Skriptkomponente von Windows verwendet werden. Die Dateien dieser Sprache werden in Windows mit der Erweiterung .vbs gespeichert.

Es gibt viele Kontrollstrukturen wie Schleifen, die im Code dieser Sprache verwendet werden. Es enthält auch Argumente, die Befehlszeilen sind und benannt oder unbenannt sein können. Die Dateien dieser Sprache können einfach in den Ordnern oder auf dem Desktop eines Windows-Betriebssystems abgelegt werden. Obwohl es keine spezielle integrierte Entwicklungsumgebung für VBScript gibt, bieten Programme wie Microsoft Script Editor die Möglichkeit, diese Sprache zu entwickeln.

Wenn VBScript vom Skripthost von Windows gehostet wird, bietet es verschiedene Funktionen, die den Skriptsprachen recht häufig vorkommen, in Visual Basic 6.0 jedoch nicht verfügbar sind. Zu den Funktionen, die einen einfachen oder direkten Zugriff beinhalten, gehören Netzwerkdrucker, unbenannte und benannte Befehlszeilenargumente, stdout und stdin, Netzwerkfreigaben, Windows-Verwaltungsinstrumentation, Benutzerinformationen von Netzwerken wie Gruppenmitgliedschaft und vieles mehr.

## Beispiel für ein VBS-Dateiformat ##

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

## Bezug ##

* [VBS - von Wikipedia](https://en.wikipedia.org/wiki/VBScript)



