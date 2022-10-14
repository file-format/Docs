{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7-Zertifikatsdatei",
  "description":"Erfahren Sie mehr über das P7C-Dateiformat und APIs, die P7C-Dateien erstellen und öffnen können.",
  "linktitle" :"P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine P7B-Datei?

Eine P7B-Datei ist eine Sicherheitszertifikatdatei, die ein sicheres digitales Zertifikat zum Authentifizieren einer Person oder eines Geräts enthält. Ähnlich wie eine [.cer](/de/web/cer/)-Zertifikatsdatei kann eine P7B-Datei mit der Option „Zertifikat installieren“ installiert werden, indem Sie die Rechtsklick-Option auf die Datei verwenden. P7B verwendet andere Formatierungsoptionen als das CER-Dateiformat. Es enthält eine oder mehrere digitale X.509-Zertifikatsdateien, die die base64-Codierung (ASCII) verwenden. P7B-Dateien werden als [ZIP](/de/compression/zip/)-Datei empfangen oder von der Zertifizierungsstelle empfangen.

## P7B-Dateiformat

P7B-Dateien werden als reine ASCII-Dateien gespeichert, die in jedem Texteditor geöffnet werden können. Es enthält den öffentlichen Schlüssel, der eine verschlüsselte Zeichenfolge ist, die aus Sicht der Lesbarkeit bedeutungslos ist.

### Beispiel für ein P7B-Dateiformat

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Verweise ##

* [Public-Key-Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Wie erstelle ich eine P7C-Datei?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

