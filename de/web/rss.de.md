{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "teilweise", "Erweiterung", "Datei", "Format", "Web", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Wirklich einfache Syndizierung",
  "description":"Erfahren Sie mehr über das RSS-Dateiformat und APIs, die RSS-Dateien erstellen und öffnen können.",
  "linktitle" :"RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Was ist eine RSS-Datei? ##

Eine Datei mit der Erweiterung .rss wird als Really Simple Syndication bezeichnet. RSS ist ein vom Computer leicht lesbarer Dateityp, die XML-Datei. Diese XML-Dateien werden bei Datenänderungen oder Aktualisierungen einer Website oder Webseite automatisch aktualisiert. Die aktualisierten Informationen zusammen mit den Metadaten (Name des Autors, Name des Herausgebers, Veröffentlichungsdatum usw.) und andere Webinhalte der Website werden aus den RSS-Dateien des Benutzers extrahiert und in einem leicht lesbaren Format dargestellt. Das Beste an diesen RSS-Dateien ist, dass sie in Echtzeit funktionieren und die Updates, Neuigkeiten, Veröffentlichungen, dh die neuesten, oben in der Datei angezeigt werden. Mithilfe einer RSS-Datei können Sie ganz einfach eine Datei erstellen, die die neuesten Aktualisierungen zu jedem Thema enthält, an dem Sie interessiert sind, indem Sie den zugehörigen Inhalt aus dem Internet ziehen und ihn mithilfe einer RSS-Datei lesen.

## Kurze Geschichte ##

Die eigentliche RSS-Datei wurde zuerst von Netscape erstellt, sie erfanden die erste Version der RSS-Datei, verwarfen dann aber die Idee und setzten nicht mit neueren Versionen fort. Es war dann die **Userland Software**, die am RSS-Dateiformat arbeitete und es mit einer neueren Version weiter innovierte, so kam RSS v2 auf den Markt. Die Erfindung von RSS kann jedoch auf das Resource Description Framework von Ramanathan V im Jahr 1997 zurückgeführt werden. Die Funktionsweise der beiden Dateien ist ziemlich ähnlich, und man kann mit Sicherheit davon ausgehen, dass das Konzept von RSS auf der Grundlage der Funktionsweise von RDF entwickelt wurde. ein Dateireader, der zum Sammeln von Metadaten verwendet wurde.

## Technische Spezifikation ##

Die RSS-Datei ist eine Art XML-Datei und alle RSS-Dateien müssen den Standards von XML 1.0 entsprechen. Es gibt verschiedene Versionen verschiedener RSS-Dateien, wie ua 0.91, 0.92, 2.0. Die Datei jeder Version entspricht den Spezifikationen und Standards dieser spezifischen Version.

## RSS-Beispiel ##

Das Folgende ist ein vereinfachtes Beispiel für RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Bezug ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
