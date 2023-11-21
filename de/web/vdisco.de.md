{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO-Datei – DISCO Dynamic Discovery Document File Format",
  "description":"Erfahren Sie, was eine VDISCO-Datei ist?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Was ist eine VDISCO-Datei?

Eine VDISCO-Datei ist eine Erkennungsdatei, die von Microsoft Visual Studio in seinen Webdiensten verwendet wird. Es bietet Informationen zu den verfügbaren Webdiensten wie deren URLs, Namespaces und Methoden. Die VDISCO-Datei ähnelt dem Dateiformat [DISCO](/web/disco/), wird jedoch zur Laufzeit generiert. Es wird in der Webdienstanwendung gespeichert und von Visual Studio verwendet, um Webdienste dynamisch in einem Projekt zu erkennen und zu verwenden. VDISCO-Dateien werden in Kombination mit der Datei [.asmx](/web/asmx/) verwendet, die den eigentlichen Webdienstcode enthält.

Sie können die VDISCO-Datei in jedem Texteditor wie Microsoft Notepad, Github Atom und Apple TextEdit öffnen. Es kann auch mit Microsoft Visual Studio 2012 und höher geöffnet werden, um damit zu arbeiten.

## VDISCO-Dateiformat

Eine VDISCO-Datei wird im Dateiformat [XML](/web/xml/) gespeichert und gehostet, einem universellen Format für die Zusammenstellung und Veröffentlichung von Daten. Es enthält die Dienst-URL, Namespaces und Methoden in Standard-XML-Tags, wobei jedes Tag den jeweiligen Wert seiner Informationen enthält.

## Verweise

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C#-Beispiel der DiscoveryClient-Klasse](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

