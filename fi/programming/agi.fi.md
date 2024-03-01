{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AGI-tiedosto - Asterisk Gateway Interface -tiedostomuoto",
  "description":"Opi AGI-tiedostomuodosta esimerkkien ja API:iden avulla, jotka voivat luoda ja avata AGI-tiedostoja.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mikä on AGI-tiedosto?

AGI-tiedosto on komentosarjatiedosto, jota käyttää avoimen lähdekoodin puhelinjärjestelmä, Asterisk. Se sisältää tietoja, joita voidaan käyttää automatisoimaan prosesseja ja Asterisk-valintasuunnitelmaa. AGI-skriptitiedostoja käyttämällä voidaan muodostaa yhteyksiä relaatiotietokantoihin, kuten PostgreSQL tai MySQL. Lisäksi AGI-skriptien avulla voidaan käyttää myös muita ulkoisia resursseja. AGI-skriptit voivat siirtää valintasuunnitelman hallinnan ulkoiselle AGI-skriptille, jolloin Asterisk voi suorittaa monimutkaisia tehtäviä.

## AGI-tiedostomuoto - lisätietoja

AGI-skriptitiedostot tallennetaan tekstitiedostoina ja ne voidaan avata missä tahansa tekstieditorissa muutosten tekemistä varten.

### AGI-viestinnän vakiomalli

AGI-skripti lataa Asteriskin sille lähettämät muuttujat ja niiden arvot. Näiden muuttujien yleinen ulkoasu on seuraava.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Näitä muuttujia seuraa Asteriskin lähettämä tyhjä rivi, joka osoittaa, että AGI-skripti voi nyt hallita valintasuunnitelmaa.

### Ohjelmointikieli AGI-skriptitiedostoille

AGI-skriptit voidaan yleensä kirjoittaa Perlissä, [PHP](/programming/php/), [C](/programming/c/), Pascalissa tai Bourne Shellissä.

## Viitteet

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

