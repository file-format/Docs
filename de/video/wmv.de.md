{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV-Dateiformat",
  "description":"Erfahren Sie mehr über das WMV-Dateiformat und APIs, die WMV-Dateien erstellen und öffnen können.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Was ist eine WMV-Datei?

Das Advanced Systems Format (ASF) ist ein digitaler Multimedia-Container, der hauptsächlich zum Speichern und Übertragen von Medienströmen entwickelt wurde. Microsoft Windows Media Video (WMV) ist das komprimierte Videoformat und Microsoft Windows Media Audio (WMA) ist das komprimierte Audioformat zusammen mit zusätzlichen Metadaten im von Microsoft entwickelten ASF-Container. Sobald die WMV- oder WMA-Dateien mit Windows Media Video- und Windows Media Audio-Codecs codiert sind, werden sie mit der Erweiterung .asf dargestellt. WMV komprimiert große Dateien für eine bessere Übertragungsrate über ein Netzwerk, während die Videoqualität erhalten bleibt. WMV wurde speziell entwickelt, um auf allen Windows-Geräten ausgeführt zu werden. Nach der Standardisierung durch die Society of Motion Picture and Television Engineers (SMPTE) gilt WMV heute als offenes Standardformat.

## Geschichte ##

Mit Hilfe von Microsoft-eigenen Codecs wurde 1999 ein neues komprimiertes Videoformat namens WMV7 entwickelt, das auf MPEG-4 Teil 2 basierte. Verbesserungen wurden in zwei weiteren Versionen hinzugefügt, nämlich WMV8 und 9. Microsoft hat eine 9^^th^^-Version eingereicht von WMV zu SMPTE zur Standardisierung im Jahr 2003, das schließlich 2006 als SMPTE 421M, auch bekannt als VC-1, standardisiert wurde. Die Idee hinter WMV war die Entwicklung eines Medienformats, das von der gesamten von Microsoft unterstützten Hardware und Software unterstützt werden kann. Darüber hinaus war ein weiterer wichtiger Zweck, Videostreams in einem optimalen Szenario über das Internet zu übertragen. Nach der Standardisierung von SMPTE wurde WMV auch ein Videoformat für Blu-ray-Discs.

## Dateiformatspezifikationen

### Behälter

Im Allgemeinen wird WMV in einen ASF-Container gepackt, aber zusätzlich können Matroska oder AVI-Container es auch mit den Erweiterungen .mkv bzw. .avi unterstützen.

### Windows Media-Video 9

Obwohl in der Windows Media Video 9-Serie verschiedene Audio- und Video-Codecs für das Authoring und die Wiedergabe digitaler Medien verfügbar sind, ist der WMV-9-Codec der neueste und beste Video-Codec, da er die optimale Komprimierung bei sehr niedrigen Bitraten, dh 160x, erreichen kann 120 bei 10 Kbps bis 1920 x 1080 bei 4-8 Mbps für eine Vielzahl von HD-Videos.

### Codec-Struktur

WMV-9 hat ein internes 8-Bit-4:2:0-Farbformat. Wie alle anderen gängigen Videokomprimierungsstandards MPEG-1 und H.261 verwendet WMV-9 eine blockbasierte Bewegungskompensation und ein räumliches Transformationsschema. Im Allgemeinen können wir sagen, dass diese Standards eine Block-für-Block-Bewegungskompensation aus dem vorherigen rekonstruierten Frame mit Hilfe einer 2-D-Größe durchführen, die als Bewegungsvektor (MV) bezeichnet wird, um die räumliche Verschiebung zu signalisieren. Der aktuelle Block wird mit Hilfe der Vorhersage der Werte aus dem vorherigen rekonstruierten Einzelbild gleicher Größe gebildet, das von der aktuellen Position um den Bewegungsvektor verschoben ist. Schließlich wird der Restfehler als Differenz zwischen dem bewegungskompensierten vorhergesagten Block und dem tatsächlichen Block berechnet. Dieser Restfehler wird unter Verwendung einer linearen Energieverdichtungstransformation transformiert, dann quantisiert und entropiecodiert.

Quantisierte Transformationskoeffizienten werden entropiedecodiert, dequantisiert und invers transformiert, um eine Näherung des Restfehlers auf der Decodiererseite zu erzeugen, die dann zu der bewegungskompensierten Vorhersage hinzugefügt wird, um die Rekonstruktion zu erzeugen. Die allgemeine Beschreibung des Codecs ist in der folgenden Abbildung dargestellt.

Der Rest des Abschnitts behandelt die neuen Verbesserungen in WMV-9, die es von den übrigen Videokodierungslösungen wie MPEG-Standards unterscheiden. WMV-9 hat Intra- (I), vorhergesagte (P) und bidirektional vorhergesagte (B) Frames. Intraframes sind diejenigen, die unabhängig codiert werden und keine Abhängigkeit von anderen Frames haben. Vorhergesagte Frames sind Frames, die von einem Frame in der Vergangenheit abhängen. Die Decodierung eines vorhergesagten Frames kann nur erfolgen, nachdem alle Referenzframes vor dem aktuellen Frame, beginnend mit dem jüngsten (I) Frame, decodiert wurden. B-Frames sind Frames, die zwei Referenzen haben – eine in der zeitlichen Vergangenheit und eine in der zeitlichen Zukunft. B-Frames werden nach ihren Referenzen übertragen, was bedeutet, dass B-Frames außerhalb der Reihenfolge gesendet werden, um sicherzustellen, dass ihre Referenzen zum Zeitpunkt der Decodierung verfügbar sind. B-Frames in WMV-9 werden nicht als Referenz für nachfolgende Frames verwendet. Dadurch werden B-Frames außerhalb der Decodierschleife platziert, sodass während der Decodierung von B-Frames Abkürzungen ohne Drift oder langfristige visuelle Artefakte genommen werden können. Die obige Definition von I-, P- und B-Frames gilt sowohl für progressive als auch für Interlaced-Sequenzen.

Die Leistung von Video-Codecs wird mit ihrem Ratenverzerrungsdiagramm (RD) verglichen. Es ist eine 2-D-Kurve, die die durch die Komprimierung bei einer bestimmten Bitrate erzeugte Verzerrung zeigt.

WMV-9 hat dieses Problem mit der Einführung einer Vielzahl von Techniken angegangen, die unten aufgeführt sind:

1. Adaptive Blockgrößentransformation

2. Transformationssatz mit begrenzter Genauigkeit

3. Bewegungskompensation

4. Quantisierung und Dequantisierung

5. Fortgeschrittene Entropiecodierung

6. Schleifenfilterung

7. Erweiterte B-Frame-Codierung

8. Interlace-Codierung

9. Überlappungsglättung

10. Low-Rate-Tools

11. Fading-Kompensation

## Verweise ##

* [https://bytescout.com/blog/2014/10/windows-media-videoformat.html](https://bytescout.com/blog/2014/10/windows-media-videoformat.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


