{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL-Dateiformat - Beschreibungssprachendatei für Webdienste",
  "description":"Erfahren Sie, was eine WSDL-Datei und APIs sind, die WSDL-Dateien erstellen und öffnen können.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Was ist eine WSDL-Datei?

Eine WSDL-Datei ist eine Web Services Description Language-Datei, die in XML-Sprache zur Beschreibung von Webdiensten geschrieben ist. Es enthält Informationen über die Endpunkte oder Schnittstellen für die Konnektivität zur Außenwelt in einem allgemein anerkannten Format. [Spezifikationen des WSDL-Dateiformats](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (gepflegt von W3C.org) definieren die Bedingungen für die Veröffentlichung von Daten-Feeds zum Austausch von Daten, um zu haben Fernzugriff auf Anwendungen über Ports und Endpunkte.

## WSDL-Dateiformat – Weitere Informationen

WSDL-Dateien werden als XML-Dateien gespeichert, die für Menschen lesbar sind und in jedem Texteditor geöffnet werden können, um den Inhalt anzuzeigen.

## WSDL-Dienstbeschreibung

Die Spezifikation des WSDL 2.0-Dateiformats beschreibt den WSDL-Dienst als aus zwei Phasen bestehend:

- Abstrakte Bühne
- Betonbühne

Die Wiederverwendbarkeit der Beschreibung und eigenständiger Anliegendesigns wird durch einen Webservice geregelt. Dies wird durch mehrere unterschiedliche Arten von Elementen erreicht, darunter Typen (Datentypdefinitionen), Nachrichten (die übermittelten Daten), Operationen (Aktionen) und Protokolle, die vom Dienst verwendet werden. Diese werden alle auf abstrakter Ebene verwaltet. Die Bindung von Transport- und Wire-Formatdetails wird durch die Bindung angegeben, die die Endpunkte gruppiert, um eine gemeinsame Schnittstelle zu implementieren.

### Welche Technologien können für die Anbindung an WSDL-Dienste verwendet werden?

Für die Anbindung an WSDL-Dienste können verschiedene Technologien verwendet werden, darunter ASP.NET-, C/C++- und Java-Anwendungen.

## WSDL-Beispiel

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

In diesem Beispiel definiert der portType „glossaryTerms“ eine unidirektionale Operation namens „setTerm“.

## Verweise

* [WSDL-XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Spezifikationen des WSDL-Dateiformats](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

