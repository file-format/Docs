{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das AHK-Dateiformat und APIs, die AHK-Dateien erstellen und öffnen können.",
  "title" :"AHK-Dateiformat - AutoHotkey-Skriptdatei",
  "linktitle" :"AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Was ist eine AHK-Datei?

Eine AHK-Datei ist eine mit der AutoHotkey-Softwareanwendung generierte Skriptdatei, die zur Automatisierung von Aufgaben in Microsoft Windows verwendet wird. Es enthält Anweisungen zur Automatisierung von Aufgaben mithilfe von Tastenkombinationen, mit denen sofortige Aktionen ausgeführt werden können. Die Datei wird von AutoHotkey ausgeführt und alle Aktionen werden nacheinander ausgeführt. AHK-Dateien sind leistungsfähig genug, um komplexe Aufgaben mit den mit den Hotkeys definierten Hotkeys auszuführen. AHK-Dateien können mit Texteditoren wie Microsoft Notepad und Notepad++ geöffnet werden.

## AHK-Dateiformat

AHK-Dateien werden als reine Textdateien auf der Disc gespeichert und enthalten Codezeilen, die von AutoHotkey ausgeführt werden können. AutoHotkey ist eine kostenlose Open-Source-Skriptsprache und ermöglicht es Benutzern, einfache bis komplexe Skripts zu erstellen, um Aktionen wie das Ausfüllen von Formularen, automatisches Klicken, Ausführen von Makros usw. auszuführen. Eine AHK-Datei kann mindestens eine einzelne Aktion ausführen und dann beendet werden .

Es sind Tools verfügbar, mit denen AHK in [Exe](/de/executable/exe/)-Dateien konvertiert werden kann.

### AHK-Beispiel

Im folgenden Beispiel wird die Taste Win+Z verwendet, um Microsoft Notepad auszuführen oder in den Vordergrund zu bringen, wenn es bereits ausgeführt wird.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Wie erstelle ich eine AHK-Datei?

Die folgenden Schritte können verwendet werden, um eine AHK-Datei zu erstellen. Diese gehen davon aus, dass AutoHotkey bereits auf dem Rechner installiert ist.

* Klicken Sie mit der rechten Maustaste auf Ihren Desktop.
* Finden Sie "Neu" im Menü.
* Klicken Sie im Menü "Neu" auf "AutoHotkey-Skript".
* Geben Sie dem Skript einen neuen Namen.
* Suchen Sie die neu erstellte Datei auf Ihrem Desktop und klicken Sie mit der rechten Maustaste darauf.
* Klicken Sie auf „Skript bearbeiten“.
* Ein Fenster sollte aufgetaucht sein, wahrscheinlich Notepad.
* Speicher die Datei.

## Verweise

* [AutoHotkey](https://www.autohotkey.com/)
* [Batch-Datei – von Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

