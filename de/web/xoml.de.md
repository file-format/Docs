{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "Extensible Object Markup Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Windows-Workflow-Dateiformat",
  "description":"Erfahren Sie mehr über das XOML-Dateiformat und APIs, die XOML-Dateien erstellen und öffnen können.",
  "linktitle" :"XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine XOML-Datei?

XOML ist ein Akronym für Extensible Object Markup Language und ist ein Serialisierungsformat für die Workflowobjekte von Windows Workflow Foundation. Basierend auf **[XAML](/de/web/xaml/)** wird es hauptsächlich zum Erstellen von Benutzeroberflächen in reinem **[XML](/de/web/xml/)** verwendet. Diese werden verwendet, um den Workflow für die Benutzeroberfläche zu deklarieren, und werden zusammen mit der separaten Datei kompiliert, die die Implementierungslogik enthält. Es enthält eine baumbasierte Struktur, die einen Root-Workflow-Knoten, verschachtelte Unterelemente und eingebettete Codesegmente definiert. Wenn ein neuer Workflow mit Visual Studio für .NET erstellt wird, können Sie auswählen, ob er im Codeformat oder im durch Code getrennten Format vorliegen soll. Falls Sie die spätere auswählen, erstellt die IDE zwei Dateien für Sie; eine im XOML-Format (bestehend aus Workflow-Layout und -Einstellungen) und eine andere im Format [.CS](/de/programming/cs/)/[.VB](/de/programming/vb/), in dem sich der Programmiercode befindet.

