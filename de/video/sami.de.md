{
"Datum": "16.05.2023",
  "keywords": [
"Sami-Datei",
"Was ist eine Sami-Datei",
"Beispiel einer Sami-Datei",
"Datei",
"Sami-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SAMI-Dateiformat – Untertitel- und Metadaten-Austauschdatei",
  "description":"Erfahren Sie mehr über das SAMI-Format und die APIs, mit denen SAMI-Dateien erstellt und geöffnet werden können.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Was ist eine SAMI-Datei?

Eine Datei mit der Erweiterung ".sami" bezieht sich normalerweise auf eine SAMI-Datei (Subtitles And Metadata Interchange). SAMI ist ein Untertitelformat, das zum Anzeigen von Untertiteln oder Untertiteln in Videos verwendet wird. Es wurde ursprünglich von Microsoft für den Windows Media Player entwickelt.

SAMI-Dateien enthalten Timing-Informationen und Textinhalte für Untertitel oder Untertitel, sodass sie mit einer Videowiedergabe synchronisiert werden können. Das Format unterstützt grundlegende Formatierungsoptionen wie Schriftart, Farbe und Positionierung der Untertitel auf dem Bildschirm.

SAMI-Dateien sind normalerweise reine Textdateien und können mit einem Texteditor geöffnet und bearbeitet werden. Der Inhalt einer SAMI-Datei umfasst typischerweise einen Header-Abschnitt, der Informationen über die Datei bereitstellt, gefolgt von einzelnen Untertiteleinträgen mit ihrem jeweiligen Timing und Text.

Hier ist ein Beispiel dafür, wie eine SAMI-Datei aussehen könnte:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI-Dateien werden häufig in Verbindung mit Videoplayern oder Mediaplayern verwendet, die die Anzeige von Untertiteln unterstützen, wie z. B. Windows Media Player oder VLC Media Player. Der Player liest die SAMI-Datei und synchronisiert die Untertitel mit dem Videoinhalt, sodass Zuschauer die Untertitel lesen können, während sie das Video ansehen.

## Unterstützte HTML-Tags

SAMI-Dateien (Subtitles And Metadata Interchange) unterstützen einen begrenzten Satz HTML-ähnlicher Tags zum Formatieren und Gestalten der Untertitel. Hier sind einige der häufig verwendeten Tags, die von SAMI unterstützt werden:

- ``<SAMI> :`` Das Stammelement, das die gesamte SAMI-Datei kapselt.
- ``<HEAD> :`` Enthält Header-Informationen für die SAMI-Datei.
<html>- ``<TITLE> :`` Gibt den Titel der SAMI-Datei an. </html>
- ``<BODY> :`` Schließt die Untertiteleinträge und ihre Zeitinformationen ein.
- ``<SYNC> :`` Stellt einen Synchronisierungspunkt für einen Untertiteleintrag dar. Es gibt den Zeitpunkt an, zu dem der Untertitel angezeigt werden soll.
- ``<P> :`` Schließt den eigentlichen Textinhalt eines Untertitels ein. Es wird typischerweise innerhalb von a verwendet<SYNC> Block.
<html>- `` <FONT>:`` Definiert Schriftarteigenschaften für den eingeschlossenen Text. Attribute wie Farbe, Gesicht, Größe und Stil können verwendet werden, um das Erscheinungsbild der Schriftart zu ändern.</font>
- ``<BR> :`` Fügt einen Zeilenumbruch innerhalb eines Untertitels ein.
<html>- `` <B>:`` Stellt den eingeschlossenen Text fett dar.</b>
<html>- `` <I>:`` Gibt den eingeschlossenen Text kursiv wieder.</i>
<html>- `` <U>:`` Stellt den eingeschlossenen Text unterstrichen dar.</u>
- ``<C> :`` Gibt die Position oder Ausrichtung des Untertiteltextes auf dem Bildschirm an. Es unterstützt Attribute wie "Mitte", "Mitte", "Links", "Rechts", "Oben", "Unten" und deren Kombinationen.
- ``<LANG> :`` Gibt den Sprachcode für den Untertiteltext an. Es hilft bei der Identifizierung der Sprache der Untertitel.

Dies sind einige der grundlegenden Tags, die von SAMI-Dateien unterstützt werden. Es ist wichtig zu beachten, dass SAMI nicht alle HTML-Tags und -Attribute unterstützt. Die unterstützten Tags konzentrieren sich in erster Linie auf die Gestaltung und Positionierung der Untertitel und nicht auf die umfassende Strukturierung oder Interaktivität des Dokuments.

## Verweise
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

