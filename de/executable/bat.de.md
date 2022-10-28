{
  "date" : "2021-06-24",
  "keywords" :[ "bat-Datei", "was ist eine bat-Datei", "Datei", "bat-Datei-Beispiel", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das BAT-Dateiformat und APIs, die BAT-Dateien erstellen und öffnen können.",
  "title" :"BAT - Stapeldateiformat",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Was ist eine BAT-Datei?
Eine BAT-Datei ist als Batch-Datei bekannt, die unter DOS und allen Windows-Versionen unter cmd.exe ausgeführt wird. Es besteht aus einer Reihe von Zeilenbefehlen im Klartext, die vom Befehlszeileninterpreter ausgeführt werden, um verschiedene Aufgaben auszuführen, z. B. das Ausführen von Wartungsdienstprogrammen in Windows oder das Starten typischer Programme. Eine Stapeldatei kann jeden Befehl enthalten, der vom Interpreter interaktiv akzeptiert werden kann, und die Codestruktur verwenden, die bedingte Verzweigungen und Schleifen ermöglicht, wie sie in der Stapeldatei geschrieben sind.
## BAT-Dateiformat
Ein BAT-Dateiformat ist einfach ein Skript, das zur Automatisierung von sich wiederholenden Befehlssequenzen eingebaut wird. Der Begriff "Batch" wird für die Stapelverarbeitung verwendet, die als "nicht interaktive Ausführung" betrachtet werden kann. Daher darf eine Stapeldatei keinen Stapel mit mehreren Daten verarbeiten. Im alten Disk Operating System (DOS) wurde die Batchdatei unter der Befehlszeilenschnittstelle ausgeführt, indem der Dateiname und die Erweiterung .bat eingegeben wurden. Das frühere auf einer grafischen Benutzeroberfläche von Microsoft basierende Betriebssystem wie Microsoft Windows war von DOS abhängig. Die Benutzer mussten DOS verwenden, um typische Operationen wie das Reparieren, Optimieren oder Neuinstallieren von Windows durchzuführen. Später führte Microsoft Windows NT ein, das nicht vom DOS-Betriebssystem abhängig war. Daher können die Batchdateien mit der Eingabeaufforderung oder **cmd.exe** in den modernen Microsoft-Betriebssystemen ausgeführt werden.
### Batch-Dateiparameter
Die Eingabeaufforderung unterstützt eine Reihe spezieller Variablen wie **%0, %1 bis %9**, um auf den Namen und Pfad des Batch-Jobs und die neun Aufrufparameter innerhalb des Batch-Jobs zu verweisen. Nicht vorhandene Parameter werden durch einen String der Länge Null ersetzt. Sie können zwar ähnlich wie Umgebungsvariablen verwendet werden, werden aber nicht in der Umgebung gespeichert. Microsoft und IBM bezeichnen diese Variablen als Ersatzparameter, während Novell, Digital Research und Caldera den Begriff Ersatzvariablen für sie eingeführt haben.

Hier sind einige nützliche Batch-Dateibefehle:
| Befehl | Beschreibung |
------|------------|
| VER | Dieser Stapelbefehl zeigt die Version von MS-DOS an, die Sie verwenden. |
|ASSOC| Dies ist ein Stapelbefehl, der eine Erweiterung einem Dateityp (FTYPE) zuordnet, vorhandene Zuordnungen anzeigt oder eine Zuordnung löscht. |
|CD| Dieser Stapelbefehl hilft bei Änderungen an einem anderen Verzeichnis oder zeigt das aktuelle Verzeichnis an. |
|CLS| Dieser Stapelbefehl löscht den Bildschirm. |
|KOPIE| Dieser Stapelbefehl wird zum Kopieren von Dateien von einem Speicherort zum anderen verwendet. |
|DEL| Dieser Stapelbefehl löscht Dateien und keine Verzeichnisse. |
|DIR| Dieser Stapelbefehl listet den Inhalt eines Verzeichnisses auf. |
|DATUM| Dieser Stapelbefehl hilft, das Systemdatum zu finden. |
|ECHO| Dieser Stapelbefehl zeigt Meldungen an oder schaltet das Befehlsecho ein oder aus. |
|BEENDEN| Dieser Stapelbefehl beendet die DOS-Konsole. |
|MD| Dieser Stapelbefehl erstellt ein neues Verzeichnis am aktuellen Speicherort. |
|BEWEGEN| Dieser Stapelbefehl verschiebt Dateien oder Verzeichnisse zwischen Verzeichnissen. |
|PFAD| Dieser Stapelbefehl zeigt die Pfadvariable an oder legt sie fest. |
|PAUSE| Dieser Stapelbefehl fordert den Benutzer auf und wartet auf die Eingabe einer Eingabezeile. |
|AUFFORDERUNG| Dieser Stapelbefehl kann verwendet werden, um die Eingabeaufforderung cmd.exe zu ändern oder zurückzusetzen. |
|RD| Dieser Stapelbefehl entfernt Verzeichnisse, aber die Verzeichnisse müssen leer sein, bevor sie entfernt werden können. |
|REN| Benennt Dateien und Verzeichnisse um |
|REM| Dieser Stapelbefehl wird für Anmerkungen in Stapeldateien verwendet und verhindert, dass der Inhalt der Anmerkung ausgeführt wird. |
|START| Dieser Stapelbefehl startet ein Programm in einem neuen Fenster oder öffnet ein Dokument. |
|ZEIT| Dieser Stapelbefehl stellt die Uhrzeit ein oder zeigt sie an. |
|TYP| Dieser Stapelbefehl gibt den Inhalt einer oder mehrerer Dateien in die Ausgabe aus. |
|VOL| Dieser Stapelbefehl zeigt die Datenträgerbezeichnungen an. |
|ATTRIB| Zeigt die Attribute der Dateien im aktuellen Verzeichnis an oder setzt sie |
|CHKDSK| Dieser Stapelbefehl überprüft die Festplatte auf Probleme. |
|WAHL| Dieser Stapelbefehl stellt dem Benutzer eine Liste mit Optionen bereit. |
|CMD| Dieser Stapelbefehl ruft eine weitere Instanz der Eingabeaufforderung auf. |
|COMP| Dieser Stapelbefehl vergleicht 2 Dateien basierend auf der Dateigröße. |
|KONVERTIEREN| Dieser Stapelbefehl konvertiert ein Volume vom FAT16- oder FAT32-Dateisystem in das NTFS-Dateisystem. |
|TREIBERABFRAGE| Dieser Stapelbefehl zeigt alle installierten Gerätetreiber und ihre Eigenschaften an. |
|ERWEITERUNG| Dieser Stapelbefehl extrahiert Dateien aus komprimierten .cab-CAB-Dateien. |
|FINDEN| Dieser Stapelbefehl sucht nach einer Zeichenfolge in Dateien oder Eingaben und gibt übereinstimmende Zeilen aus. |
|FORMATIEREN| Dieser Stapelbefehl formatiert eine Festplatte, um ein von Windows unterstütztes Dateisystem wie FAT, FAT32 oder NTFS zu verwenden, wodurch der vorherige Inhalt der Festplatte überschrieben wird. |
|HILFE| Dieser Stapelbefehl zeigt die Liste der von Windows bereitgestellten Befehle. |
|IPKONFIG| Dieser Stapelbefehl zeigt die Windows-IP-Konfiguration an. Zeigt die Konfiguration nach Verbindung und den Namen dieser Verbindung an. |
|LABEL| Dieser Stapelbefehl fügt eine Datenträgerbezeichnung hinzu, legt sie fest oder entfernt sie. |
|MEHR| Dieser Stapelbefehl zeigt den Inhalt einer oder mehrerer Dateien bildschirmweise an. |
|NETZ| Stellt je nach verwendetem Befehl verschiedene Netzwerkdienste bereit. |
|PING| Dieser Stapelbefehl sendet ICMP/IP-Echopakete über das Netzwerk an die angegebene Adresse. |
|HERUNTERFAHREN| Dieser Stapelbefehl fährt einen Computer herunter oder meldet den aktuellen Benutzer ab. |
|SORTIEREN| Dieser Stapelbefehl nimmt die Eingabe aus einer Quelldatei und sortiert ihren Inhalt alphabetisch, von A bis Z oder von Z bis A. Er gibt die Ausgabe auf der Konsole aus. |
|SUBST| Dieser Stapelbefehl weist einem lokalen Ordner einen Laufwerksbuchstaben zu, zeigt aktuelle Zuweisungen an oder entfernt eine Zuweisung. |
|SYSTEMINFO| Dieser Stapelbefehl zeigt die Konfiguration eines Computers und seines Betriebssystems. |
|AUFGABENKILL| Dieser Stapelbefehl beendet eine oder mehrere Aufgaben. |
|AUFGABENLISTE| Dieser Stapelbefehl listet Aufgaben auf, einschließlich Aufgabenname und Prozess-ID (PID). |
|XCOPY| Dieser Stapelbefehl kopiert Dateien und Verzeichnisse auf fortgeschrittenere Weise. |
|BAUM| Dieser Stapelbefehl zeigt eine Baumstruktur aller Unterverzeichnisse des aktuellen Verzeichnisses mit beliebiger Rekursionsebene oder Tiefe an. |
|FC |Dieser Stapelbefehl listet die tatsächlichen Unterschiede zwischen zwei Dateien auf. |
|DISKPART |Dieser Stapelbefehl zeigt und konfiguriert die Eigenschaften von Plattenpartitionen. |
|TITLE |Dieser Stapelbefehl legt den im Konsolenfenster angezeigten Titel fest. |
|EINSTELLEN | Zeigt die Liste der Umgebungsvariablen auf dem aktuellen System an. |

## BAT-Datei Beispiel
Batch-Skripte werden normalerweise als einfache Textdateien gespeichert; enthält Befehle, die in einer Sequenz ausgeführt werden. Diese Dateien werden mit der Erweiterung .bat gespeichert; erkannt und ausgeführt, indem die Software **Command Interpreter** verwendet wird. Diese Software ist nativ in Microsoft Windows unter dem Namen **cmd.exe** verfügbar.

Hier ist ein Beispiel-Batch-Skript, das alle Dateien im aktuellen Verzeichnis löscht:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Verweise

* [Batch-Skript – Kurzanleitung](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Batch-Datei – von Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

