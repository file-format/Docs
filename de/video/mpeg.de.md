{
"Datum": "12.07.2023",
  "keywords": [
"mpeg",
"MPEG-Datei",
"Was ist eine MPEG-Datei",
"Wie öffnet man eine MPEG-Datei",
"Datei",
"mpeg-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MPEG-Dateiformat – MPEG-Video",
  "description":"Erfahren Sie mehr über das MPEG-Format und APIs, mit denen MPEG-Dateien erstellt und geöffnet werden können.",
"linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg",
"parent": "video"
}
},
"lastmod": "12.07.2023"
}

## Was ist eine MPEG-Datei?

Eine MPEG-Datei, auch MPEG-Videodatei genannt, ist ein digitales Videodateiformat, das die MPEG-Standards (Moving Picture Experts Group) für die Videokomprimierung verwendet. MPEG ist ein weit verbreitetes Format zum Speichern und Übertragen von Videodaten.

Das MPEG-Format verwendet eine verlustbehaftete Komprimierung, was bedeutet, dass einige Informationen verworfen werden, um die Dateigröße zu reduzieren. Diese Komprimierungstechnik ermöglicht eine effiziente Speicherung und Streaming von Videoinhalten bei gleichzeitiger Beibehaltung einer angemessenen Videoqualität. Es gibt mehrere Versionen des MPEG-Standards, darunter MPEG-1, MPEG-2, MPEG-4 und MPEG-7, jeweils mit unterschiedlichen Komprimierungs- und Qualitätsstufen.

MPEG-Dateien haben normalerweise die Dateierweiterung ".mpeg" oder ".mpg". Sie können sowohl Video- als auch Audiodaten enthalten, oft kombiniert in einer einzigen Datei. MPEG-Dateien sind mit einer Vielzahl von Mediaplayern und Videobearbeitungsprogrammen kompatibel und daher eine beliebte Wahl für die gemeinsame Nutzung und Verbreitung von Videoinhalten.

## Wie öffne ich eine MPEG-Datei?

Es stehen zahlreiche Softwareanwendungen zur Verfügung, mit denen MPEG-Dateien geöffnet und abgespielt werden können. Hier sind einige beliebte Optionen:

- VLC Media Player
- Windows Media Player
- QuickTime-Player
- MPC-HC
- GOM-Spieler
- MPlayer
- PotPlayer
- Kodi

## Wie konvertiert man eine MPEG-Datei?

Es gibt eine Reihe von Videoanwendungen, darunter VideoLAN VLC Media Player, HandBrake und Apple QuickTime Player, die MPEG-Dateien in andere Formate konvertieren können. VLC kann beispielsweise MPEG-Dateien in diese Formate konvertieren

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## Überblick über die interne Struktur von MPEG-Dateien

Die interne Struktur von MPEG-Dateien besteht aus verschiedenen Komponenten und Datenstrukturen, die Video-, Audio- und andere verwandte Informationen organisieren und speichern. Hier ist ein Überblick über die Schlüsselelemente in der internen Struktur von MPEG-Dateien:

- **Systemschicht:**

Die Systemschicht definiert die Gesamtstruktur der MPEG-Datei. Es umfasst Header, Programmströme und andere systembezogene Daten, die für die Dekodierung und Wiedergabe erforderlich sind. Die Systemschicht ist für die Verwaltung der Synchronisierung und des Multiplexens elementarer Streams verantwortlich.

- **Elementare Streams:**

MPEG-Dateien enthalten separate Elementarstreams für Video, Audio und andere Datentypen. Jeder Elementarstrom trägt komprimierte Daten, die für seinen Typ spezifisch sind. Beispielsweise enthält der Video-Elementarstrom komprimierte Videobilder und der Audio-Elementarstrom enthält komprimierte Audio-Samples.

- **Video-Kompression:**

MPEG-Videokomprimierungstechniken wie Intra-Frame- und Inter-Frame-Komprimierung werden verwendet, um die Dateigröße zu reduzieren und gleichzeitig die Videoqualität beizubehalten. Die komprimierten Videobilder werden in Bildgruppen (GOPs) organisiert, die aus intracodierten (I), vorhergesagten (P) und bidirektionalen (B) Bildern bestehen.

- **Audiokomprimierung:**

MPEG-Dateien unterstützen verschiedene Audiokomprimierungscodecs wie MP3, AAC oder MPEG-1 Audio Layer II. Die Audio-Samples werden mit diesen Codecs komprimiert, was eine effiziente Speicherung und Übertragung von Audiodaten ermöglicht.

- **Synchronisation und Timing:**

