{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM-Datei - Handheld Device Markup Language-Datei",
  "description":"Erfahren Sie mehr über das HDM-Dateiformat und APIs, die HDM-Dateien erstellen und öffnen können.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Was ist eine HDM-Datei?

Eine HDM-Datei ist eine Auszeichnungssprachen-Webseitendatei, die in der Handheld Device Markup Language (HDML) erstellt wird. Es enthält Markup-Tags ähnlich der Sprache [HTML](/de/web/html/), ist aber für tragbare elektronische Geräte wie Smartphones und PDAs konzipiert. Die [Spezifikationen des HDML-Dateiformats](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) wurden dem W3C zur Standardisierung vorgelegt, konnten aber nicht zum Standard werden. HDM basiert auf den [HDML](/de/web/hdml/)-Dateiformatspezifikationen, die auf der W3-Website verfügbar sind.

## HDM-Dateiformat – Weitere Informationen

Die HDM-Datei besteht aus Markup-Tags, die auf Handheld-Geräten zu einer visuell gestalteten Website gerendert werden. HDM-Dateien werden mithilfe des HDTP-Protokolls (Handheld Device Transport Protocol) anstelle des HTTP-Protokolls, das für HTML-Seiten verwendet wird, auf Geräte kopiert.

## Elemente der HDML-Datei

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
* [HDML-Spezifikationen – W3-Schulen](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

