{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7-Zertifikatsdatei",
  "description":"Erfahren Sie mehr über das P7C-Dateiformat und APIs, die P7C-Dateien erstellen und öffnen können.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine P7C-Datei?

Eine P7C-Datei ist wie andere Sicherheitszertifikatsdateien ein digitales Zertifikat, das zur Authentifizierung der Identität über das Netzwerk verwendet wird. Anwendungen, die Zertifikate verwenden, authentifizieren die Identität mithilfe des öffentlichen Schlüssels, der in diesen Zertifikatsdateien enthalten ist. Public-Key-Kryptographie oder asymmetrische Kryptographie verwendet Schlüsselpaare, von denen einer der öffentliche Schlüssel und der andere als privater Schlüssel bekannt ist. Der private Schlüssel wird für effektive Sicherheit sicher aufbewahrt, während der öffentliche Schlüssel mit anderen geteilt werden kann. Andere gängige Dateiformate für Zertifikate sind [CRT](/de/web/crt/), DER und PEM.

## P7C-Dateiformat – Weitere Informationen

P7C-Dateien werden als Binärdateien auf der Disc gespeichert und enthalten die öffentlichen Schlüsselinformationen, die mit kryptografischen Algorithmen basierend auf mathematischen Problemen generiert werden. Diese können in jedem Texteditor geöffnet werden, aber ihr Inhalt ist nicht in menschenlesbarer Form. Zu den Anwendungen, die P7C-Dateien öffnen können, gehören Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager und Microsoft Windows Contacts.

### Beispiel für ein P7C-Dateiformat

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Verweise ##

* [Public-Key-Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Wie erstellt man eine P7C-Datei?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

