{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "Dateiformat", "Dateityp", "was ist eine .asa-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP-Konfigurationsdatei",
  "description" :"Erfahren Sie, was eine ASA-Datei und APIs sind, die ASA-Dateien erstellen und öffnen können.",
  "linktitle" :"ALS EIN",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Was ist eine ASA-Datei?

Eine ASA-Datei ist eine Konfigurationsdatei, die für [ASP](/de/web/asp/)/ASP.NET-Projekte erstellt wurde. Es enthält Deklarationen von Variablen, Contains und Funktionen, die auf globaler Ebene in der Anwendung zugänglich sein sollen. Alle Seiten im Projekt können auf diese Variablen und Funktionen zugreifen, wodurch das Erfordernis, diese neu zu schreiben, vermieden wird. Ein solches Beispiel ist die Seite Global.asa, die im Stammverzeichnis gespeichert ist, damit sie von anderen Seiten der ASP-Website aufgerufen werden kann. Global.asa-Dateien sind optional, aber wenn sie verwendet werden, kann jede Anwendung nur eine Global.asa-Datei haben.

## ASA-Dateiformat - Weitere Informationen

ASA-Dateien sind einfache Textdateien mit den folgenden Informationen.

* Bewerbungsveranstaltungen
* Sitzungsereignisse
* \<object> Erklärungen
* TypeLibrary-Deklarationen
* die #include-Direktive

## Beispiel einer ASA-Datei

Eine Global.asa-Datei könnte etwa so aussehen.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Verweise

* [ASP Global.asa-Datei - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

