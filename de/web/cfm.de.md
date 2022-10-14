{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "Erweiterung", "Datei", "Format", "System", "Cold Fusion Markup Language", "Sprache", "CFM-Webseiten", "CFML-Engine", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"Erfahren Sie mehr über das CFM-Dateiformat und APIs, die CFM-Dateien erstellen und öffnen können.",
  "linktitle" :"CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Was ist eine CFM-Datei? ##

Die Webseiten und Dateien, die in **Cold Fusion Markup Language** verwendet werden, enthalten Erweiterungen von CFM und heißen CFM-Webseiten. Diese Skriptsprache für die Webentwicklung wird auf Google App Engine, .NET Framework und JVM ausgeführt. Es kann eine Programmiersprache oder den Code der Sprache enthalten. Wenn der Benutzer auf eine seiner Seiten zugreift, führt der Webserver von ColdFusion diese aus. CFScript (das JavaScript nahe kommt) oder Tags können zum Schreiben von CFML verwendet werden. CFML kann zum Generieren anderer Sprachen außer [HTML](/de/web/html/) wie [CSS](/de/web/css/), [JavaScript](/de/web/js/), [XML](/de/web/ xml/) und mehr.

Die Verwendung dieser Sprache und der von ihr unterstützten Tags erfolgt hauptsächlich bei der Entwicklung dynamischer Webanwendungen. Die Dateien können direkt im Browser online ausgeführt werden, wenn während der Offline-Nutzung der Entwicklungsplattform der Anwendung ein Fehler auftritt.
 

CFML funktioniert so, dass bestimmte Serverdateierweiterungen (.cfc, .cfm) zur Verarbeitung an die CFML-Engine übergeben werden. Wenn die Engines auf Java basieren, wird dies durch Java-Servlets erreicht. Die Engine von CFML verarbeitet nur Funktionen und Tags und gibt Funktionen und Text außerhalb der CFML-Tags unverändert an den Webserver zurück.


## Kurze Geschichte ##

1995 wurde es erstmals von einem Unternehmen namens Allaire gegründet. 2005 wurde es von Adobe übernommen und bietet noch heute Dienstleistungen für die Entwicklung von ColdFusion an. Im Laufe der Jahre wurde es von vielen Menschen und Unternehmen entwickelt und verbessert. 2012 wurde eine Stiftung namens OpenCFML ins Leben gerufen. Später, im Jahr 2015, stellte der ehemalige Railo seine Dienste zur Verfügung, um die Leistung von CFM zu verbessern, und verringerte die Ressourcen für eine bessere Funktionalität. Das letzte Update wurde 2020 veröffentlicht und soll bis 2028 fortgesetzt werden.

## CFM-Dateiformat ##

Der Code der CFM-Dateien und Webseiten besteht hauptsächlich aus Tags wie HTML, jedoch mit einem kleinen Unterschied. Diese Dateien sind für die Ausführung verschiedener Vorgänge verantwortlich, die ColdFusion-Skripts ausführen können.
* Auf diese Dateien kann direkt unter Windows und macOS mit dem Browser eines beliebigen Betriebssystems zugegriffen und ausgeführt werden.
* Adobe ColdFusion bietet die Plattform für die Entwicklung von Webseiten und dynamischen Anwendungen auf dem PC.
* Jeder Texteditor wie NotePad oder jeder andere Texteditor in einem Betriebssystem kann verwendet werden, um diese Dateien zu öffnen, da diese Dateien textbasiert sind.
* Wenn eine CFM-Datei in einem Texteditor geöffnet wird, zeigt sie Code an, der aus Tags und Skripten besteht, die man nicht verstehen würde, wenn man kein Webentwickler ist.

## CFM-Nutzungsbeispiel ##

Das Folgende zeigt eine einfache Beispiel-CFM-Datei für die Verwendung.

### CFM-Dokument ###

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

## Verweise ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

