{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"apkg failą",
"apkg failo formatas",
"apkg failo tipas",
"failą",
"tipo",
"Kas yra APKG failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG – Anki Flashcard Deck failo formatas",
  "description": "Sužinokite, kas yra APKG failas ir API, kurios gali juos sukurti ir atidaryti.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-ltg"
}
},
  "lastmod": "2021-06-16"
}

## Kas yra APKG failas?

Failas su plėtiniu .apkg yra kortelių rinkinys, sukurtas naudoti [Anki](https://ankiweb.net/about) programinėje įrangoje, kuri yra kortelių pagrindu sukurta mokymosi programa. Jame yra [HTML](/web/html/) tekstas, kuris turi būti įkeltas ir rodomas Anki programoje, taip pat gali turėti vaizdų ir garsų, skirtų vaizdiniam ir garsiniam mokymuisi. Anki leidžia vartotojams sukurti savo Anki kortelių rinkinius, taip pat importuoti kitų naudotojų kortelių rinkinius.

## APKG failo formatas

Anki kortelių kaladės kuriamos iš šablonų, parašytų HTML – garsia ir įprasta tinklalapių kūrimo kalba. Denio kortelių stilius formuojamas naudojant CSS, kuri yra tinklalapių stiliaus formavimo kalba. Stilius apima šiuos pakeitimus:

 * font-family – šrifto, kuris bus naudojamas kortelėje, pavadinimas.
 * font-size – šrifto dydis pikseliais.
 * teksto lygiavimas – apibrėžia, ar tekstas turi būti lygiuojamas centre, kairėje ar dešinėje.
 * spalva – apibrėžia teksto spalvą, kuri gali būti paprasti spalvų pavadinimai, tokie kaip mėlyna, raudona ir kt., arba HTML spalvų kodai.
 * background-color – apibrėžia kortelės fono spalvą

Stiliaus informacija dalijamasi visoms kortelėms, o tai turi įtakos visoms kortelėms, kai atliekami pakeitimai. Toliau pateiktame pavyzdyje geltonas fonas bus naudojamas visose kortelėse, išskyrus pirmąją:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Vaizdų dydžio keitimas Anki kortelėje gali būti valdomas taip.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript įterpimas į Anki korteles

Naudojant kortelių šablonus galima įterpti [Javascript](/web/js/) į Anki kortelę. Tačiau dėl pažangaus Javascript lygio jo palaikymas neteikiamas. Be to, atvaizdavimo įrenginiai gali skirtingai parodyti Javascript diegimo poveikį kortelėje, todėl reikia išbandyti diegimą visuose įrenginiuose. Tam tikros Javascript funkcijos, pvz., window.alert, todėl sunku derinti jūsų parašytą Javascript kodą.

## Nuorodos Nr.

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