MPEG-Dateien verwenden Zeitstempel und Synchronisierungsinformationen, um eine ordnungsgemäße Ausrichtung zwischen Video- und Audiostreams während der Wiedergabe sicherzustellen. Diese Zeitstempel tragen zur Aufrechterhaltung der Synchronisierung bei und bieten ein genaues Timing für die Dekodierung und Wiedergabe von Audio- und Videobildern.

- **Metadaten:**

MPEG-Dateien können Metadaten enthalten, die zusätzliche Informationen über den Video- und Audioinhalt liefern. Diese Metadaten können Details wie Titel, Autor, Erstellungsdatum und andere beschreibende Informationen enthalten.

- **Pakete und Pack-Header:**

MPEG-Dateien organisieren Daten in Paketen. Jedes Paket enthält einen Pack-Header, der Informationen über den Inhalt des Pakets bereitstellt, z. B. den Stream-Typ, die Paketgröße und Timing-Informationen.

- **Programmspezifische Informationen (PSI):**

PSI ist ein Abschnitt in MPEG-Dateien, der zusätzliche Informationen zu den Programmstreams enthält, wie z. B. Programm- und Stream-IDs, Stream-Typ und Deskriptoren. PSI hilft beim Dekodieren und Demultiplexen der Elementarströme innerhalb der Datei.

- **Transportstrom:**

Bei MPEG-2 gibt es ein spezielles Transportstromformat, das zur Ausstrahlung und Übertragung von Videoinhalten verwendet wird. Der Transportstrom multiplext mehrere Programme in einen einzigen Stream und ermöglicht so eine effiziente Übertragung und Synchronisierung von Audio-, Video- und anderen Daten über Netzwerke.

## MPEG-Dateiformat – Weitere Informationen

Hier sind einige wichtige Dinge, die Sie über das MPEG-Dateiformat wissen sollten:

- **Kompression:**

MPEG-Dateien verwenden verlustbehaftete Komprimierungstechniken, um die Dateigröße zu reduzieren und gleichzeitig eine angemessene Videoqualität beizubehalten. Der Grad der Komprimierung kann je nach MPEG-Version und verwendeten Einstellungen variieren.

- **Video und Audio:**

MPEG-Dateien können sowohl Video- als auch Audiodaten enthalten. Die Videodaten werden mit MPEG-Standards komprimiert, während der Ton mit verschiedenen Audio-Codecs wie MP3 oder AAC komprimiert werden kann.

- **MPEG-Versionen:**

Es gibt verschiedene Versionen des MPEG-Standards, darunter MPEG-1, MPEG-2, MPEG-4 und MPEG-7. Jede Version verfügt über eigene Spezifikationen, Funktionen und Komprimierungsstufen. MPEG-1 wird üblicherweise für VCDs (Video-CDs) verwendet, während MPEG-2 für DVDs und Fernsehsendungen verwendet wird. MPEG-4 wird häufig für Online-Video-Streaming verwendet, und MPEG-7 konzentriert sich auf die Beschreibung und Metadaten von Multimedia-Inhalten.

- **Dateierweiterungen:**

MPEG-Dateien haben normalerweise die Dateierweiterungen ".mpeg" oder ".mpg". Es können jedoch unterschiedliche Variationen und Erweiterungen existieren, beispielsweise ".mp4" für MPEG-4-Dateien oder ".mp3" für MPEG-1 Audio Layer 3-Dateien.

- **Plattformübergreifende Kompatibilität:**

MPEG-Dateien werden von verschiedenen Mediaplayern, Betriebssystemen und Geräten weitgehend unterstützt. Sie können auf Windows-, Mac- und Linux-Systemen sowie auf Smartphones, Tablets und Smart-TVs gespielt werden.

- **Bearbeitung:**

MPEG-Dateien können mit Videobearbeitungssoftware bearbeitet werden. Da MPEG jedoch eine verlustbehaftete Komprimierung verwendet, kann eine wiederholte Bearbeitung und Neukodierung der Datei zu einer Verschlechterung der Qualität führen. Oft wird empfohlen, vor einer umfangreichen Bearbeitung mit verlustfreien Formaten zu arbeiten oder Sicherungskopien zu erstellen.

- **Streaming:**

MPEG-Dateien werden häufig zum Streamen von Videoinhalten über das Internet verwendet. Insbesondere MPEG-4 ist aufgrund seiner effizienten Komprimierung und seines guten Verhältnisses von Qualität zu Größe bei Online-Videoplattformen und Video-Sharing-Websites beliebt.

- **Weiterentwicklung der Standards:**

