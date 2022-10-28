{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Compressed Audio Video", "File", "Extension", "File Format", "Multimedia Container", "XVid", "DivX", "Codecs", "Resource Interchange File Format", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI-Dateiformat - Eine Audio-Video-Interleave-Datei",
  "description":"Erfahren Sie mehr über das AVI-Dateiformat und APIs, die AVI-Dateien erstellen und öffnen können.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine AVI-Datei? ##

Das **AVI**-Dateiformat ist ein Audio-Video-Multimedia-Container-Dateiformat, das von Microsoft eingeführt wurde. Es enthält die Audio- und Videodaten, die mit mehreren Codecs (Coder/Decoder) wie **XVid** und **DivX** erstellt und komprimiert wurden. Da zur Kodierung der AVI-Inhalte unterschiedliche Codecs verwendet werden können, sollten die abrufenden Anwendungen, zB AVI-Player, diese nur öffnen können, wenn sie die erforderlichen Codecs installiert haben, mit denen die AVI-Inhalte erstellt wurden. Das Format wird standardmäßig auf allen **Microsoft Windows**-Plattformen sowie auf fast allen anderen wichtigen Plattformen unterstützt. Mehrere Anwendungen und APIs bieten die Möglichkeit, AVI zu erstellen/zu speichern, zu lesen und in andere gängige Formate wie MP4, MOV, WMV usw. zu konvertieren.

## AVI-Dateiformat ##

Eine Datei mit der Erweiterung .avi ist eine AVI-Datei. Es ist ein Unterformat des Resource Interchange File Format (RIFF). RIFF organisiert Daten in Blöcken oder "Chunks", die mit einem FourCC-Tag gekennzeichnet sind. Eine AVI-Datei ist einfach ein "Stück" in einer RIFF-formatierten Datei.

Im ersten Sub-Chunk wird der Header der Datei durch das „hdrl“-Tag identifiziert; sein Inhalt umfasst die Breite, Höhe und Bildrate des Videos. Im zweiten Sub-Chunk repräsentiert das Motion-Tag die Framerate des Videos. Das AVI-Video besteht aus den eigentlichen audiovisuellen Daten in diesem Chunk. Außerdem gibt es noch einen dritten optionalen Subchunk mit dem „idx1“-Tag, der die Position der einzelnen zur Datei gehörenden Datenchunks innerhalb der Datei angibt.

### Einschränkungen ###

* Informationen zum Seitenverhältnis können in der ursprünglichen AVI-Spezifikation nicht kodiert werden, obwohl die spätere OpenDML-Spezifikation (AVI 2.0) eine standardisierte Methode bietet
* Obwohl AVI-Dateien in der Film- und Fernsehpostproduktion weit verbreitet sind, konkurrieren verschiedene Ansätze zum Hinzufügen eines Zeitcodes, was die Verwendbarkeit des Formats beeinträchtigt.
* Eine in AVI codierte Videodatei kann keine Komprimierungstechnik verwenden, die zukünftige Framedaten über das zu codierende Frame hinaus erfordert (B-Frame)
* Es ist problematisch, AVI-Dateien mit variablen Bitraten (VBR) zu verwenden (z. B. MP3-Audio mit Abtastraten unter 32 kHz).
* Eine AVI-Datei, die Spielfilme in Standardauflösung kodiert, wie sie normalerweise verwendet wird, verursacht wahrscheinlich einen Overhead von etwa 5 MB pro Stunde, je nachdem, wie die Datei verwendet wird
* Untertitel müssen in den Videostream fest codiert oder in einer separaten Datei verteilt werden, falls AVI-Dateien keine Anhänge wie Schriftarten und Untertitel aufnehmen können

## Kurze Geschichte ##

AVI wurde 1992 von Microsoft mit dem Ziel eingeführt, ein robusteres und fortschrittlicheres Audio- und Videodateiformat bereitzustellen. Das Format wurde mit der Nutzung des Internets schnell populär und ermöglichte es Einzelpersonen, Videodateien direkt und indirekt über Cloud-basierte Medienspeicher zu teilen.

## Verweise ##

* [AVI – von Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

