{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar-Dateiformat",
  "description":"Erfahren Sie mehr über das ICS-Dateiformat und APIs, die ICS-Dateien erstellen und öffnen können.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine ICS-Datei?

Die Internet Calendaring and Scheduling Core Object Specification (iCalendar) ist ein Internetstandard (RFC 2445) zum Austauschen und Bereitstellen von Kalenderereignissen und Zeitplänen. Das iCalendar-Format ist interoperabel, wodurch der Austausch von Kalenderinformationen zwischen Benutzern mit unterschiedlichen E-Mail-Anwendungen sichergestellt wird. iCalendar formatiert die Eingabedaten als Multipurpose Internet Mail Extensions (MIME) und erleichtert den Objektaustausch über verschiedene Transportprotokolle. Diese Transportprotokolle können SMTP, HTTP, asynchrone Punkt-zu-Punkt-Kommunikation und auf physikalischen Medien basierender Netzwerktransport sein.

Mit iCalendar können Benutzer Ereignisse, datums-/zeitabhängige Aufgaben und Frei/Gebucht-Informationen per E-Mail an andere Benutzer weitergeben, die antworten können. iCalendar-Dateien werden mit den Suffixen „.ics“, „.iCalendar“ oder „.ifb“ mit dem MIME-Typ „text/calendar“ gespeichert. iCalendar bleibt unabhängig und unabhängig vom Transportprotokoll. Webserver (mit HTTP-Protokoll) können iCalendar-Informationen transportieren und Webseiten können iCalendar-Daten in eingebetteter Form mit iCalendar enthalten.

## Kurze Geschichte des ICS-Dateiformats

1998 definierte die Internet Engineering Task Force (IETF) iCalendar als Standard (RFC 2445). Der Standard wurde von Frank Dawson (Lotus Notes Corporation) und Derik Stenerson (Microsoft) dokumentiert. Im Jahr 2009 wurde der Standard erneut von Bernard Desruisseaux (Oracle) als RFC 5545 verfeinert. Dieses Mal wurden einige neue Funktionen hinzugefügt und einige veraltete Funktionen wurden als veraltet markiert. Im Jahr 2016 wurde RFC 7986 veröffentlicht und zum ursprünglichen iCalendar RFC erweitert. RFC 7986 fügte dem Hauptobjekt VCALENDAR neue Merkmale hinzu, und es wurden auch neue unterstützende Funktionen für Konferenzsysteme eingeführt.

## ICS-Dateiformat ##

Der von den Daten von iCalendar verwendete MIME-Typ ist „text/calendar“. Der Standardzeichensatz für iCalendar ist UTF-8, durch Angabe von Parametern in MIME kann jedoch ein anderer Zeichensatz verwendet werden. Eine iCalendar-Datei enthält Abschnitte, unter diesen Abschnitten ist "VCALENDAR" der globale Abschnitt, der alle anderen Abschnitte einkapselt. Der Abschnitt VEVENT definiert Ereignisse, VTODO listet alle Aufgaben auf, VJOURNAL enthält Journaleinträge und VTIMEZONE gibt Informationen zur Zeitzone an. mehrere Abschnitte ähnlicher Kategorie sind erlaubt. Bei zahlreichen Veranstaltungen können mehrere VEVENT-Abschnitte in einer iCalendar-Datei vorhanden sein.

### Inhaltszeilen ###

Die iCalendar-Objekte sind in getrennten Textzeilen „Inhaltszeilen“ angeordnet. In diesem Dateiformat beendet die CRLF-Sequenz eine Zeile, während die Länge der Zeile auf 75 Oktette ohne Zeilenumbruch begrenzt ist. Ein langes Datenelement kann sich über viele Zeilen erstrecken.

### Listen- und Feldtrennzeichen ###

Eigenschaften und Parameter geben eine Liste von Werten an, die durch ein KOMMA-Zeichen getrennt sind. Zeichenfolgen in Anführungszeichen werden für URI-basierte Parameterwerte verwendet. Die Liste der Parameter kann anhand des Eigenschaftswerts erstellt werden. Jeder Eigenschaftsparameter in dieser Liste muss durch ein SEMIKOLON getrennt werden.

In einer Werteliste isoliert ein SEMIKOLON Eigenschaftsparameter und ein KOMMA trennt Eigenschaftswerte. Beispiel ist unten angegeben:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Mehrere Werte

Einige Eigenschaften können mehrere Werte haben. Einfach eine neue Inhaltszeile mit dem Eigenschaftsnamen zu erzeugen, ist die Grundregel für mehrwertige Eigenschaften. Für einen einzelnen Wert mit mehreren Sprachvariationen dürfen jedoch keine mehrwertigen Eigenschaften verwendet werden.

### Binärer Inhalt

Innerhalb eines iCalendar-Objekts kann der Eigenschaftswert mithilfe eines URI auf binäre Inhaltsdaten verweisen, die in einer externen MIME-Entität platziert sind. Inline-Binärinhalte können in besonderen Situationen mit dem Parameter „ENCODING“ verwendet werden, wenn die Anwendung ein iCalendar-Objekt als einzige Entität ausdrücken muss. Das folgende Beispiel erläutert eine "ATTACH"-Eigenschaft mit einer URI-Referenz:

ANHANG: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Zeichensatz

Obwohl das standardmäßige Zeichensatzschema für einen iCalendar UTF-8 ist, wird kein Eigenschaftsparameter angegeben, um den Zeichensatz eines Eigenschaftswerts zu definieren. Bei MIME-Übertragungen MUSS der Parameter "Zeichensatz" für den vorhandenen Zeichensatz verwendet werden.

## Verweise

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

