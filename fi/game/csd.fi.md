{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lisätietoja CSD Steam Game Data Backup -tiedostomuodosta ja API:ista.",
  "title" : "CSD-tiedostomuoto - Steam-pelin tietojen varmuuskopiotiedosto",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd-fi",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Mikä on CSD-tiedosto?

CSD-tiedosto on pelipalvelun **Steam** luoma pelin varmuuskopiotiedosto, jonka avulla käyttäjät voivat ladata ja hallita **Valve**-pelejä. Se sisältää peleihin liittyvät varmuuskopiotiedot, joita voidaan käyttää poistettujen pelien palauttamiseen. Steam pystyy palauttamaan pelin CSD-tiedostosta vain, jos peli on ladattu, asennettu ja korjattu Steamin kautta. Palauttaaksesi pelin CSD-tiedostosta, käytä vaihtoehtoa Steam → Backup and Restore Gamesteam ja valitse tiedosto.

## CSD-tiedostomuoto – lisätietoja

CSD-tiedostomuodon sisäinen rakenne ei ole saatavilla julkisesti, eivätkä sen tiedostomuotomääritykset ole saatavilla kehittäjien viitteeksi. CSD-tiedostojen mukana on CSM- ja ISS-tiedostoja, jotka ovat myös Steam-pelitiedostomuotoja.

### Mistä löytää Steam-varmuuskopiotiedostoja?

Kaikki Steam-varmuuskopiotiedostot löytyvät seuraavista paikoista:

 * C:\Ohjelmatiedostot (x86)\Steam\steamapps\common\<game name> \ :
 * \cfg\ - Mukautetut kokoonpanot ja asetusskriptit
 * \downloads\ - Mukautettu sisältö moninpeleihin
 * \maps\ - Mukautetut kartat, jotka on asennettu tai ladattu moninpelien aikana
 * \materials\ - Mukautetut tekstuurit ja pinnat
 * \SAVE\ - Yhden pelaajan tallennetut pelit

Kolmannen osapuolen luomien pelien sijainti voi kuitenkin olla erilainen, ja sen määrittää pelin kehittäjä.

### Palauttaminen CSD-varmuuskopiotiedostosta

Asenna Steam ja kirjaudu sisään oikealle Steam-tilille (lisäohjeita on kohdassa Steamin asentaminen)
 * Käynnistä Steam
 * Napsauta Steam-sovelluksen vasemmassa yläkulmassa Steam.
 * Valitse Varmuuskopioi ja palauta pelit...
 * Valitse Palauta edellinen varmuuskopio
 * Selaa pelin varmuuskopiotiedostojen sijaintiin
 * Jatka Steam-ikkunoiden läpi asentaaksesi tarvittavat pelit.

## Viitteet

 * [Steamin varmuuskopiointiominaisuuden käyttäminen](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

