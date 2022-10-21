{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","mhtml-Datei", "mhtml-Dateiformat", "mhtml-Dateityp", "Datei", "Typ", "was ist eine mhtml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME-HTML-Datei",
  "description":"Erfahren Sie mehr über das MHTML-Dateiformat und APIs, die MHTML-Dateien erstellen und öffnen können.",
  "linktitle" :"MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine MHTML-Datei?

Dateien mit der Erweiterung MHTML stellen ein Archivformat für Webseiten dar, das von einer Reihe verschiedener Anwendungen erstellt werden kann. Das Format wird als Archivformat bezeichnet, da es den **[HTML](/de/web/html/)**-Webcode und die zugehörigen Ressourcen in einer einzigen Datei speichert. Diese Ressourcen umfassen alles, was mit der Webseite verknüpft ist, wie Bilder, Applets, Animationen, Audiodateien und so weiter. MHTML-Dateien können in einer Vielzahl von Anwendungen wie Internet Explorer und Microsoft Word geöffnet werden. Microsoft Windows verwendet das MHTML-Dateiformat zum Aufzeichnen von Problemszenarien, die während der Verwendung einer Anwendung unter Windows beobachtet wurden, die Probleme aufwirft. Das MHTML-Dateiformat codiert die Seiteninhalte ähnlich den in message/rfc822 definierten Spezifikationen, bei denen es sich um E-Mail-bezogene Spezifikationen im Klartext handelt. Die tatsächlichen Spezifikationen des Formats sind in [RFC 2557] (https://tools.ietf.org/html/rfc2557) beschrieben.

## MHTML-Dateiformat

MHTML ist wegen seiner Fähigkeit, HTML-Webseiten zusammen mit seinen Ressourcen in einem einzigen Webarchiv zu kodieren, auch als MIME-Kapselung von zusammengefassten HTML-Dokumenten bekannt. Gemäß den RFC 2557-Spezifikationen ist ein aggregiertes Dokument eine MIME-codierte Nachricht, die eine Root-Ressource (Objekt) sowie andere Ressourcen enthält, die über URIs damit verknüpft sind. Solche anderen Ressourcen können Darstellungen von Inline-Bildern, Stylesheets, Applets usw. sein. Außerdem können diese die Wurzel anderer Multimedia-Dokumente sein. Die vollständigen Dokumentspezifikationen für das MHTML-Dateiformat sind in [RFC 2557] (https://tools.ietf.org/html/rfc2557) beschrieben und sollten für jede Art von Anwendungsentwicklung zum Lesen/Schreiben dieses Dateiformats herangezogen werden. Der Standard spezifiziert, dass die zu referenzierenden Körperteile entweder durch eine Content-ID oder durch eine Content-Location identifiziert werden können.

### MIME-Content-Header

Ein MIME-Inhaltsheader, Content-Location, wird definiert, um URI-Verweise auf Ressourcen in anderen Körperteilen aufzulösen. Dieser Header kann in jeder Nachrichten- oder Inhaltsüberschrift vorkommen.

### Content-Location-Header

Eine Content-Location ist eine Darstellung eines URI, der den Inhalt eines Körperteils bezeichnet, an dem er platziert ist. Sein Wert kann ein absoluter oder ein relativer URI sein. Es kann verwendet werden, um eine Ressource zu kennzeichnen, die von einigen oder allen Empfängern einer Nachricht nicht abgerufen werden kann. Eine einzelne Nachricht darf nur einen einzigen Content-Location-Header haben. Beispiel einer mehrteiligen/zusammenhängenden Struktur, die Körperteile mit sowohl Content-Location- als auch Content-ID-Beschriftungen enthält:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URIs von MHTML-Aggregaten

Der URI des MHTML-Aggregats unterscheidet sich von dem seines Stamm-URI. Das Header-Feld Content-Location sollte für das gesamte Aggregat gelten, wenn es in der Überschrift einer mehrteiligen/zusammenhängenden Überschrift verwendet wird. In ähnlicher Weise kann sich der abgerufene Satz von Ressourcen von dem Satz von Ressourcen unterscheiden, der unter Verwendung der Inhaltsorte seiner Teile abgerufen wird, wenn der URI, der sich auf das MHTML-Aggregat bezieht, zum Abrufen dieses Aggregats verwendet wird. Beispielsweise kann das Abrufen eines MHTML-Aggregats eine alte Version zurückgeben, während das Abrufen des Stamm-URI und seiner inline verknüpften Objekte eine neuere Version zurückgeben kann.

## Verweise

* [MIME-Kapselung aggregierter Dokumente – RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML-Dateiformat – von Wikipedia](https://en.wikipedia.org/wiki/MHTML)

