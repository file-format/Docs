{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das KEY-Dateiformat und APIs, die KEY-Dateien erstellen und öffnen können.",
  "title" :"KEY-Dateiformat - Private Mail-Schlüsseldatei mit verbesserter Privatsphäre",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
"identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Was ist eine KEY-Datei?

Eine KEY-Datei ist der private Teil eines Sicherheitsmechanismus, der im PEM-Dateiformat (Privacy-Enhanced Mal) auf der Disc gespeichert wird. Es wird verwendet, um Informationen zu entschlüsseln, die zwischen einem Webbrowser und dem Webserver ausgetauscht werden, der die Browsing-Anfragen bedient. Eine KEY-Datei enthält verschlüsselte Zeichenfolgen, die für das menschliche Auge nutzlos sind, aber die Essenz des Verschlüsselns/Entschlüsselns des Informationsaustauschs als Teil des SSL-Zertifikats auf Webservern darstellen. KEY-Dateien werden automatisch generiert und auf Client-Seite installiert.

Sie können **KEY**-Dateien mit jedem Texteditor wie Microsoft Notepad (Windows), Apple TextEdit (Mac) oder GitHub Atom (plattformübergreifend) öffnen. KEY-Dateien ähneln den Dateiformaten [CRT](/de/web/crt/) und [CER](/de/web/cer/).

## KEY-Dateiformat – Weitere Informationen

KEY-Dateien werden als einfache Textdateien auf der Disc gespeichert, sind jedoch codierte Zeichenfolgen, die für Menschen nicht lesbar sind. Praktisch haben Benutzer kein Verständnis für die Zeichenfolgen, wenn sie in einem Texteditor geöffnet werden. Das private Schlüsselzertifikat ist vertraulich und sollte nicht an Dritte weitergegeben werden. Der vollständige Prozess der Sicherung des Informationsaustauschs über das Internet umfasst Folgendes:

* **Öffentlicher Schlüssel** - wird verwendet, um Benutzerinformationen für den Datenaustausch zwischen dem Browser und den Webservern zu verschlüsseln
* **Privater Schlüssel** - wird verwendet, um die Informationen zu entschlüsseln, wenn sie vom Webserver empfangen werden

Die SSL-Zertifikate, auch bekannt als X.509-Zertifikate, sind für jede Website einzigartig. KEY-Dateien mit der folgenden Syntax:

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

### Beispiel für eine KEY-Datei

Es folgt ein Beispiel für eine private Schlüsseldatei.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Verweise

* [Öffentliche Schlüssel, private Schlüssel und Zertifikate](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

