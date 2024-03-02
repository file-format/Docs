{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad PEM - Formáid Chomhaid Teastais Ríomhphoist Fheabhsaithe Príobháideachta",
  "description": "Foghlaim faoi fhormáid comhaid PEM agus APIanna ar féidir comhaid PEM a chruthú agus a oscailt.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-gam"
}
},
  "lastmod": "2022-09-14"
}

## Cad is comhad PEM ann?

Is comhad deimhnithe slándála é comhad PEM a úsáidtear chun cainéal cumarsáide slán a bhunú idir freastalaí gréasáin agus brabhsálaí. Tá sé ionchódaithe le Base64 agus d’fhéadfadh eochair phríobháideach, teastas freastalaí, agus/nó meascán de theastais eile a bheith ann. Tá comhaid PEM cosúil le comhaid deimhnithe .der i dtéarmaí úsáide ach stóráiltear iad mar théacs ionchódaithe Base64 seachas sonraí dénártha. I measc formáidí comhaid teastais eile tá comhaid [.cer](/web/cer/) agus [.crt](/web/crt/).

I measc na bhfeidhmchlár ar féidir **comhaid PEM a oscailt** tá eagarthóirí téacs ar nós Microsoft Notepad agus Apple TextEdit.

## Formáid Chomhaid PEM

Is formáid comhaid coimeádáin é PEM a shainíonn struchtúr agus cineál ionchódaithe an chomhaid a úsáidtear chun na sonraí a stóráil. Stóráiltear comhaid PEM ar diosca mar fhormáid comhaid ionchódaithe Base64 nach bhfuil inléite ag an duine. Sainmhíníonn an caighdeán go dtosaíonn comhad PEM le:

```
-----BEGIN <type>-----
```
agus críochnaíonn sé le:
```
-----END <type>-----
```

Tá gach ábhar eile laistigh díobh seo ionchódaithe base64 (cás mór agus litreacha beaga, digití, +, agus /). Is féidir le hiliomad bloic a bheith i gcomhad PEM amháin ar féidir le cláir eile iad a úsáid. Má tá teastais iolracha i gcomhad PEM, tá gach teastas scartha le bloic aonair mar seo a leanas:

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

### Sampla Comhad PEM

Is gnách go mbíonn cuma chomhad seo a leanas ar chomhad PEM le bloc CERTIFICATE:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Tosaíonn comhad PEM le RSA mar seo a leanas.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Tagairtí ##

* [Criptagrafaíocht Eochracha Poiblí](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Conas comhad P7C a chruthú?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


