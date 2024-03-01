{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDM-tiedosto - Handheld Device Markup Language File",
  "description": "Opi HDM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HDM-tiedostoja.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-fim"
}
},
  "lastmod": "2022-10-12"
}

## Mikä on HDM-tiedosto?

HDM-tiedosto on sivunkuvauskielen verkkosivutiedosto, joka luodaan Handheld Device Markup Language (HDML) -kielellä. Se sisältää merkintätunnisteita, jotka ovat samankaltaisia kuin [HTML](/web/html/)-kieli, mutta se on suunniteltu kädessä pidettäville elektronisille laitteille, kuten älypuhelimille ja PDA-laitteille. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) lähetettiin W3C:lle standardointia varten, mutta niistä ei voi tulla standardia. HDM perustuu [HDML](/web/hdml/)-tiedostomuodon määrityksiin, jotka ovat saatavilla W3-verkkosivustolla.

## HDM-tiedostomuoto – lisätietoja

HDM-tiedosto koostuu merkintätageista, jotka renderöidään visuaalisesti suunnitellulle verkkosivustolle kämmenlaitteilla. HDM-tiedostot kopioidaan laitteisiin käyttämällä HDTP-protokollaa (Handheld Device Transport Protocol) HTML-sivuilla käytettävän HTTP-protokollan sijaan.

## HDML-tiedostoelementit

Seuraavassa on luettelo elementeistä, jotka tarjoavat ajonaikaisen ympäristön HDML:lle ja joita kutsutaan käyttäjäagentiksi.

|Elementti|Kuvaus|
---|---|
|Kortit|Tämä on HDML:n perusrakennuspalikka, ja se näyttää ja antaa käyttäjälle mahdollisuuden olla vuorovaikutuksessa tietokorttien kanssa. |
|Kannet|HDML-kortit on ryhmitelty pakiksi. HDML-paketti on samanlainen kuin HTML-sivu, koska se tunnistetaan URL-osoitteella [RFC1738] ja se on palvelimelta pyydetty ja käyttäjäagentin välimuistiin tallentama sisältöyksikkö.|
|Toiminnot|Toiminnot voivat olla PREV-, SOFT1-SOFT8- ja HELP-tyyppisiä. Nämä ovat abstrakteja ja niitä tuetaan käyttöliittymässä käyttäjäagenttikohtaisella tavalla.|
|Toiminnot|Toiminto on kuin joukko toisiinsa liittyviä kortteja, jotka suorittavat yhden loogisen toiminnon. Nämä voivat kattaa yhden tai useamman kannen. HDML-navigointi- ja tilamalli rakentuu toimintojen ympärille.|
|Historiapohjainen navigointi|Käyttäjäagentti ylläpitää historiaa käyttäjälle näytetyistä korteista. Jokainen käytetty kortti lisätään korttihistoriaan. Käyttäjäagentin avulla käyttäjä voi siirtyä helposti takaisin edelliseen korttiin historiassa.|

## Viitteet

* [HDML – Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML-tiedot – W3-koulut](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


