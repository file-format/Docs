{
  "date": "2021-08-04",
  "keywords": [
"mod",
"mp3",
"tiedosto",
"laajennus",
"muoto",
"mikä on mod-tiedostomuoto",
"musiikkia",
"mod-tiedostomuoto",
"mod vs MP3",
"mod-tiedostomuodon määrittely"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MOD-tiedostomuodosta ja API-liittymistä, jotka voivat luoda, muuntaa ja avata MOD-tiedostoja.",
  "title": "MOD - musiikkimoduulitiedosto",
  "linktitle": "MOD",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mo-fid"
}
},
  "lastmod": "2021-08-04"
}

## Mikä on MOD-tiedosto?
Tiedosto, jonka tarkenne on .mod, on musiikkimoduulitiedosto, joka on luotu käyttämällä vakiomusiikkimoduulimuotoa, joka perustuu Karsten Obarskin kehittämään **Amiga-moduulimuotoon** ja julkaistu **Ultimate Soundtracker** -ohjelmistolla Commodorelle. Amiga järjestelmä. Kuten [MIDI](/audio/mid/)-tiedosto, se koostuu nuottikuvioista ja ääninäytteistä, jotka edustavat erilaisia instrumentteja, jotka toistetaan nuottien mukaan. MOD-tiedostoja käytetään erityisesti videopeleissä taustamusiikkina ja **demoscene**-tietokonetaiteen alakulttuurissa.

## MOD-tiedostomuoto

MOD on tietokonetiedostomuoto, jonka perustehtävä on esittää musiikkia, ja se oli ensimmäinen moduulitiedostomuoto. MOD-tiedostot käyttävät .mod-tiedostotunnistetta, paitsi **Amiga**, joka lukee tiedoston otsikon määrittääkseen tiedostotyypin, joten se ei ole riippuvainen tiedostopäätteistä. MOD-tiedosto koostuu joukosta erilaisia soittimia näytteiden muodossa, useista kuvioista, jotka määrittelevät, miten ja milloin näytteet tulee soittaa, sekä luettelosta, mitä kuvioita toistetaan missä järjestyksessä.

### MOD-tiedostomuodon tekniset tiedot

MOD-tiedostomalli on itse asiassa suunniteltu sekvensserin käyttöliittymässä taulukoksi, jossa on yksi sarake kanavaa kohden, joten tässä taulukossa on neljä saraketta (yksi jokaiselle Amiga-laitteistokanavalle. Jokaisessa sarakkeessa on 64 riviä).

Taulukon solu voi saada jonkin seuraavista toiminnoista tapahtumaan sen sarakkeen kanavalla, kun sen rivin aika saavutetaan:

- Aloita soitin soittamaan uutta nuottia tässä kanavassa annetulla äänenvoimakkuudella, mahdollisesti erikoistehosteella
- Muuta nykyisen nuotin äänenvoimakkuutta tai erikoistehostetta
- Muuta kuvion kulkua; hypätä tiettyyn kappaleen tai kuvion paikkaan tai silmukaan kuvion sisällä
- Älä tee mitään; kaikki tällä kanavalla toistuvat nuotit jatkuvat

Instrumentti on yksi näyte sekä valinnainen määritys siitä, mikä osa näytteestä voidaan toistaa kiinteän sävelen säilyttämiseksi.

### Ajoitus
Vähimmäisaikajakso oli 0,02 sekuntia alkuperäisessä MOD-tiedostossa tai pystysuora tyhjennys (VSync) -väli, koska alkuperäinen ohjelmisto käytti näytön VSync-ajoitusta 50 Hz:llä (PAL) tai 60 Hz:llä (NTSC:llä). ajoitusta varten.

## Viitteet

* [MOD (tiedostomuoto) - Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))


