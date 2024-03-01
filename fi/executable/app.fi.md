{
  "date": "2023-02-02",
  "keywords": [
"sovellustiedosto",
"mikä on sovellustiedosto",
"tiedosto",
"kuinka avata sovellustiedosto",
"sovelluksen tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Opi APP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata APP-tiedostoja.",
  "title": "APP-tiedostomuoto - macOS-sovelluspaketti",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app-fi",
      "parent": "executable"
}
},
  "lastmod": "2023-02-02"
}

## Mikä on APP-tiedosto?

.app-tiedosto macOS:ssä on erityinen hakemistotyyppi, joka sisältää kaikki tietyn sovelluksen suorittamiseen tarvittavat tiedostot, mukaan lukien suoritettavan koodin, resurssit ja metatiedot. .app-laajennus viestittää käyttöjärjestelmälle, että tätä hakemistoa tulee käsitellä yhtenä yksikkönä erillisten tiedostojen kokoelman sijaan ja että se voidaan käynnistää suoraan Finderista tai Dockista.

Finder on oletusarvoinen tiedostonhallintasovellus macOS:ssä. Sen avulla voit selata ja järjestää tietokoneesi tiedostoja ja hakemistoja. Dock on macOS:n ominaisuus, joka tarjoaa nopean pääsyn usein käytettyihin sovelluksiin ja asiakirjoihin. Sekä Finderin että Dockin avulla voit käynnistää sovelluksia napsauttamalla niiden .app-tiedostoja, mikä avaa vastaavan sovelluspaketin. Kun käynnistät sovelluksen, .app-paketin suoritettava koodi suoritetaan, jolloin sovellus on käytettävissä. .app-tiedosto edustaa sovellusta tiedostojärjestelmässä ja tarjoaa käyttäjälle tavan käyttää ja käynnistää sovellusta.

Kun napsautat .app-tiedostoa hiiren kakkospainikkeella Finderissa macOS-järjestelmässä ja valitset Näytä paketin sisältö, näet sovelluspaketin sisäisen rakenteen. Tästä on hyötyä, jos haluat käyttää sovelluksen käyttämiä resursseja tai tiedostoja tai jos haluat tarkastaa sovelluksen sisällön vianmääritystä varten. .app-tiedoston paketin sisältö sisältää yleensä hakemistoja resursseille, kuten kuville ja äänille, sekä sovelluksen suoritettavan koodin. Tutkimalla .app-tiedoston sisältöä voit saada syvempää tietoa siitä, miten sovellus on koottu ja mitä se tekee.

## Kuinka avata APP-tiedosto?

Avaa .app-tiedosto macOS:ssä kaksoisnapsauttamalla tiedostoa Finderissa. Tämä käynnistää .app-paketin sisältämän sovelluksen. Jos sovellus on asennettu järjestelmääsi ja se on liitetty .app-tiedostotyyppiin, kaksoisnapsauttamalla tiedostoa sovelluksen pitäisi käynnistyä automaattisesti. Jos sovellusta ei ole liitetty .app-tiedostotyyppiin, sinun on ehkä napsautettava tiedostoa hiiren kakkospainikkeella ja valittava Avaa sovelluksella valitaksesi sopiva sovellus, jolla se avataan.

Voit avata .app-tiedoston macOS:n terminaalissa käyttämällä open-komentoa. Voit tehdä tämän siirtymällä cd-komennolla hakemistoon, jossa .app-tiedosto sijaitsee, ja suorittamalla sitten seuraavan komennon:

```
open <AppName>.app 
```

missä<AppName> on sen sovelluksen nimi, jonka haluat käynnistää. Tämä käynnistää sovelluksen ikään kuin olisit kaksoisnapsauttanut sitä Finderissa. Open-komento on yleiskäyttöinen apuohjelma, jolla voidaan avata monenlaisia tiedostoja, mukaan lukien sovellukset, asiakirjat ja hakemistot. Kun käytät open-komentoa .app-tiedostossa, se käynnistää paketin sisältämän sovelluksen.

## Viitteet
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
