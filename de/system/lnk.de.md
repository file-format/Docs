{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "Erweiterung", "Datei", "Format", "System", "LNK-Datei", "Link", "LNK-Dateien", "LNK-Dokumente", "Anwendung", "Programme" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Link-Dateiformat",
  "description":"Erfahren Sie mehr über das LNK-Dateiformat und APIs, die LNK-Dateien erstellen und öffnen können.",
  "linktitle" :"LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Was ist eine LNK-Datei? ##

Eine LNK-Datei, analog zu einer Identität auf dem Mac-System, ist eine Windows-Alternative oder ein „Link“, der als Verbindung zu einem ursprünglichen Bilddokumentordner oder -programm dient. Es enthält den Typ, die Position und den Dateinamen des Verknüpfungsziels sowie die Anwendung, die das Zieldokument öffnet, und eine zusätzliche Tastenkombination.

Wählen Sie in Windows direkt eine Datei, einen Ordner oder ein ausführbares Programm und wählen Sie Verknüpfung erstellen. Der Speicherort des Dateiformats und das Verzeichnis „Anfang“ sind zwei grundlegende Merkmale von LNK-Dateien. Das Dateiformat von LNK-Dateien ist maskiert und ein gekrümmter Pfeil zeigt an, dass es sich um Verknüpfungen handelt.

## LNK-Dateiformat ##

LNK-Dateiformate haben normalerweise das gleiche Symbol wie ihre Zieldateien, jedoch mit einem kleinen gebogenen Pfeil, der anzeigt, dass die Datei auf einen anderen Speicherort verweist. Wenn auf die Verknüpfung doppelgeklickt wird, verhält sie sich so, als ob der Benutzer auf die eigentliche Datei doppelgeklickt hätte.

LNK-Dateien, die Anwendungsverknüpfungen enthalten, können Eigenschaften haben, die sich auf die Ausführung des Programms auswirken. Um die Attribute zu ändern, klicken Sie mit der rechten Maustaste auf die Verknüpfungsdatei und wählen Sie **Eigenschaften**, und ändern Sie dann das Feld Ziel.

LNK-Dateien sind keine Dateierweiterungen, sondern Windows Explorer-Erweiterungen. Als Terminalerweiterung können .lnk-Dokumente nur im Windows Explorer verwendet werden, um eine Datei zu ersetzen, und sie haben im Windows Explorer noch andere Zwecke, als als Verknüpfung zu einem lokalen Dokument zu dienen. Auch diese Dateien beginnen mit dem Buchstaben „L“.

Obwohl Verknüpfungen bei ihrer Erstellung mit bestimmten Dateien und Verzeichnissen verknüpft sind, können sie unbrauchbar werden, wenn das Ziel an einen anderen Speicherort geändert wird. Der Explorer beginnt mit der Reparatur eines Verknüpfungsordners, der beim Öffnen auf ein totes Ziel verweist.


## Technische Spezifikation ##

Nur wenn die Ordneranzeigeeinstellung „Erweiterungen für erkannte Dateitypen ausblenden“ deaktiviert ist, zeigt Windows die Dokumenterweiterung .lnk nicht für Dokumentverknüpfungen an. Obwohl dies nicht empfohlen wird, können Sie die Anzeige der Dateierweiterung aktivieren, indem Sie die Eigenschaft „NeverShowExt“ aus dem Windows-Registrierungseintrag der Datei HKEY_CLASSES_ROOT\lnk entfernen.

Gehen Sie dazu folgendermaßen vor:

* Öffnen Sie "Registration Editor", indem Sie "Regedit" in das Suchfeld der Taskleiste eingeben und das Programm auswählen
* Navigieren Sie in der Anwendung zum Speicherort Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Erstellen Sie eine Sicherungskopie des Elements, indem Sie mit der rechten Maustaste darauf klicken und Exportieren auswählen
* Wählen und löschen Sie das Attribut "NeverShowExt".
* Windows sollte neu gestartet werden


## Bezug ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
