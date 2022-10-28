{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR-Datei - Dateiformat für Zertifikatsignierungsanforderung",
  "description" :"Erfahren Sie, was eine CSR-Datei und APIs sind, die CSR-Dateien erstellen und öffnen können.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
"identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Was ist eine CSR-Datei?

Eine CSR-Datei ist eine **Certificate Signing Request**-Datei, die verwendet wird, um ein SSL/TLS-Zertifikat anzufordern. Wenn Sie Ihr SSL/TLS-Zertifikat benötigen, generieren Sie die CSR auf demselben Server, auf dem sie schließlich installiert wird. Diese CSR-Datei wird mit der Zertifizierungsstelle (CA) zur Erstellung des Zertifikats geteilt. Es enthält Informationen wie den allgemeinen Namen, die Organisation, das Land und vor allem den **öffentlichen Schlüssel**, der in Ihre Zertifikatsdatei integriert und mit dem entsprechenden privaten Schlüssel signiert ist.

Zu den Anwendungen, die **CSR-Dateien öffnen** können, gehören OpenSSL und Microsoft IIS.

## Format der Anforderungsdatei für die Zertifikatsignierung

Eine CSR-Datei wird in einem Base-64-PEM-Format erstellt, das in einem einfachen Texteditor wie Microsoft Notepad geöffnet und angezeigt werden kann. Sie enthält eine Kopfzeile **-----BEGIN NEW CERTIFICATE REQUEST-----** am Anfang der Datei und eine Fußzeile **-----END NEW CERTIFICATE REQUEST-----** at das Ende der Datei.

### Wie sieht eine CSR-Datei aus?

Ein einfaches Beispiel für eine CSR-Datei ist wie folgt.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## Welche Informationen sind in einem CSR enthalten?

Eine CSR-Datei enthält die folgenden Informationen.

1. „Informationen über Unternehmen und Website“ – Umfasst Informationen wie den allgemeinen Namen, die Organisation, die Organisationseinheit, die Stadt/den Ort, das Bundesland/das Bundesland/die Region (S), das Land und die E-Mail-Adresse
1. „Public Key“ – Er ist im Zertifikat enthalten und dient zur Verschlüsselung übertragener Daten, die mit dem entsprechenden privaten Schlüssel entschlüsselt werden
1. "Informationen zu Schlüsseltyp und -länge" - Dies ist normalerweise RSA 2048, kann aber auch in größeren Größen wie RSA 4096+ vorliegen

## Verweise

* [Konzeptanwendungsserver](https://github.com/Devronium/ConceptApplicationServer)

