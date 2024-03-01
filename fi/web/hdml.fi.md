{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Kämmenlaitteen merkintäkielitiedosto",
  "description": "Opi HDML-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata HDML-tiedostoja.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-fil"
}
},
  "lastmod": "2021-08-21"
}

## Mikä on HDML-tiedosto?

Tiedosto, jonka laajennus on .hdml (Handheld Device Markup Language), on sivunkuvauskieli, jolla luodaan verkkosivuja kannettaville elektronisille laitteille, kuten kämmentietokoneille, älypuhelimille ja tietojen näyttölaitteille. HDML:n sanotaan olevan [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language)-kielen laajennus. HDML on samanlainen kuin HTML, mutta langattomille ja kannettaville laitteille, joissa on pienet näytöt, kuten PDA:t, matkapuhelimet ja niin edelleen. Se korvattiin WML:llä, johon sillä oli tärkeä vaikutus.

## HDML-tiedostomuoto – lisätietoja

HDML on kämmenlaitteiden merkintäkieli, joka perustuu HTML:n kaltaisiin merkintätageihin. HDML lähetettiin W3C:lle standardointia varten, mutta siitä ei koskaan tullut standardia. Sen tiedostomuotomääritykset ovat kuitenkin saatavilla osoitteessa [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) viitteeksi. [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) on saatavana kehittäjien viitteeksi, ja sitä voidaan käyttää esimerkkisovelluskehitykseen.

## HDML-elementit

Seuraavassa on lista elementeistä, jotka tarjoavat ajonaikaisen ympäristön HDML:lle ja joita kutsutaan käyttäjäagentiksi.

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


