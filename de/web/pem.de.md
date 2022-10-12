{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM-Datei - Privacy Enhanced Mail Certificate File Format",
  "description":"Erfahren Sie mehr über das PEM-Dateiformat und APIs, die PEM-Dateien erstellen und öffnen können.",
  "linktitle" :"PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Was ist eine PEM-Datei?

Eine PEM-Datei ist eine Sicherheitszertifikatdatei, die verwendet wird, um einen sicheren Kommunikationskanal zwischen einem Webserver und einem Browser einzurichten. Es ist Base64-codiert und kann einen privaten Schlüssel, ein Serverzertifikat und/oder eine Kombination anderer Zertifikate enthalten. PEM-Dateien ähneln in Bezug auf die Verwendung .der-Zertifikatsdateien, werden jedoch als Base64-codierter Text und nicht als Binärdaten gespeichert. Andere ähnliche Zertifikatsdateiformate sind [.cer](/de/web/cer/)- und [.crt](/de/web/crt/)-Dateien.

Zu den Anwendungen, die **PEM-Dateien öffnen** können, gehören Texteditoren wie Microsoft Notepad und Apple TextEdit.

## PEM-Dateiformat

PEM ist ein Containerdateiformat, das die Struktur und den Codierungstyp der Datei definiert, die zum Speichern der Daten verwendet wird. PEM-Dateien werden als Base64-codiertes Dateiformat auf der Disc gespeichert, das nicht für Menschen lesbar ist. Der Standard definiert, dass eine PEM-Datei beginnt mit:

```
-----BEGIN <type>-----
```
und endet mit:
```
-----END <type>-----
```

Alle anderen Inhalte darin sind base64-codiert (Groß- und Kleinbuchstaben, Ziffern, + und /). Eine einzelne PEM-Datei kann aus mehreren Blöcken bestehen, die von anderen Programmen verwendet werden können. Wenn eine PEM-Datei mehrere Zertifikate enthält, wird jedes Zertifikat wie folgt durch einzelne Blöcke getrennt:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Beispiel für eine PEM-Datei

Eine PEM-Datei mit CERTIFICATE-Block sieht normalerweise wie folgt aus:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Eine PEM-Datei mit RSA beginnt wie folgt.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Verweise ##

* [Public-Key-Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Wie erstellt man eine P7C-Datei?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

