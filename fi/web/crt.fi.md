{
  "date": "2019-10-11",
  "keywords": [
"crt",
"crt tiedosto",
"crt tiedostomuoto",
"crt tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on crt-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT - suojaussertifikaatin tiedostomuoto",
  "description": "Opi CRT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CRT-tiedostoja.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on CRT-tiedosto?

Tiedosto, jonka laajennus on .crt, on suojausvarmennetiedosto, jota suojatut verkkosivustot käyttävät suojattujen yhteyksien luomiseen verkkopalvelimesta selaimeen. Suojatut verkkosivustot mahdollistavat tiedonsiirron, kirjautumisten, maksukorttitapahtumien turvaamisen ja suojatun selaamisen sivustolle. Jos avaat suojatun verkkosivuston, näet lukko-kuvakkeen osoitepalkissa. Jos napsautat sitä, voit tarkastella asennetun varmenteen tietoja. Kansainväliset yritykset, kuten Verisign ja Thawte, jakavat näitä SSL-varmenteita.

## CRT-tiedostomuoto

CRT-tiedostot ovat ASCII-muodossa, ja ne voidaan avata missä tahansa tekstieditorissa nähdäksesi varmennetiedoston sisällön. Se noudattaa X.509-sertifiointistandardia, joka määrittelee varmenteen rakenteen. Se määrittelee tietokentät, jotka tulee sisällyttää SSL-varmenteeseen. CRT kuuluu PEM-muotoon varmenteissa, jotka ovat Base64 ASCII -koodattuja tiedostoja.

### PEM-tiedostorakenne

PEM-tiedostolla voi olla useita varmenteita. Tässä tapauksessa jokainen PEM-tiedoston varmenne noudattaa seuraavaa rakennetta.

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

### Esimerkki CRT-tiedostomuodosta

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Viitteet ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

