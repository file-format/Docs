{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - E-Mail-Postfachdatei",
  "description":"Erfahren Sie mehr über das MBOX-Dateiformat und APIs, die MBOX-Dateien erstellen und öffnen können.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine MBOX-Datei?

Das MBox-Dateiformat ist ein allgemeiner Begriff, der einen Container zum Sammeln von E-Mail-Nachrichten darstellt. Die Nachrichten werden zusammen mit ihren Anhängen im Container gespeichert. Nachrichten aus einem ganzen Ordner werden in einer einzigen Datenbankdatei gespeichert und neue Nachrichten werden an das Ende der Datei angehängt. Zahlreiche Anwendungen und APIs unterstützen das MBox-Dateiformat wie Apple Mail und Mozilla Thunderbird.

## MBOX-Dateiformat ##

Das MBox-Dateiformat blieb ziemlich lange nicht standardisiert, bis 2005 die Anwendung/mbox als [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Nachrichten im RFC 2822-Format standardisiert wurde , werden innerhalb des MBox-Dateiformats nacheinander verkettet. Jede Nachricht beginnt mit einer Trennlinie, die den Absender der Nachricht identifiziert und auch das Datum und die Uhrzeit identifiziert, zu der die Nachricht vom endgültigen Empfänger empfangen wurde (entweder das Last-Hop-System im Übertragungspfad oder das System, das als das System des Empfängers dient Mailstore). Jede Nachricht wird typischerweise durch eine Leerzeile abgeschlossen. Das Ende der Datenbank wird normalerweise entweder durch das Fehlen zusätzlicher Daten oder durch das Vorhandensein einer expliziten Dateiendemarkierung erkannt.

## Lesen einer Nachricht aus einer MBox-Datei ##

Ein Reader durchsucht eine mbox-Datei und sucht nach From_-Zeilen. Jede From_-Zeile markiert den Anfang einer Nachricht. Der Leser sollte nicht versuchen, die Tatsache auszunutzen, dass jede From_-Zeile (nach dem Anfang der Datei) eine Leerzeile ist. Sobald das Lesegerät eine Nachricht findet, extrahiert es einen (möglicherweise beschädigten) Absender des Umschlags und ein Lieferdatum aus der From_-Zeile. Es liest dann bis zur nächsten From_-Zeile oder dem Dateiende, je nachdem, was zuerst eintritt. Es entfernt die letzte Leerzeile und löscht die Anführungszeichen von >From_-Zeilen und >>From_-Zeilen und so weiter. Das Ergebnis ist eine RFC 822-Nachricht.

## Codierungsüberlegungen ##

Der Inhalt einer MBox-Datei kann irreversibel vermischt werden, wenn eine empfangene E-Mail eine MBox-Datei als Anhang enthält und in einer anderen MBox-Datei gespeichert wird. Um dies zu vermeiden, müssen Messaging-Systeme eine mbox-Datenbank mit nicht transparenter Übertragungscodierung (z. B. BASE64 oder Quoted-Printable) codieren, wenn ein solches Objekt über Messaging-Protokolle übertragen wird. Implementierer sollten auch darauf vorbereitet sein, mbox-Daten lokal zu codieren, wenn nicht konforme Daten empfangen werden.

## Verweise ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

