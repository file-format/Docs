{
"Datum": "21.06.2023",
  "keywords": [
"Unterdatei",
"Was ist eine Unterdatei",
"Beispiel einer MicroDVD-Untertiteldatei",
"Untertitelerweiterungen",
"Sub öffnen",
"Untertiteldateitypen",
"Wie öffnet man eine SUB-Datei",
"Datei",
"SUB-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SUB-Dateiformat – MicroDVD-Untertiteldatei",
  "description":"Erfahren Sie mehr über das SUB-Format und APIs, mit denen SUB-Dateien erstellt und geöffnet werden können.",
"linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub",
"parent": "video"
}
},
"lastmod": "21.06.2023"
}

## Was ist eine SUB-Datei?

Eine SUB-Datei ist ein MicroDVD-Untertiteldateiformat, das zur Anzeige von Untertiteln in Videos verwendet wird und normalerweise die Dateierweiterung .sub hat. Diese Dateien enthalten Zeitinformationen und Text für jeden Untertiteleintrag.

MicroDVD-Untertiteldateien verwenden ein einfaches textbasiertes Format, bei dem jeder Untertiteleintrag aus mehreren Zeilen besteht. Die erste Zeile enthält die Timing-Informationen des Untertitels, einschließlich der Start- und Endzeitstempel. Die nachfolgenden Zeilen enthalten den eigentlichen Untertiteltext.

Hier ist ein Beispiel einer MicroDVD-Untertiteldatei:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Untertitelerweiterungen

Untertitel können je nach Format unterschiedliche Dateierweiterungen haben. Einige gängige Dateierweiterungen für Untertitel sind:

- **.srt:** SubRip-Untertitelformat. Es ist eines der am weitesten verbreiteten Untertitelformate und wird von vielen Mediaplayern und Videobearbeitungsprogrammen unterstützt.
- **.sub:** Untertiteldateiformat, das von verschiedenen Untertitelformaten wie MicroDVD, SubViewer und SubStation Alpha verwendet werden kann.
- **.ass oder .ssa:** Erweitertes SubStation Alpha- oder SubStation Alpha-Untertitelformat. Es unterstützt erweiterte Funktionen wie Textformatierung, Positionierung und Effekte.
- **.vtt:** WebVTT-Format (Web Video Text Tracks), das zur Anzeige von Untertiteln in Webvideos verwendet wird. Es wird häufig mit HTML5-Videoplayern verwendet.
- **.idx/.sub:** Von DVD-Untertiteln verwendetes Format. Die .idx-Datei enthält Zeit- und Formatierungsinformationen, während die .sub-Datei den eigentlichen Untertiteltext enthält.
- **.smi oder .sami:** Synchronized Accessible Media Interchange-Format. Es wird häufig für Untertitel und Untertitel im Windows Media Player verwendet.

## Was versteht man unter "Open Sub"?

Open Sub bedeutet normalerweise OpenSubtitles, eine beliebte Online-Plattform, die Untertitel für Filme und Fernsehsendungen in mehreren Sprachen bereitstellt. Es bietet eine umfangreiche Sammlung von Untertiteldateien, die von seiner Benutzergemeinschaft bereitgestellt wurden. Sie können die OpenSubtitles-Website (www.opensubtitles.org) besuchen, um nach Untertiteln für Ihre gewünschten Filme oder Fernsehserien zu suchen und diese herunterzuladen.

## Untertitel-Dateitypen

Untertiteldateien gibt es in verschiedenen Formaten, jedes mit seinem eigenen Dateityp oder seiner eigenen Erweiterung. Hier sind einige gängige Untertiteldateitypen:

- **SubRip-Untertitelformat (.srt):** Dies ist eines der am häufigsten verwendeten Untertitelformate. SRT-Dateien sind reine Textdateien, die Untertiteleinträge mit Zeitstempeln und entsprechendem Text enthalten.
- **SubViewer-Untertitelformat (.sub):** SubViewer-Dateien ähneln SRT-Dateien, enthalten Untertiteleinträge mit Zeitstempeln und Text und unterstützen möglicherweise zusätzliche Funktionen wie Textformatierung und Farben.
- **SubStation Alpha (.ssa) und Advanced SubStation Alpha (.ass):** Diese Formate unterstützen erweiterte Funktionen wie Textformatierung, Stil, Positionierung und Animationseffekte. SSA- und ASS-Dateien werden häufig für Anime-Untertitel verwendet.
- **MicroDVD-Untertitelformat (.sub):** Das MicroDVD-Format verwendet .sub-Dateien und enthält Zeitinformationen und Text für jeden Untertiteleintrag. Es wird häufig mit Mediaplayern und Videobearbeitungssoftware verwendet.
- **DVD-Untertitel (.sub und .idx):** DVD-Untertitel bestehen normalerweise aus zwei Dateien: der .sub-Datei, die Untertiteltext enthält, und der .idx-Datei, die Zeit- und Formatierungsinformationen enthält.
- **WebVTT (.vtt):** WebVTT ist ein Untertitelformat für Webvideos, das häufig mit HTML5-Videoplayern verwendet wird und grundlegende Formatierungsoptionen unterstützt.
- **MPL2-Untertitelformat (.mpl):** MPL2-Dateien werden mit MPlayer, einem Mediaplayer für Unix-ähnliche Systeme, verwendet und enthalten Untertiteleinträge mit Zeitstempeln und Text.
- **iTunes Timed Text (.itt):** iTunes Timed Text-Dateien werden für Untertitel in Apples iTunes und anderen Apple-Plattformen verwendet. Sie unterstützen Funktionen wie Textstil und -positionierung.
- **Teletext-Untertitelformat (.srt oder .txt):** Teletext-Untertitel werden häufig im Rundfunkfernsehen verwendet. Sie werden normalerweise als reine Textdateien mit der Erweiterung .srt oder .txt gespeichert.

## Wie öffne ich eine SUB-Datei?

Die folgenden Mediaplayer können SUB-Dateien als Untertitelspur öffnen.

- VideoLAN VLC-Mediaplayer
- MPlayer

Um die SUB-Datei im VLC-Player zu öffnen, befolgen Sie diese Schritte

- Öffnen Sie den VLC-Player und spielen Sie Ihr Video ab
- Wählen Sie in der Menüleiste des VLC Media Players **Untertitel > Untertiteldatei hinzufügen ...**
- Navigieren Sie zur SUB-Datei und öffnen Sie sie

Wenn Sie die SUB-Datei bearbeiten müssen, können Sie sie mit einem beliebigen Texteditor öffnen, z. B. Microsoft Notepad (Windows) oder Apple TextEdit (Mac).

## Verweise
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

