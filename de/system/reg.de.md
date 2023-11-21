{
"Datum": "07.03.2023",
  "keywords": [
"Reg-Datei",
"Was ist eine Reg-Datei?",
"Datei",
"reg-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "REG-Dateiformat – Windows-Registrierungsdatei",
  "description":"Erfahren Sie mehr über das REG-Format und APIs, mit denen REG-Dateien erstellt und geöffnet werden können.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent": "system"
}
},
"lastmod": "07.03.2023"
}

## Was ist eine REG-Datei?

Eine REG-Datei ist ein Dateiformat, das zum Importieren oder Exportieren von Windows-Registrierungsdaten verwendet wird. Die Windows-Registrierung ist eine hierarchische Datenbank, die Konfigurationseinstellungen und Optionen für das Windows-Betriebssystem und installierte Anwendungen speichert. Die Registrierung enthält Informationen wie Benutzereinstellungen, Anwendungseinstellungen, Hardware- und Softwarekonfigurationsdaten und mehr.

Eine REG-Datei hat normalerweise die Dateierweiterung ".reg" und ist eine reine Textdatei, die eine Reihe von Registrierungseinträgen und -werten in einem bestimmten Format enthält. Das Format besteht aus einem Header-Abschnitt, der die Datei als Registrierungsdatei identifiziert, gefolgt von einer Reihe von Schlüssel-Wert-Paaren, die Registrierungseinträge darstellen.

## REG-Dateiformat – Weitere Informationen

Hier ist ein Beispiel für ein reg-Dateiformat:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Die erste Zeile der Datei gibt die Version des Registrierungseditors an. Die folgenden Zeilen enthalten die Registrierungseinträge im Format eines Schlüsselpfads, gefolgt von einem Wertnamen und Wertdaten. In diesem Beispiel enthält die Reg-Datei zwei Einträge: einen, der ein Programm namens "Example.exe" zur Windows-Startliste hinzufügt, und einen anderen, der den Wert "Versteckt" in den erweiterten Einstellungen des Windows Explorers auf "true" setzt.

Reg-Dateien können mit einem Texteditor wie Notepad erstellt und bearbeitet werden. Sie werden häufig zu Sicherungs- und Wiederherstellungszwecken sowie zum Konfigurieren mehrerer Computer mit denselben Registrierungseinstellungen verwendet.

## Importieren oder exportieren Sie die Windows-Registrierung

Eine REG-Datei ist ein Dateityp, der zum Importieren oder Exportieren von Daten aus der Windows-Registrierung verwendet wird. Die Windows-Registrierung ist eine hierarchische Datenbank, die Konfigurationseinstellungen und Optionen für das Windows-Betriebssystem und installierte Anwendungen speichert. Die Registrierung enthält Informationen wie Benutzereinstellungen, Anwendungseinstellungen, Hardware- und Softwarekonfigurationsdaten und mehr.

Reg-Dateien können zum Erstellen oder Ändern von Registrierungseinträgen verwendet werden. Sie werden häufig zu Sicherungs- und Wiederherstellungszwecken sowie zum Konfigurieren mehrerer Computer mit denselben Registrierungseinstellungen verwendet. So fügen Sie mit einer Reg-Datei einen neuen Registrierungseintrag zur Windows-Registrierung hinzu:

1. Erstellen Sie eine neue Textdatei mit einem Texteditor wie Notepad.
2. Geben Sie den Registrierungseintrag im richtigen Format ein. Das Format besteht aus einem Header-Abschnitt, der die Datei als Registrierungsdatei identifiziert, gefolgt von einer Reihe von Schlüssel-Wert-Paaren, die Registrierungseinträge darstellen. Hier ist ein Beispiel:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Dadurch wird ein neuer Schlüssel mit dem Namen "Example" unter dem Schlüssel "Software" in der Registrierungsstruktur des aktuellen Benutzers erstellt und der Wert "Setting1" auf "Value1" gesetzt.

3. Speichern Sie die Datei mit der Dateierweiterung .reg.
4. Doppelklicken Sie auf die .reg-Datei, um den neuen Registrierungseintrag zur Windows-Registrierung hinzuzufügen.

Sie werden aufgefordert zu bestätigen, dass Sie den Eintrag zur Registrierung hinzufügen möchten. Nach der Bestätigung wird der neue Eintrag zur Registrierung hinzugefügt und Sie können ihn mit dem Registrierungseditor-Tool überprüfen.

## Verweise
* [Windows-Registrierung](https://en.wikipedia.org/wiki/Windows_Registry)