Die MPEG-Standards entwickeln sich ständig weiter, um mit dem technologischen Fortschritt Schritt zu halten. Neuere Versionen und Variationen wie MPEG-4 Part 10 (auch bekannt als H.264 oder AVC) und MPEG-4 Part 14 (MP4) bieten eine verbesserte Komprimierungseffizienz und Unterstützung für erweiterte Funktionen wie hochauflösendes Video und 3D-Inhalte.

- **Multimedia-Anwendungen:**

MPEG-Dateien finden in verschiedenen Bereichen Anwendung, darunter digitales Fernsehen, Streaming-Dienste, Videokonferenzen, Videoüberwachung, Multimedia-Präsentationen und mehr.

## MPEG im Vergleich zu anderen Formaten

Beim Vergleich des MPEG-Dateiformats mit anderen Videoformaten spielen mehrere Faktoren eine Rolle, darunter Komprimierungseffizienz, Kompatibilität, Funktionen und Unterstützung. Hier ist ein Vergleich von MPEG mit einigen gängigen Videoformaten:

### MPEG vs. AVI (Audio Video Interleave)

- **Kompression:**
   

MPEG-Dateien bieten im Vergleich zu AVI im Allgemeinen eine höhere Komprimierungseffizienz, was zu kleineren Dateigrößen führt.

- **Kompatibilität:**

AVI-Dateien werden von verschiedenen Mediaplayern weitgehend unterstützt, MPEG-Dateien weisen jedoch eine breitere Kompatibilität zwischen Geräten und Plattformen auf.

- **Merkmale:**

MPEG-Dateien unterstützen häufig erweiterte Funktionen wie mehrere Audiospuren, Untertitel und Kapitel, während AVI solche Funktionen nur begrenzt unterstützt.

- **Videoqualität:**

Abhängig von den Komprimierungseinstellungen können MPEG und AVI eine ähnliche Videoqualität erzielen, MPEG bietet jedoch aufgrund fortschrittlicher Komprimierungstechniken oft eine bessere Qualität bei niedrigeren Bitraten.

### MPEG vs. WMV (Windows Media Video):

- **Kompression:**

WMV-Dateien bieten im Allgemeinen eine bessere Komprimierungseffizienz im Vergleich zu MPEG, was zu kleineren Dateigrößen bei gleichzeitig guter Videoqualität führt.

- **Kompatibilität:**

MPEG-Dateien weisen eine breitere Kompatibilität zwischen verschiedenen Geräten und Plattformen auf, während WMV-Dateien hauptsächlich mit Windows-basierten Systemen verknüpft sind.

- **Merkmale:**

Beide Formate unterstützen eine Reihe von Funktionen, einschließlich mehrerer Audiospuren und Untertitel. MPEG bietet jedoch häufig mehr Vielseitigkeit und eine umfassendere Unterstützung für erweiterte Funktionen.

- **Videoqualität:**

Mit ähnlichen Komprimierungseinstellungen können MPEG und WMV eine vergleichbare Videoqualität erzielen, WMV kann jedoch aufgrund seiner fortschrittlichen Komprimierungstechniken in bestimmten Szenarien eine bessere Leistung erbringen.

### MPEG vs. MP4 (MPEG-4 Teil 14):

- **Kompression:**

Sowohl MPEG als auch MP4 verwenden ähnliche Komprimierungstechniken und die Komprimierungseffizienz kann vergleichbar sein. Allerdings bietet MPEG-4 Part 10 (H.264/AVC) in MP4 oft eine bessere Komprimierung als ältere MPEG-Formate.

- **Kompatibilität:**

Sowohl MPEG als auch MP4 weisen eine weitreichende Kompatibilität zwischen Geräten und Plattformen auf. MP4 hat in den letzten Jahren aufgrund seiner breiten Unterstützung und Akzeptanz erheblich an Popularität gewonnen.

- **Merkmale:**

MP4 bietet erweiterte Funktionen und Möglichkeiten, einschließlich Unterstützung für Untertitel, Kapitel, interaktive Menüs und erweiterte Video-Codecs wie H.264 und HEVC (H.265). MPEG-4 Teil 2 (DivX, Xvid) in MP4 unterstützt auch erweiterte Funktionen.

- **Videoqualität:**

MPEG und MP4 können bei Verwendung vergleichbarer Komprimierungseinstellungen eine ähnliche Videoqualität erzielen. Die Unterstützung fortschrittlicherer Videocodecs durch MP4 ermöglicht jedoch eine bessere Qualität bei niedrigeren Bitraten.

## Verweise
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)

