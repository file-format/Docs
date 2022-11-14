{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM File - Privacy Enhanced Mail Certificate File Format",
  "description":"Meer informatie over PEM-bestandsindeling en API's die PEM-bestanden kunnen maken en openen.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Wat is een PEM-bestand?

Een PEM-bestand is een beveiligingscertificaatbestand dat wordt gebruikt om een veilig communicatiekanaal tussen een webserver en een browser tot stand te brengen. Het is Base64-gecodeerd en kan een privésleutel, servercertificaat en/of een combinatie van andere certificaten bevatten. PEM-bestanden lijken qua gebruik op .der-certificaatbestanden, maar worden opgeslagen als Base64-gecodeerde tekst in plaats van binaire gegevens. Andere vergelijkbare bestandsindelingen voor certificaten zijn onder meer [.cer](/nl/web/cer/)- en [.crt](/nl/web/crt/)-bestanden.

Toepassingen die **PEM-bestanden** kunnen openen** zijn onder meer teksteditors zoals Microsoft Notepad en Apple TextEdit.

## PEM-bestandsindeling

PEM is een containerbestandsindeling die de structuur en het coderingstype definieert van het bestand dat wordt gebruikt om de gegevens op te slaan. PEM-bestanden worden op schijf opgeslagen als Base64-gecodeerde bestandsindeling die niet door mensen leesbaar is. De standaard definieert dat een PEM-bestand begint met:

```
-----BEGIN <type>-----
```
en eindigt met:
```
-----END <type>-----
```

Alle andere inhoud hierin is base64-gecodeerd (hoofdletters en kleine letters, cijfers, + en /). Een enkel PEM-bestand kan uit meerdere blokken bestaan die door andere programma's kunnen worden gebruikt. Als een PEM-bestand meerdere certificaten bevat, wordt elk certificaat als volgt gescheiden door afzonderlijke blokken:

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

### PEM-bestandsvoorbeeld

Een PEM-bestand met CERTIFICATE-blok ziet er meestal als volgt uit:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Een PEM-bestand met RSA begint als volgt.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referenties ##

* [cryptografie met openbare sleutel](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hoe maak je een P7C-bestand aan?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

