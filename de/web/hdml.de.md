{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Handheld Device Markup Language File",
  "description":"Erfahren Sie mehr über das HDML-Dateiformat und APIs, die HDML-Dateien erstellen und öffnen können.",
  "linktitle" :"HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Was ist eine HDML-Datei?

Eine Datei mit der Erweiterung .hdml (Handheld Device Markup Language) ist eine Auszeichnungssprache zum Erstellen von Webseiten für tragbare elektronische Geräte wie Handheld-Computer, Smartphones und Informationsanzeigegeräte. HDML soll eine Erweiterung der Sprache [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) sein. HDML ähnelt HTML, jedoch für drahtlose und tragbare Geräte mit kleinen Displays wie PDAs, Mobiltelefone usw. Es wurde durch WML ersetzt, für das es einen wichtigen Einfluss hatte.

## HDML-Dateiformat – Weitere Informationen

HDML ist eine Markup-Sprache für Handheld-Geräte, die ähnlich wie HTML auf Markup-Tags basiert. HDML wurde dem W3C zur Standardisierung vorgelegt, wurde aber nie zum Standard. Seine Dateiformatspezifikationen sind jedoch auf der [W3-Website] (https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) als Referenz verfügbar. Die [Syntax für die Sprache HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) ist als Referenz für Entwickler verfügbar und kann für die Entwicklung von Beispielanwendungen verwendet werden.

## HDML-Elemente

Im Folgenden finden Sie eine Reihe von Elementen, die eine Laufzeitumgebung für HDML bereitstellen und als User Agent bezeichnet werden.

|Element|Beschreibung|
---|---|
|Karten|Dies ist der grundlegende Baustein von HDML und zeigt Informationskarten an und ermöglicht es dem Benutzer, mit ihnen zu interagieren. |
|Decks|HDML-Karten werden in Decks gruppiert. Ein HDML-Deck ähnelt einer HTML-Seite, da es durch die URL [RFC1738] identifiziert wird und die Inhaltseinheit ist, die von einem Server angefordert und vom Benutzeragenten zwischengespeichert wird.|
|Aktionen|Aktionen können vom Typ PREV, SOFT1-SOFT8 und HELP sein. Diese sind abstrakt und werden in der Benutzeroberfläche auf benutzeragentenspezifische Weise unterstützt.|
|Aktivitäten|Eine Aktivität ist wie eine Gruppe verwandter Karten, die eine logische Funktion ausführen. Diese können sich über ein oder mehrere Decks erstrecken. Das HDML-Navigations- und Zustandsmodell ist um Aktivitäten herum strukturiert.|
|Verlaufsbasierte Navigation|Der Benutzeragent verwaltet einen Verlauf der Karten, die dem Benutzer angezeigt werden. Jede Karte, auf die zugegriffen wird, wird der Kartenhistorie hinzugefügt. Der Benutzeragent ermöglicht es dem Benutzer, einfach zurück zur vorherigen Karte in der Historie zu navigieren.|

## Verweise

* [HDML – Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML-Spezifikationen – W3-Schulen] (https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

