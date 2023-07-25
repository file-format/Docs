{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx-Datei", "asmx-Dateiformat", "asmx-Dateityp", "Datei", "Typ", "was ist eine asmx-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET-Webdienstdatei",
  "description" :"Erfahren Sie, was eine ASMX-Datei und APIs sind, die ASMX-Dateien erstellen und öffnen können.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Was ist eine ASMX-Datei?

Eine Datei mit der Erweiterung .asmx ist eine ASP.NET-Webdienstdatei, die die Kommunikation zwischen zwei Objekten über das Internet mithilfe des Simple Object Access Protocol (SOAP) ermöglicht. Es wird als Dienst auf dem Windows-basierten Webserver bereitgestellt, um eingehende Anforderungen zu verarbeiten und die Antwort zurückzugeben. Im Gegensatz zu [ASPX](/de/web/aspx/)-Dateien, die den Code für die visuelle Anzeige von ASP.NET-Webseiten enthalten, werden ASMX-Dateien auf dem Server im Hintergrund ausgeführt und führen verschiedene Aufgaben aus, z ein Format, in dem die Anfrage gestellt wurde. Diese werden speziell für XML-Webdienste verwendet.

## ASMX-Dateiformat

ASMX-Dateien sind im Nur-Text-Format und können in Anwendungen wie Microsoft Visual Studio oder Texteditoren geöffnet oder bearbeitet werden. Es ist ein proprietäres Dateiformat von Microsoft und hat eine klar definierte Syntax für die Erstellung von Webdiensten. Eine Antwort von einer ASMX-Datei in Form von SOAP-XML hat die folgenden Elemente.

* „Envelop“ – Ein Root-Element, das das XML-Dokument als SOAP-Nachricht identifiziert.
* „Header“ – Ein optionales Element, das anwendungsspezifische Informationen wie Authentifizierungsdaten enthält. Wenn das Header-Element vorhanden ist, muss es das erste untergeordnete Element des Envelope-Elements sein.
* `Body` - Enthält die für den Empfänger bestimmte SOAP-Nachricht.
* `Fault` - Ein optionales Element, das verwendet wird, um Fehlermeldungen anzuzeigen. Wenn das Fault-Element vorhanden ist, muss es ein untergeordnetes Element des Body-Elements sein.

ASMX-Dateien können in .NET-Sprachen wie [C#](/de/programming/cs/), [Visual Basic](/de/programming/vb/) oder JScript geschrieben werden.

## Wie unterscheidet sich ASMX von ASPX und ASCX?

ASMX-Dateien unterscheiden sich von ASPX- und ASCX-Dateien.

* ASPX, Active Server Pages, Dateien sind Programmierdateien, die mit dem Microsoft ASP.NET-Framework generiert werden, das auf Webservern ausgeführt wird. Diese werden im Webbrowser des Clients gerendert, wenn der Benutzer den Zugriff auf eine solche Seite anfordert.
* ASCX, Active Server User Control, definiert Benutzersteuerelemente, die verwendet werden, um wiederverwendbare Steuerelemente in ASP.NET-Webseiten oder ganzen Websites zu definieren.

## Verweise

* [Verbrauch des ASMX-Dienstes](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX-Benutzersteuerung](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

