{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC-Datei - Google Docs-Verknüpfung",
  "description":"Erfahren Sie, was eine GDOC-Datei und APIs sind, die GDOC-Dateien erstellen und öffnen können.",
  "linktitle" :"GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Was ist eine GDOC-Datei?

Eine GDOC-Datei ist eine Verknüpfungsdatei, die auf eine Datei verweist, die sich auf Google Drive befindet, einem Cloud-basierten Dokumentenspeicherdienst. Wenn der Google Drive-Client auf einem Computer installiert ist und darin ein Dokument erstellt wird, erstellt das Laufwerk ein Dokument im Online-Cloud-Speicher und schreibt die [URL](/de/web/url/) dieses Dokuments in die GDOC-Datei im lokalen Google Drive-Ordner. Wenn auf diese Verknüpfungsdatei doppelgeklickt wird, öffnet der Standard-Webbrowser das Dokument vom Speicherort [URL](/de/web/url/). Wenn diese Verknüpfungsdatei aus diesem Ordner verschoben wird, wird die Verknüpfung zum Online-Dokument unterbrochen.

## GDOC-Dateiformat - Weitere Informationen

Die GDOC-Datei enthält eine Verknüpfung zum Online-Dokument, das im Dateiformat [JSON](/de/web/json/) geschrieben ist. Der Browser, der GDOC-Dateien öffnet, liest die URL-Informationen und öffnet das verknüpfte Dokument zur Anzeige, sofern der Benutzer in diesem Google-Konto angemeldet ist, in dem das Dokument gespeichert ist. GDOC-Dateien enthalten nicht den Inhalt des Dokuments.

### Beispiel für eine GDOC-Datei

Die GDOC-Datei kann in einem Texteditor geöffnet werden und ihr Inhalt sieht wie folgt aus.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Wie zu sehen ist, sind die Inhalte in JSON formatiert und haben die URL eines Dokuments und die zugehörige Dokument-ID.

## Verweise

* [Google Docs öffnet weder gdoc- noch docx-Dateien](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

