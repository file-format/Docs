{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"apkg tiedosto",
"apkg tiedostomuoto",
"apkg tiedostotyyppi",
"tiedosto",
"tyyppi",
"Mikä on APKG-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG - Anki Flashcard Deck -tiedostomuoto",
  "description": "Opi APKG-tiedostosta ja sovellusliittymistä, jotka voivat luoda ja avata niitä.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-fig"
}
},
  "lastmod": "2021-06-16"
}

## Mikä on APKG-tiedosto?

Tiedosto, jonka laajennus on .apkg, on flashcard-paketti, joka on luotu käytettäväksi [Anki](https://ankiweb.net/about)-ohjelmistosovelluksessa, joka on flashcard-pohjainen oppimisohjelma. Se sisältää [HTML](/web/html/) tekstiä, joka ladataan ja näytetään Anki-sovelluksessa, ja siinä voi olla lisäksi kuvia ja ääniä visuaalista ja kuultavaa oppimista varten. Ankin avulla käyttäjät voivat luoda omia Anki-flashcard-pakkoja sekä tuoda muiden käyttäjien korttipakkauksia.

## APKG-tiedostomuoto

Anki-korttipakat luodaan malleista, jotka on kirjoitettu HTML-kielellä, joka on kuuluisa ja yleinen verkkosivujen luomisen kieli. Pakkakorttien muotoilu tehdään CSS:llä, joka on web-sivujen muotoiluun käytetty kieli. Tyyli sisältää muutoksia:

 * font-family - Kortissa käytettävän fontin nimi.
 * font-size - Fontin koko pikseleinä.
 * tekstin tasaus – Määrittää, tasataanko teksti keskelle, vasemmalle vai oikealle.
 * väri - Määrittää tekstin värin, joka voi olla yksinkertaisia värinimiä, kuten sininen, punainen jne. tai HTML-värikoodeja.
 * background-color - Määrittää kortin taustavärin

Tyylitiedot jaetaan kaikkien korttien kesken, mikä vaikuttaa kaikkiin kortteihin, kun muutos tehdään. Seuraava esimerkki käyttää keltaista taustaa kaikissa korteissa paitsi ensimmäistä:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Anki-kortilla olevien kuvien koon muuttaminen voidaan ohjata seuraavasti.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascriptin upottaminen Anki-kortteihin

Anki-korttiin on mahdollista upottaa [Javascript](/web/js/) korttipohjien avulla. Javascriptin edistyneen tason vuoksi sen tukea ei kuitenkaan tarjota. Lisäksi renderöintilaitteet voivat näyttää Javascriptin toteutusvaikutukset kortilla eri tavalla, jolloin toteutus on testattava kaikilla laitteilla. Tietyt Javascript-ominaisuudet, kuten window.alert, vaikeuttavat kirjoittamasi Javascript-koodin virheenkorjausta.

## Viitteet ##

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

