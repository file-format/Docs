{
  "date": "2019-10-11",
  "keywords": [
"crt",
"comhad crt",
"formáid comhaid crt",
"cineál comhaid crt",
"comhad",
"cineál",
"cad is comhad crt ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT - Formáid Chomhaid an Teastais Slándála",
  "description": "Foghlaim faoi fhormáid comhaid CRT agus APIanna ar féidir leo comhaid CRT a chruthú agus a oscailt.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-gat"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad CRT ann?

Is comhad deimhnithe slándála é comhad a bhfuil síneadh .crt aige a úsáideann suíomhanna gréasáin slána chun naisc shlána a bhunú ó fhreastalaí gréasáin go brabhsálaí. Is féidir le suíomhanna gréasáin slán aistrithe sonraí, logáil isteach, idirbhearta cártaí íocaíochta, agus brabhsáil chosanta a sholáthar don láithreán. Má osclaíonn tú suíomh Gréasáin slán, feiceann tú deilbhín glas” sa bharra seoltaí. Má chliceálann tú air, is féidir leat sonraí an deimhnithe suiteáilte a fheiceáil. Dáileann cuideachtaí idirnáisiúnta ar nós Verisign agus Thawte na deimhnithe SSL seo.

## Formáid Chomhaid CRT

Tá comhaid CRT i bhformáid ASCII agus is féidir iad a oscailt in aon eagarthóir téacs chun a bhfuil sa chomhad teastais a fheiceáil. Leanann sé an caighdeán deimhniúcháin X.509 a shainíonn struchtúr an deimhnithe. Sainmhíníonn sé na réimsí sonraí ba cheart a áireamh sa deimhniú SSL. Baineann CRT le formáid PEM deimhnithe ar comhaid ionchódaithe Base64 ASCII iad.

### Struchtúr Comhad PEM

Is féidir le teastais iolracha a bheith ag comhad PEM. I gcás den sórt sin, leanann gach deimhniú sa chomhad PEM an struchtúr seo a leanas.

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

### Sampla Formáid Comhaid CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Tagairtí ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

