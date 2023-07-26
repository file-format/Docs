{
  "date" : "2019-10-11",
  "keywords" :[ "tgs-Datei", "tgs-Dateiformat", "was ist eine tgs-Datei", "Datei", "tgs-Beispiel", "tgs-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animated Sticker File Format",
  "description":"Erfahren Sie mehr über das TGS-Dateiformat und APIs, die TGS-Dateien erstellen und öffnen können.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Was ist eine TGS-Datei?

Eine Datei mit der Erweiterung .tgs ist eine animierte Aufkleberdatei, die vom plattformübergreifenden Nachrichtendienst [Telegram](https://core.telegram.org/stickers#animated-stickers) eingeführt wurde. Animierte Aufkleber werden von Benutzern von Messaging-Apps verwendet, um im Gegensatz zu den statischen Grafiken, bei denen es sich um Standbilder handelt, verbesserte und lebendigere Inhalte in Nachrichten zu senden. Telegram verwendete ursprünglich das Dateiformat [WEBP](/de/image/webp/) für Standbildaufkleber. Das TGS-Dateiformat kann Animationsdaten mit höheren Auflösungen und kleinerer Dateigröße im Vergleich zu den statischen WEBP-Aufklebern speichern. TGS-Dateien können mit Anwendungen wie Telegram, 7-zip, Apple Archive Utility und Corel WinZip geöffnet werden.

## TGS-Dateiformat

Telegram führte das TGS-Dateiformat bereits im Juli 2019 basierend auf der Lottie-Bibliothek ein. Eine TGS-Datei besteht aus [JSON](/de/web/json/)-Text, der aus einer Animation in Adobe After Effects exportiert wird. Der exportierte JSON-Text wird mit der gzip-Komprimierung komprimiert, wodurch die Dateigröße reduziert wird. Die JSON-Informationen über die Textdatei werden in einer Textdatei gespeichert, die die Grundlage für hohe Komprimierungsraten bildet.

### Technische Daten der TGS-Aufkleber

Das TGS-Dateiformat erlegt der Erstellung animierter TGS-Sticker bestimmte Einschränkungen auf. Eine animierte TGS-Datei:

* Die Aufkleber-/Leinwandgröße muss 512 x 512 Pixel betragen.
* Aufkleberobjekte dürfen die Leinwand nicht verlassen.
* Die Animationslänge darf 3 Sekunden nicht überschreiten.
* Alle Animationen müssen wiederholt werden.
* Die Stickergröße darf nach dem Rendern in Bodymovin 64 KB nicht überschreiten.
* Alle Animationen müssen mit 60 Bildern pro Sekunde laufen.

### TGS-JSON-Beispieltext

Ein animierter Beispielsticker enthält nach dem Entpacken den folgenden JSON-Textinhalt.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Verweise ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

