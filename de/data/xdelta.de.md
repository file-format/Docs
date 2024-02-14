{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA-Datei – xdelta-Differenzdatei – Was ist eine .xdelta-Datei und wie öffnet man sie?",
  "description" : "XDELTA-Datei – xdelta-Differenzdatei – Was ist eine .xdelta-Datei und wie öffnet man sie?",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Was ist eine XDELTA-Datei?

Das XDELTA-Dateiformat enthält die binären Unterschiede zwischen zwei anderen Dateien und wird vom xdelta-Tool generiert, einem Befehlszeilendienstprogramm für die Delta-Kodierung, bei dem die Unterschiede zwischen zwei Dateien berechnet und diese Unterschiede in einem kompakten Format kodiert werden. XDELTA-Dateien speichern Binärdaten, die Änderungen oder Unterschiede zwischen der Originaldatei und der aktualisierten Datei darstellen. Die Binärdaten in einer XDELTA-Datei stellen die Änderungen dar, die erforderlich sind, um eine Datei (das Original) in eine andere Datei (die aktualisierte oder gepatchte Version) umzuwandeln.

XDELTA-Dateien werden in der Gaming-Community häufig verwendet, um Modifikationen (Mods) für Videospiele zu verteilen. Diese Mods können alles umfassen, von kosmetischen Änderungen bis hin zu erheblichen Änderungen in der Spielmechanik. Mit XDELTA-Dateien können Benutzer diese Änderungen auf ihre Spielinstallationen anwenden, indem sie die ursprünglichen Spieldateien mit den in der XDELTA-Datei angegebenen Änderungen patchen.

## xdelta

xdelta ist ein Befehlszeilendienstprogramm, das für die Delta-Kodierung und -Dekodierung verwendet wird; Es wird hauptsächlich zum Erstellen und Anwenden von Binärpatches, oft Delta-Patches oder Xdelta-Patches genannt, zwischen zwei Dateien verwendet. Diese Patches stellen Unterschiede zwischen der Originaldatei und der geänderten oder aktualisierten Version dar und ermöglichen eine effiziente Verteilung von Updates, insbesondere in Szenarien, in denen Bandbreite oder Speicherplatz begrenzt sind.

Hier ist ein kurzer Überblick über die Hauptfunktionen von xdelta:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

xdelta wird häufig in verschiedenen Szenarien verwendet, z. B. beim Verteilen von Software-Updates, beim Patchen von Videospielen und beim Aktualisieren von Systemdateien in eingebetteten Geräten oder Netzwerkgeräten. Es bietet eine flexible und effiziente Möglichkeit, Dateiaktualisierungen zu verwalten und gleichzeitig die Bandbreitennutzung und den Speicherbedarf zu minimieren.

## xdeltaui

xdeltaui ist eine grafische Benutzeroberflächenanwendung (GUI) zum Verwalten und Anwenden von XDELTA-Patches. xdelta gui bietet Benutzern eine benutzerfreundliche Oberfläche, über die sie mit XDELTA-Dateien interagieren und diese auf entsprechende Originaldateien anwenden können, um sie effektiv zu patchen oder zu aktualisieren.

Im Gegensatz zur Befehlszeilenversion von xdelta, die über textbasierte Befehle arbeitet, bietet xdeltaui eine intuitivere Möglichkeit, mit XDELTA-Dateien umzugehen, insbesondere für Benutzer, die mit Befehlszeilenschnittstellen nicht vertraut sind oder grafische Tools bevorzugen.

Mit xdeltaui können Benutzer in der Regel Aufgaben wie die Auswahl der Originaldatei, die Auswahl der XDELTA-Patchdatei und die Anwendung eines Patches zum Generieren einer aktualisierten Datei ausführen. Dies kann besonders nützlich sein, um Mods oder Updates für Videospiele oder andere Softwareanwendungen zu installieren.

## xdelta herunterladen

Auf Linux-Systemen können Sie Paketmanager wie apt, yum oder dnf verwenden, um xdelta zu installieren. Unter Ubuntu können Sie beispielsweise den folgenden Befehl verwenden:

```
sudo apt-get install xdelta3
```

## So verwenden Sie xdelta

Um xdelta zu verwenden, müssen Sie normalerweise die folgenden allgemeinen Schritte ausführen:

1.  **Herunterladen und installieren**: Stellen Sie zunächst sicher, dass xdelta auf Ihrem System installiert ist. Sie können es von der offiziellen Website, den Paketmanagern oder anderen vertrauenswürdigen Quellen herunterladen.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Patch erstellen**:
    
- Öffnen Sie Ihre Befehlszeilenschnittstelle (Terminal oder Eingabeaufforderung).
– Verwenden Sie den Befehl xdelta mit den entsprechenden Optionen, um einen Patch zu erstellen. Die grundlegende Syntax lautet:
               

xdelta delta<original_file><updated_file><patch_output_file>

        
Ersetzen Sie `<original_file> ` mit Pfad zur Originaldatei, `<updated_file> ` mit Pfad zur aktualisierten Datei und `<patch_output_file> ` mit dem gewünschten Namen für die Patchdatei.
- Beispiel:
               

xdelta delta ursprüngliche_datei aktualisierte_datei patch.xdelta

        
4.  **Anwenden eines Patches**:
    
- Stellen Sie sicher, dass Sie über die Originaldatei und die Patchdatei verfügen.
- Öffnen Sie Ihre Befehlszeilenschnittstelle.
– Verwenden Sie den Befehl xdelta mit den entsprechenden Optionen, um den Patch anzuwenden. Die grundlegende Syntax lautet:
        
      

xdelta-Patch<original_file><patch_file><output_file>

        
Ersetzen Sie `<original_file> ` mit Pfad zur Originaldatei, `<patch_file> ` mit Pfad zur Patch-Datei und `<output_file> ` mit dem gewünschten Namen für die Ausgabedatei.
- Beispiel:
                

xdelta-Patch Originaldatei patch.xdelta aktualisierte_Datei

        
5.  **Hilfe anzeigen**: Wenn Sie Hilfe zu bestimmten Optionen oder Befehlen benötigen, können Sie den Befehl xdelta mit der Option --help verwenden, um Nutzungsinformationen und verfügbare Optionen anzuzeigen.
    
## So öffnen Sie eine XDELTA-Datei

XDELTA-Dateien sind nicht zum direkten Öffnen gedacht. Wenn Sie einen XDELTA-Patch auf ein Spiel oder eine andere Datei anwenden möchten, haben Sie die Möglichkeit, entweder xdelta zu verwenden, das mit mehreren Plattformen kompatibel ist, oder xdelta UI, das speziell für Windows-Benutzer entwickelt wurde.

## Verweise
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


