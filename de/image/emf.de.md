{
  "date" : "2019-10-11",
  "keywords" :[ "emf-Datei", "emf-Dateiformat", "was ist eine emf-Datei", "Datei", "emf-Beispiel", "emf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Erweitertes Metafile-Format",
  "description":"Erfahren Sie mehr über das EMF-Dateiformat und APIs, die EMF-Dateien erstellen und öffnen können.",
  "linktitle" :"EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine EMF-Datei?

**Enhanced Metafile Format (EMF)** speichert grafische Bilder geräteunabhängig. Metadateien von EMF bestehen aus Datensätzen variabler Länge in chronologischer Reihenfolge, die das gespeicherte Bild nach dem Analysieren auf jedem Ausgabegerät wiedergeben können. Diese Datensätze mit variabler Länge können Definitionen eingeschlossener Objekte, Zeichenbefehle und Grafikeigenschaften sein, die für die genaue Wiedergabe des Bildes entscheidend sind. Wenn ein Gerät eine EMF-Metadatei mit seiner eigenen Grafikumgebung öffnet, bleiben die Proportionen, Abmessungen, Farben und andere Grafikeigenschaften des Originalbilds gleich, unabhängig von der Plattform des öffnenden Geräts.

## Kurze Geschichte ##

1990 entwarf Microsoft ein Bilddateiformat Windows Metafile ([WMF](/de/image/wmf/)) für Microsoft Windows. Windows-Metadateien sind 16-Bit-Formate, die einige Bitmap-Komponenten enthalten können. WMF kann aus Vektorgrafiken bestehen und soll zwischen verschiedenen Anwendungen portabel bleiben. 1993 kündigte Win32/GDI das Enhanced Metafile (EMF) an, eine neuere Version mit verbesserter Flexibilität und Skalierbarkeit. EMF wird auch als Grafiksprache verwendet, um die Druckertreiber auszuführen. Microsoft empfiehlt jetzt das erweiterte Metadateiformat (EMF) gegenüber dem Windows-Format (WMF). Als Windows XP eingeführt wurde, wurde die Version Enhanced Metafile Format Plus (EMF+) veröffentlicht. Diese neuere Version findet ihren Weg, indem GDI+ API-Aufrufe ebenso serialisiert werden wie WMF/EMF-Aufzeichnungsaufrufe an GDI. Es gibt eine gzip-komprimierte Version von EMF, die als EMZ bekannt ist.

## EMF-Metafile-Format ##

Im Folgenden sind die wesentlichen Elemente des erweiterten Metafile-Formats aufgeführt:

* Ein EMR_HEADER (Version, Größe, die Auflösung des Bildes bei der Erstellung)
* Eine Tabelle für GDI-Objekte
* Eine reservierte Palette (optional)
* Metafile-Datensätze in Array-Struktur angeordnet (Eigenschaftseinstellungen, definierte Objekte, Zeichenbefehle)
* EMR_EOF-Datensatz (letzter Datensatz in der EMF-Metadatei)

## EMF-Versionen ##
* **Original**: Die Originalversion gibt den Datensatz an, der erforderlich ist, um das Originalbild aufzubewahren und seine Geräteunabhängigkeit beizubehalten. Darüber hinaus unterstützt der Datensatz mit Grafikobjekten und Befehlen zum Zeichnen.
* **Version 1**: Die zweite Version von EMF verbesserte die Flexibilität und Geräteunabhängigkeit, indem der Datensatz für das Pixelformat und die Bereitstellung zur Verwendung des OpenGL-Befehls hinzugefügt wurden.
* **Version 2**: Die dritte Version verbesserte die Genauigkeit, indem das metrische System hinzugefügt wurde, um die Entfernungen der Geräteoberfläche zu messen, wodurch die Aufzeichnung skalierbarer wurde.

## Erweiterte Metafile-Datensätze ##

Metafile-Datensätze sind in Form eines Arrays angeordnet. Diese Datensätze haben eine ENHMETARECORD-Struktur und eine variable Länge. ENHMETARECORD gibt Daten an, die GDI-Funktionen definieren, um ein Bild mit erweitertem Metadateiformat zu erstellen. **ENHMETAHEADER**-Struktur ist immer der erste Datensatz in diesem Format. Dieser EMF-Header enthält die folgenden Informationen.

Jeder Datensatz der erweiterten Metadatei hat am Anfang zwei Mitglieder von EMR (stellt die Basisstruktur bereit). Das erste Mitglied erkennt die GDI-Funktion (Parameter werden im Datensatz verwendet), die den Typ des Datensatzes bestimmt und als iType bekannt ist. Der andere Member nSize definiert die Größe jedes Datensatzes. Verbleibende Parameter (falls vorhanden) und zusätzliche Daten, die unmittelbar unter nSize angeordnet sind. Unmittelbar nach der Kopfzeile kann eine optionale Textbeschreibung vorhanden sein. Der Name des Bildes und des Autors wird in dieser Textbeschreibung festgehalten. Die Palette, deren Vorhandensein eine Option ist, gibt die Farben an, die bei der erweiterten Metadateierstellung verwendet werden. Die anderen Datensätze werden verwendet, um die GDI-Funktion zu spezifizieren, die bei der Bilderzeugung wesentlich ist.

In jeder Metadatei sollte mindestens ein EMF-Datensatz vorhanden sein. Die Traversierungsinformationen von einem Datensatz zum anderen hängen von EMF-Datensätzen ab, sodass diese Datensätze nebeneinander angeordnet werden müssen. Bei jedem gegebenen Datensatz in der Metadatei mit Ausnahme von EOF_record definiert die Länge dieses bestimmten Datensatzes, dass zum nächsten Datensatz übergegangen wird.

## Verbesserte Erstellung von Metadateien ##

Die Funktion **CreateEnhMetaFile** wird verwendet, um eine erweiterte Metadatei zu erstellen. Diese Funktionsargumente werden für die Dimensionierung und Speicherung des Bildes auf der Festplatte/im Speicher verwendet. Außerdem benötigt diese Funktion die Dimension des Geräts, in dem das Bild zuerst erschienen ist (referenziertes Gerät) und den Kontext des Referenzgeräts (DC). Daher müssen die Argumente zur Behandlung dieses DC beim Aufruf der **CreateEnhMetaFile**-Funktion bereitgestellt werden. Die Syntax der Funktion lautet wie folgt:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** Handle auf ein Referenzgerät.

**lptoFilename:** Ein Zeiger auf den Dateinamen.

**lprc:** Zeiger auf ovale Struktur gibt die Bildabmessungen in mm an.

**lpDesc:** ein Zeiger auf eine Zeichenkette für den Titel des Bildes und den Namen der Anwendung, die das Bild erstellt hat.

## Erweiterte Metadatei-Operationen ##

Im Folgenden sind Jobs aufgeführt, die mithilfe des Handles für eine erweiterte Metadatei ausgeführt werden können.

* Anzeigen und Bearbeiten für das gespeicherte Bild.
* Produzieren Sie erweiterte Metafile-Kopien.
* Abrufen der Kopie eines EMF-Headers, einer optionalen Beschreibung und einer binären Version einer erweiterten Metadatei
* Rekapitulieren Sie die Farben in der Palette.

## Grafikobjekte ##

Bei Zeichen- und Malvorgängen können Grafikobjekte durch Objekterzeugungsdatensätze erstellt und zur weiteren Verwendung gespeichert werden. Ein `EMR_SELECTOBJECT`-Datensatz kann diese Grafikobjekte unter Verwendung des Kontexts des Wiedergabegeräts abrufen. Stifte, Paletten, Pinsel, Farbräume, Schriftarten und Bestandsobjekte sind einige wiederverwendbare Objekttypen.

## Byte-Reihenfolge ##

Das Little-Endian-Format wird verwendet, um Daten in Metadatei-Datensätzen zu speichern.

## Versionierung ##

Das EMF-Dateiformat wurde zweimal überarbeitet. Die geänderten Versionen sind Original, Erweiterung 1 und Erweiterung 2. Erweiterte Versionen haben Vorkehrungen für OpenGL-Einträge und einen optionalen Deskriptor für das interne Pixelformat. Bei angezeigten Maßen ist eine Maßeinheit in Millilitern hinzugefügt.

## Verweise ##

* [Metadateien im erweiterten Format | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Enhanced Metafile Format and Specification](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

