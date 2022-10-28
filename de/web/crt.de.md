{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt-Datei", "crt-Dateiformat", "crt-Dateityp", "Datei", "Typ", "was ist eine crt-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Dateiformat für Sicherheitszertifikate",
  "description":"Erfahren Sie mehr über das CRT-Dateiformat und APIs, die CRT-Dateien erstellen und öffnen können.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine CRT-Datei?

Eine Datei mit der Erweiterung .crt ist eine Sicherheitszertifikatdatei, die von sicheren Websites verwendet wird, um sichere Verbindungen von einem Webserver zu einem Browser herzustellen. Sichere Websites ermöglichen die Sicherung von Datenübertragungen, Anmeldungen und Zahlungskartentransaktionen und bieten ein geschütztes Surfen auf der Website. Wenn Sie eine sichere Website öffnen, sehen Sie ein „Schloss“-Symbol in der Adressleiste. Wenn Sie darauf klicken, können Sie die Details des installierten Zertifikats anzeigen. Internationale Unternehmen wie Verisign und Thawte vertreiben diese SSL-Zertifikate.

## CRT-Dateiformat

CRT-Dateien sind im ASCII-Format und können in einem beliebigen Texteditor geöffnet werden, um den Inhalt der Zertifikatsdatei anzuzeigen. Es folgt dem X.509-Zertifizierungsstandard, der die Struktur des Zertifikats definiert. Es definiert die Datenfelder, die im SSL-Zertifikat enthalten sein sollen. CRT gehört zum PEM-Format von Zertifikaten, bei denen es sich um Base64-ASCII-codierte Dateien handelt.

### PEM-Dateistruktur

Eine PEM-Datei kann mehrere Zertifikate haben. In einem solchen Fall folgt jedes Zertifikat in der PEM-Datei der folgenden Struktur.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Beispiel für ein CRT-Dateiformat

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Verweise ##

* [Öffentliche Schlüssel, private Schlüssel und Zertifikate](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

