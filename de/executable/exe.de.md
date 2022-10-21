{
  "date" : "2021-06-30",
  "keywords" :[ "exe-Datei", "exe-Dateiformat", "was ist eine exe-Datei", "Datei", "exe-Beispiel", "exe-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Eine .exe-Datei ist eine ausführbare Microsoft-Datei, die unter Windows ausgeführt wird. Erfahren Sie mehr über das EXE-Dateiformat.",
  "title" :"Was ist eine ausführbare EXE-Datei?",
  "linktitle" :"EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Was ist eine EXE-Datei?

Das Wort EXE ist die Abkürzung für **ausführbar**. Eine .exe-Datei ist ein Programm, das auf dem Microsoft Windows-Betriebssystem ausgeführt werden kann. Anwendungsentwickler veröffentlichen ihre Programme für Windows-Betriebssysteme meist im ausführbaren Format als exe-Dateien. Es ist das Standarddateiformat zum Ausführen von Anwendungen unter Windows. **Setup.exe**, **Install.exe** und **cmd.exe** sind einige gebräuchliche und bekannte Namen von EXE-Dateien.

## EXE-Dateiformat

MS-DOS-Compiler wurden mit den Speichermodellen mit der Speicherbeschränkung von 64 KB eingeführt. Das allgemeine Konzept besteht darin, unterschiedliche Segmentregister in der x86-CPU (CS, DS, ES, SS) so einzustellen, dass sie auf die unterschiedlichen oder gleichen Segmente zeigen, wodurch verschiedene Grade des Zugriffs auf den Speicher ermöglicht werden. Einige spezifische Speichermodelle waren:

- **Tiny**: Alle Speicherzugriffe sind 16-Bit (Segmentregister unverändert). Erzeugt eine .COM-Datei anstelle einer .EXE-Datei.
- **Small**: Alle Speicherzugriffe sind 16-Bit (Segmentregister unverändert).
- **Kompakt**: Datenadressen enthalten sowohl Segment als auch Offset, laden die DS- oder ES-Register beim Zugriff neu und erlauben bis zu 1 MB an Daten. Codezugriffe ändern das CS-Register nicht, wodurch 64 KB Code zugelassen werden.
- **Mittel**: Codeadressen enthalten die Segmentadresse, laden CS beim Zugriff neu und erlauben bis zu 1 MB Code. Datenzugriffe ändern die DS- und ES-Register nicht, wodurch 64 KB an Daten zugelassen werden.
- **Groß**: Sowohl Code- als auch Datenadressen sind (Segment-, Offset-)Paare, wobei die Segmentadressen immer neu geladen werden. Der gesamte Speicherplatz von 1 MB steht sowohl für Code als auch für Daten zur Verfügung.
- **Riesig**: Wie das große Modell, wobei der Compiler zusätzliche Arithmetik generiert, um den Zugriff auf Arrays mit mehr als 64 KB zu ermöglichen.

Die Entwickler müssen beim Erstellen einer exe-Datei entscheiden, welches Modell ausgewählt werden soll.

### Portables EXE-Dateiformat

Das portable ausführbare Dateiformat (PE) enthält eine Reihe von informativen Headern, die folgende Liste der Header:

- **DOS-Header**: Der MS-DOS-Header gewährleistet entweder die Abwärtskompatibilität oder die ordnungsgemäße Ablehnung neuer Dateitypen.
- **PE-Header**: Bei Offset 60 (0x3C) vom Anfang des DOS-Headers befindet sich ein Zeiger auf den PE-Datei-Header
- **COFF-Header**: Der COFF-Header enthält einige Informationen, die für eine ausführbare Datei nützlich sind, und einige Informationen, die für eine Objektdatei nützlicher sind.
- **PE Optional Header**: Der PE Optional Header tritt direkt nach dem COFF-Header auf, und einige Quellen zeigen sogar, dass die beiden Header Teil derselben Struktur sind.
- **Abschnittstabelle**: Unmittelbar nach dem optionalen PE-Header finden wir eine Abschnittstabelle. Die Abschnittstabelle besteht aus einem Array von IMAGE_SECTION_HEADER-Strukturen.
- **Mappable Sections**: Kann Speicherplatz sparen, indem der Code einer Bibliothek mehr als einem Prozess zugeordnet wird.

## Können Sie eine EXE-Datei auf einem Mac ausführen?

Exe-Dateien werden unter Mac OS nicht als ausführbare Dateien verwendet. Wenn Sie jedoch eine exe-Datei unter Mac OS ausführen möchten, können die folgenden Methoden verwendet werden.

1. **Wine** - Wine ist die perfekte Lösung für Leute, die ihre PC-Anwendungen auf Mac-Systemen verwenden möchten. Es ist ein Akronym, das für "Wine Is Not A Emulator" steht und bedeutet. Wine erstellt die gleiche Umgebung von Verzeichnissen wie sie von Microsoft verwendet wird, sodass Sie Ihre Windows-Anwendung damit ausführen können.
2. **Virtuelle Maschinen** – Erstellen Sie eine virtuelle Windows-Maschine mit Parallel Desktop oder VM Virtual Box und führen Sie Ihre Anwendung innerhalb der virtuellen Maschine aus.
3. **Boot Camp** – Durch Installieren und Konfigurieren von Windows Boot Camp unter Mac OS können Sie das Windows-Betriebssystem auf einem Mac-Computer ausführen.

## Verweise

* [.exe- von Wikipedia](https://en.wikipedia.org/wiki/.exe)
* [x86-Disassemblierung/ausführbare Windows-Dateien](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

