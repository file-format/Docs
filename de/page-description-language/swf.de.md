{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "Datei", "Erweiterung", "Format", "Videoformat", "Was ist eine SWF-Datei", "SWF-Dateiformat", "SWF-Dateiplayer", "So öffnen Sie eine SWF-Datei"] ,
  "title" :"SWF-Datei - Shockwave Flash Movie-Dateiformat",
  "description":"Erfahren Sie, was eine SWF-Datei ist, und APIs, die erstellt werden können, und zeigen Sie, wie die SWF-Datei geöffnet wird.",
  "linktitle" :"SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine SWF-Datei?

Eine SWF-Datei ist eine Animationsdatei, die mit Adobe Flash erstellt wird. Es kann verschiedene Arten von Elementen wie Text, Vektorbilder, Rasterbilder, Actionscripts, Objekte wie Kreise, Linien, Quadrate und Rechtecke enthalten, um die Animation zu erstellen. SWF-Dateien ordnen diese Multimediaelemente in Frames an, die mit unterschiedlichen Frames pro Sekunde (fps) wiedergegeben werden können. SWF bedeutet Short Web File, ist aber auch für das Shockwave-Format bekannt.

Zu den Anwendungen, die *SWF-Dateien öffnen** konnten, gehörten Adobe Flash Player (jetzt eingestellt) und Eltima Elmedia Player.

## SWF-Dateiformat – Weitere Informationen

SWF-Dateien wurden verwendet, um als Binärdateien auf Disc gespeichert zu werden. Das SWF-Dateiformat wurde verwendet, um Animationen und Spiele zu entwickeln, die in Websites eingebettet und auch unabhängig gespielt werden konnten. Es unterstützte auch Videos und Sounds, die Entwicklern viele Möglichkeiten zur Erstellung interaktiver Multimedia-Anwendungen boten. SWF-Dateien können in Webbrowsern abgespielt werden, auf denen Adobe Shockwave installiert ist. Adobe Flash wurde im Dezember 2020 aufgrund seiner Mängel und Sicherheitsprobleme eingestellt.

## Kurze Geschichte des SWF-Dateiformats

Das SWF-Dateiformat wurde ursprünglich von FutureWave Software entwickelt, um Animationen anzuzeigen, die auf einer Player-Software auf jedem System mit langsameren Netzwerkverbindungen ausgeführt werden sollen, während die Dateigröße klein bleibt. Im Dezember 1996 übernahm Macromedia FutureWave und wechselte zu Macromedia Flash 1.0.

Im Jahr 2005 wurde Macromedia von Adobe übernommen, das SWF 2008 als Teil seines Open-Source-Projekts ankündigte. Im selben Jahr veröffentlichte Adobe Code für weltweit beliebte Web-Engines, um ihnen das Crawlen und Indizieren von SWF-Dateien zu ermöglichen. Da SWF-Dateien jedoch ein Standardformat für die Veröffentlichung von Flash-Inhalten im Internet zu werden scheinen, wurde SWF in „Small Web Format“ geändert.

## SWF-Dateistruktur

Der Pfad ist das grundlegende grafische Element in SWF, bei dem es sich um eine Abfolge von Segmenten grundlegender Elemente handelt, die von einfachen Linien bis hin zu Bezier-Kurven reichen. Diese einfachen Elemente helfen auch, andere zusätzliche Grundelemente wie Würfel, Ellipsen und sogar Texte zu erstellen. Die grafischen Grundelemente in SWF haben Ähnlichkeit mit den grafischen Elementen anderer Formate wie SVG und MPEG-4 BIFS.

Listen anzeigen und bereits definierte Elemente wiederverwenden/umbenennen, erlaubt das Format ebenfalls. Das binäre Stream-Format von SWF kann mit QuickTime-Atomen verglichen werden, die in Bezug auf Tag, Größe und Nutzlast ähnlich sind. Das binäre Stream-Format ermöglicht es älteren Spielern, nicht unterstützte Inhalte zu überspringen. Obwohl Originalversionen von SWF darauf beschränkt waren, Vektorgrafiken und Bilder anzubieten, erlauben neue Versionen daher auch Audio- und Videoinhalte.

Eine neue Low-Level-3D-API des Flash Players namens „Stage3D“ wurde in Version 11 eingeführt. Diese API war als Gegenstück zu OpenGL oder Direct3D gedacht. Stage3D definiert Farben in einer Low-Level-Sprache namens Adobe Graphics Assembly Language (AGAL). Im Folgenden sind einige grundlegende Datentypen des SWF-Dateiformats aufgeführt.

### Koordinaten

XY-Koordinaten im SWF-Dateiformat werden als ganze Zahlen gespeichert und in einer Einheit namens Twip gemessen. Ein Twip besteht aus 1/20 eines logischen Pixels. Logisches Pixel und Bildschirmpixel sind gleich, wenn die Datei ohne Skalierung auf 100 % abgespielt wird.

### Integer-Typen und Byte-Reihenfolge

Die vorzeichenbehafteten und vorzeichenlosen Integer-Typen von 8, 16, 32 und 64 Bit sind im SWF-Dateiformat zulässig. Die Little-Endian-Byte-Reihenfolge wird verwendet, um ganzzahlige Werte zu speichern. Obwohl innerhalb von Bytes, wird die Bitreihenfolge in Big-Endian gespeichert. Alle ganzzahligen Werte sollten Byte-ausgerichtet sein. Vorzeichenbehaftete Ganzzahlen werden durch Verwendung herkömmlicher 2er-Komplement-Bitmuster dargestellt.

### Festkommazahlen

Das SWF-Dateiformat unterstützt zwei Arten von Festkommazahlen, nämlich 32 und 16 Bit.

### Gleitkommazahlen

SWF 8 und neuere Versionen verwenden drei Arten von Gleitkommazahlen (FLOAT, FLOAT 16, DOUBLE), die mit dem IEEE-Standard 754 für Gleitkommazahlen kompatibel sind.

### Kodierte Ganzzahlen

Ein Typ von codierter Ganzzahl wird von SWF 9 und höher mit einer variablen Anzahl von Bytes unterstützt.

## Verweise

* [SWF-Dateiformat](https://en.wikipedia.org/wiki/Swf)

